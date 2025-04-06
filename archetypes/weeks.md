+++
title = "{{ replace .Name "_" " " | title }}"
date = {{ .Date }}
draft = true
type = "week"
layout = "week"
description = "Meal plan for the week of {{ .Name | replace "_" "/" }}"
week_data = "weeks/week_of_{{ .Name }}.yaml"
+++

## Meal Plan: Week of {{ .Name | replace "_" "/" }}

This week’s meal plan includes breakfast, lunch, and dinner ideas from Sunday through Saturday. See `data/{{ .Params.week_data }}` for the full details.

{{< meal-plan week="{{ .Params.week_data }}" >}}