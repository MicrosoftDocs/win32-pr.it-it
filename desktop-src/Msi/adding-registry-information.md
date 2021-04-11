---
description: La tabella del registro di sistema e le tabelle correlate del database di installazione contengono le informazioni del registro di sistema che l'applicazione deve scrivere nel registro di sistema.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Aggiunta di informazioni del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb299116b4e5c567d1e1f4b18f23c1e5b0447fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967296"
---
# <a name="adding-registry-information"></a>Aggiunta di informazioni del registro di sistema

La [tabella del registro](registry-table.md)di sistema e le tabelle correlate del database di installazione contengono le informazioni del registro di sistema che l'applicazione deve scrivere nel registro di sistema. Vedere il [gruppo di tabelle del registro di sistema](registry-tables-group.md). In questa sezione si aggiungono le informazioni che devono essere registrate nel computer dell'utente tramite l'esempio del blocco note.

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella del registro di sistema vuota.

[Tabella del registro di sistema](registry-table.md)



| Registro       | Radice | Codice                                 | Nome             | Valore    | Componente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfCharSet        | \#0      | Blocco note     |
| ClipPrecision  | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfClipPrecision  | \#2      | Blocco note     |
| Rotazione     | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfFaceName       | FixedSys | Blocco note     |
| Corsivo         | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfItalic         | \#0      | Blocco note     |
| Orientamento    | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfOrientation    | \#0      | Blocco note     |
| OutPrecision   | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfOutPrecision   | \#1      | Blocco note     |
| PageSettings   | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | fSavePageSetting | \#0      | Blocco note     |
| PitchAndFamily | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfPitchAndFamily | \#49     | Blocco note     |
| PointSize      | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | iPointSize       | \#120    | Blocco note     |
| Qualità        | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfQuality        | \#2      | Blocco note     |
| Barrato      | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfStrikeOut      | \#0      | Blocco note     |
| Peso         | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | lfWeight         | \#400    | Blocco note     |
| Wrap           | 2    | SOFTWARE \\ Microsoft \\ notepad Sample | fWrap            | \#0      | Blocco note     |



 

[Continua](specifying-shortcuts.md)

 

 



