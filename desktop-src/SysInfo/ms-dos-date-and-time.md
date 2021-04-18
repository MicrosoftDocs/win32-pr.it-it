---
description: La data di MS-DOS e l'ora di MS-DOS vengono compressi con valori a 16 bit che specificano il mese, il giorno, l'anno e l'ora del giorno in cui è stato scritto un file MS-DOS.
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Data e ora di MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308099"
---
# <a name="ms-dos-date-and-time"></a>Data e ora di MS-DOS

La **Data di MS-DOS** e l'ora di **MS-DOS** vengono compressi con valori a 16 bit che specificano il mese, il giorno, l'anno e l'ora del giorno in cui è stato scritto un file MS-DOS. MS-DOS registra la data e l'ora ogni volta che un'applicazione MS-DOS crea o scrive in un file. Le applicazioni MS-DOS recuperano questa data e ora usando le funzioni MS-DOS. Quando si usa la funzione [**GetFileTime ha provocato**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) per recuperare le ore dei file creati da MS-DOS, **GetFileTime ha provocato** converte automaticamente le date e gli orari di MS-DOS in orari basati su UTC.

Se si verifica una data e un'ora di MS-DOS che non sono state convertite, è possibile convertirla in un'ora basata su UTC tramite la funzione [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) . Questa funzione copia la data e l'ora convertite in una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . È possibile convertire nuovamente il valore in una data e un'ora di MS-DOS utilizzando la funzione [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .

 

 
