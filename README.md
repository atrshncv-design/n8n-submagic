# n8n + Submagic: Video Editing Automation

An n8n workflow ([`n8n-submagic.json`](n8n-submagic.json)) that automates short-video editing in **Submagic** (captions, effects, cuts) for Reels/Shorts production.

> **Status: experiment** — a personal automation experiment, not a production service.

## Problem

Manual editing of short videos (Reels, Shorts) took hours per project; the goal was to scale production.

## Solution

- n8n chain: **Google Drive Trigger** (new video detected) → HTTP request to the **Submagic API** (captions, transitions, music templates) → processed file returned → uploaded back to Google Drive → sent via **Telegram**
- Optional Telegram bot integration to trigger processing on demand
- Optimized prompts for subtitle and description generation

The workflow automates the routine part of editing; output still benefits from a human check before publishing.

## Stack

- n8n
- Submagic API
- Google Drive
- Telegram (optional)

---

# n8n + Submagic: Автоматизация видео-редактирования

n8n-workflow ([`n8n-submagic.json`](n8n-submagic.json)) для автоматизации редактирования коротких видео в **Submagic** (субтитры, эффекты, монтаж) в производстве Reels/Shorts.

> **Статус: experiment** — личный эксперимент по автоматизации, не production-сервис.

## Проблема

Ручной монтаж коротких видео (Reels, Shorts) отнимал часы на проект; нужно было масштабировать производство.

## Решение

- Цепочка n8n: **Google Drive Trigger** (появление нового видео) → HTTP-запрос к **Submagic API** (шаблоны субтитров, переходов, музыки) → готовый файл → загрузка обратно в Google Drive → отправка через **Telegram**
- Опционально — запуск через Telegram-бота по запросу
- Оптимизированные промпты для генерации субтитров и описаний

Workflow автоматизирует рутинную часть монтажа; перед публикацией результат всё же стоит проверить вручную.

## Стек

- n8n
- Submagic API
- Google Drive
- Telegram (опционально)
