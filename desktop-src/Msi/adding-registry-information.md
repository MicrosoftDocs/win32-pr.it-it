---
description: La tabella Del Registro di sistema e le tabelle correlate del database di installazione contiene le informazioni del Registro di sistema necessarie all'applicazione scritte nel Registro di sistema.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Aggiunta di informazioni del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df31ad20fef317d5d67f7f45a7b877511d4c35b05b1517c529693e787306b44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066411"
---
# <a name="adding-registry-information"></a>Aggiunta di informazioni del Registro di sistema

La [tabella Del Registro di](registry-table.md)sistema e le tabelle correlate del database di installazione contiene le informazioni del Registro di sistema necessarie per l'applicazione scritte nel Registro di sistema. Vedere gruppo [tabelle del Registro di sistema](registry-tables-group.md). In questa sezione si aggiungono le informazioni che devono essere registrate nel computer dell'utente dal Blocco note esempio.

Usare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella del Registro di sistema vuota.

[Tabella del Registro di sistema](registry-table.md)



| Registro       | Radice | Codice                                 | Nome             | Valore    | Componente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfCharSet        | \#0      | Blocco note     |
| ClipPrecision  | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfClipPrecision  | \#2      | Blocco note     |
| Scappamento     | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfFaceName       | Fixedsys | Blocco note     |
| Corsivo         | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfItalic         | \#0      | Blocco note     |
| Orientamento    | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfOrientation    | \#0      | Blocco note     |
| OutPrecision   | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfOutPrecision   | \#1      | Blocco note     |
| Pagesettings   | 2    | Esempio \\ di software Microsoft \\ Blocco note | fSavePageSetting | \#0      | Blocco note     |
| PitchAndFamily | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfPitchAndFamily | \#49     | Blocco note     |
| PointSize      | 2    | Esempio \\ di software Microsoft \\ Blocco note | iPointSize       | \#120    | Blocco note     |
| Qualità        | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfQuality        | \#2      | Blocco note     |
| Barrato      | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfStrikeOut      | \#0      | Blocco note     |
| Peso         | 2    | Esempio \\ di software Microsoft \\ Blocco note | lfWeight         | \#400    | Blocco note     |
| Wrap           | 2    | Esempio \\ di software Microsoft \\ Blocco note | fWrap            | \#0      | Blocco note     |



 

[Continua](specifying-shortcuts.md)

 

 



