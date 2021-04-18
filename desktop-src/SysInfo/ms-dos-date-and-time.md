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
# <a name="ms-dos-date-and-time"></a><span data-ttu-id="09d1b-103">Data e ora di MS-DOS</span><span class="sxs-lookup"><span data-stu-id="09d1b-103">MS-DOS Date and Time</span></span>

<span data-ttu-id="09d1b-104">La **Data di MS-DOS** e l'ora di **MS-DOS** vengono compressi con valori a 16 bit che specificano il mese, il giorno, l'anno e l'ora del giorno in cui è stato scritto un file MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="09d1b-104">**MS-DOS date** and **MS-DOS time** are packed 16-bit values that specify the month, day, year, and time of day an MS-DOS file was last written to.</span></span> <span data-ttu-id="09d1b-105">MS-DOS registra la data e l'ora ogni volta che un'applicazione MS-DOS crea o scrive in un file.</span><span class="sxs-lookup"><span data-stu-id="09d1b-105">MS-DOS records the date and time whenever an MS-DOS application creates or writes to a file.</span></span> <span data-ttu-id="09d1b-106">Le applicazioni MS-DOS recuperano questa data e ora usando le funzioni MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="09d1b-106">MS-DOS applications retrieve this date and time using MS-DOS functions.</span></span> <span data-ttu-id="09d1b-107">Quando si usa la funzione [**GetFileTime ha provocato**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) per recuperare le ore dei file creati da MS-DOS, **GetFileTime ha provocato** converte automaticamente le date e gli orari di MS-DOS in orari basati su UTC.</span><span class="sxs-lookup"><span data-stu-id="09d1b-107">When you use the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the file times for files that were created by MS-DOS, **GetFileTime** automatically converts MS-DOS dates and times to UTC-based times.</span></span>

<span data-ttu-id="09d1b-108">Se si verifica una data e un'ora di MS-DOS che non sono state convertite, è possibile convertirla in un'ora basata su UTC tramite la funzione [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) .</span><span class="sxs-lookup"><span data-stu-id="09d1b-108">If you encounter an MS-DOS date and time that has not been converted, you can convert it to a UTC-based time by using the [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) function.</span></span> <span data-ttu-id="09d1b-109">Questa funzione copia la data e l'ora convertite in una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="09d1b-109">This function copies the converted date and time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="09d1b-110">È possibile convertire nuovamente il valore in una data e un'ora di MS-DOS utilizzando la funzione [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .</span><span class="sxs-lookup"><span data-stu-id="09d1b-110">You can convert the value back to an MS-DOS date and time by using the [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) function.</span></span>

 

 
