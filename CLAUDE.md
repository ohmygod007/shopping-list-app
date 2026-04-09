# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

단일 HTML 파일로 구성된 쇼핑 리스트 웹 앱. 별도 빌드 도구나 서버 없이 브라우저에서 직접 실행.

## 실행 방법

- 브라우저에서 `shopping-list.html`을 직접 열어 실행
- 데이터는 `localStorage`에 저장되어 새로고침 후에도 유지

## 아키텍처

- `shopping-list.html`: HTML, CSS, JS가 모두 포함된 단일 파일 앱
- 상태 관리: `items` 배열을 localStorage(`shopping-list` 키)와 동기화
- 렌더링: `render()` 함수가 상태 변경 시마다 전체 리스트를 다시 그림
- XSS 방지: `escapeHtml()` 함수로 사용자 입력을 이스케이프
