---
description: La tabella seguente illustra il set di proprietà del flusso di informazioni di riepilogo, che include le proprietà, gli ID di proprietà, i PID e i tipi corrispondenti.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Set di proprietà del flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3929e4180a85a8f154c0a0352ddd1f9a052769ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319953"
---
# <a name="summary-information-stream-property-set"></a>Set di proprietà del flusso di informazioni di riepilogo

La tabella seguente illustra il set di proprietà del flusso di informazioni di riepilogo, che include le proprietà, gli ID di proprietà, i PID e i tipi corrispondenti. Per ulteriori informazioni sull'utilizzo di queste proprietà da parte del programma di installazione, vedere [descrizioni delle proprietà di riepilogo](summary-property-descriptions.md). Per informazioni sulle funzioni di Windows Installer utilizzate per configurare le proprietà delle informazioni di riepilogo, vedere [utilizzo del flusso di informazioni di riepilogo](using-the-summary-information-stream.md).



| Nome proprietà                                                | ID proprietà        | PID | Tipo         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**CodePage**](codepage-summary.md)                         | tabella \_ codici PID      | 1   | \_I2 VT       |
| [**Titolo**](title-summary.md)                               | \_titolo PID         | 2   | \_LPSTR VT    |
| [**Oggetto**](subject-summary.md)                           | \_oggetto PID       | 3   | \_LPSTR VT    |
| [**Autore**](author-summary.md)                             | \_autore PID        | 4   | \_LPSTR VT    |
| [**Parole chiave**](keywords-summary.md)                         | \_parole chiave PID      | 5   | \_LPSTR VT    |
| [**Commenti**](comments-summary.md)                         | \_Commenti PID      | 6   | \_LPSTR VT    |
| [**Modello**](template-summary.md)                         | \_modello PID      | 7   | \_LPSTR VT    |
| [**Autore ultimo salvataggio**](last-saved-by-summary.md)               | \_LASTAUTHOR PID    | 8   | \_LPSTR VT    |
| [**Numero revisione**](revision-number-summary.md)           | \_REVNUMBER PID     | 9   | \_LPSTR VT    |
| [**Ultima stampa**](last-printed-summary.md)                 | \_LASTPRINTED PID   | 11  | FILETIME VT \_ |
| [**Data/ora creazione**](create-time-date-summary.md)         | PID \_ creare il \_ DTM   | 12  | FILETIME VT \_ |
| [**Data/ora ultimo salvataggio**](last-saved-time-date-summary.md)  | PID \_ LASTSAVE \_ DTM | 13  | FILETIME VT \_ |
| [**Conteggio pagine**](page-count-summary.md)                     | \_PageCount PID     | 14  | VT \_ I4       |
| [**Conteggio parole**](word-count-summary.md)                     | \_WORDCOUNT PID     | 15  | VT \_ I4       |
| [**Numero di caratteri**](character-count-summary.md)           | \_charCount PID     | 16  | VT \_ I4       |
| [**Creazione dell'applicazione**](creating-application-summary.md) | \_appname PID       | 18  | \_LPSTR VT    |
| [**Sicurezza**](security-summary.md)                         | \_sicurezza PID      | 19  | VT \_ I4       |



 

Il programma di installazione gestisce attualmente tre formati di archiviazione per pacchetti di installazione, trasformazioni e pacchetti di patch. Il CLSID per l'archiviazione è impostato sulla classe di formato appropriata per il formato specifico, indipendentemente dalle informazioni di riepilogo per l'archiviazione.

 

 



