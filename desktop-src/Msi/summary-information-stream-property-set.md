---
description: Nella tabella seguente viene illustrato il set di proprietà del flusso di informazioni di riepilogo, che include le proprietà, gli ID delle proprietà, i PIN e i tipi corrispondenti.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Set di proprietà del flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d41439e15a59ca1942fcbb49c06067251060935b165d6a34972df868fa7feac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627051"
---
# <a name="summary-information-stream-property-set"></a>Set di proprietà del flusso di informazioni di riepilogo

Nella tabella seguente viene illustrato il set di proprietà del flusso di informazioni di riepilogo, che include le proprietà, gli ID delle proprietà, i PIN e i tipi corrispondenti. Per altre informazioni sull'uso di queste proprietà da parte del programma di installazione, vedere [Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md). Per informazioni sulle funzioni di Windows Installer usate per configurare le proprietà delle informazioni di riepilogo, vedere [Uso del flusso di informazioni di riepilogo](using-the-summary-information-stream.md).



| Nome proprietà                                                | ID proprietà        | PID | Tipo         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**Codepage**](codepage-summary.md)                         | TABELLA CODICI \_ PID      | 1   | VT \_ I2       |
| [**Titolo**](title-summary.md)                               | TITOLO DEL \_ PID         | 2   | VT \_ LPSTR    |
| [**Oggetto**](subject-summary.md)                           | SOGGETTO \_ PID       | 3   | VT \_ LPSTR    |
| [**Autore**](author-summary.md)                             | PID \_ AUTHOR        | 4   | VT \_ LPSTR    |
| [**Parole chiavi**](keywords-summary.md)                         | PAROLE \_ CHIAVE PID      | 5   | VT \_ LPSTR    |
| [**Commenti**](comments-summary.md)                         | COMMENTI \_ PID      | 6   | VT \_ LPSTR    |
| [**Modello**](template-summary.md)                         | MODELLO \_ PID      | 7   | VT \_ LPSTR    |
| [**Autore ultimo salvataggio**](last-saved-by-summary.md)               | PID \_ LASTAUTHOR    | 8   | VT \_ LPSTR    |
| [**Numero di revisione**](revision-number-summary.md)           | PID \_ REVNUMBER     | 9   | VT \_ LPSTR    |
| [**Ultima stampa**](last-printed-summary.md)                 | PID \_ LASTPRINTED   | 11  | VT \_ FILETIME |
| [**Crea ora/data**](create-time-date-summary.md)         | PID \_ CREATE \_ DTM   | 12  | VT \_ FILETIME |
| [**Data/ora ultimo salvataggio**](last-saved-time-date-summary.md)  | PID \_ LASTSAVE \_ DTM | 13  | VT \_ FILETIME |
| [**Conteggio pagine**](page-count-summary.md)                     | PID \_ PAGECOUNT     | 14  | VT \_ I4       |
| [**Conteggio parole**](word-count-summary.md)                     | PID \_ WORDCOUNT     | 15  | VT \_ I4       |
| [**Conteggio caratteri**](character-count-summary.md)           | PID \_ CHARCOUNT     | 16  | VT \_ I4       |
| [**Creazione di un'applicazione**](creating-application-summary.md) | PID \_ APPNAME       | 18  | VT \_ LPSTR    |
| [**Sicurezza**](security-summary.md)                         | SICUREZZA \_ PID      | 19  | VT \_ I4       |



 

Il programma di installazione attualmente gestisce tre formati di archiviazione per i pacchetti di installazione, le trasformazioni e i pacchetti di patch. Il CLSID per l'archiviazione viene impostato sulla classe di formato appropriata per il formato specifico, indipendentemente dalle informazioni di riepilogo per l'archiviazione.

 

 



