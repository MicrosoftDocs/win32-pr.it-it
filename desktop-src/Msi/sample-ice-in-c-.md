---
description: Questo codice di esempio è da un'azione personalizzata ICE (ICE01). Verifica che il meccanismo di ghiaccio funzioni visualizzando l'ora. Il ghiaccio pubblica un messaggio che indica l'ora in cui il programma di installazione ha chiamato il ghiaccio. Questo ghiaccio non dovrebbe mai restituire un errore.
ms.assetid: 7e580f6b-8adf-4b11-9072-5b2e1506fabb
title: Esempio di ghiaccio in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91897d4d056052b27025c87f13105e2cc54657df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308324"
---
# <a name="sample-ice-in-c"></a>Esempio di ghiaccio in C++

Questo codice di esempio è da un'azione personalizzata ICE ( [ICE01](ice01.md)). Verifica che il meccanismo di ghiaccio funzioni visualizzando l'ora. Il ghiaccio pubblica un messaggio che indica l'ora in cui il programma di installazione ha chiamato il ghiaccio. Questo ghiaccio non dovrebbe mai restituire un errore.


```C++
// 
// test of external database access
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
#include <MsiQuery.h>
#pragma comment(lib, "msi.lib")

///////////////////////////////////////////////////////////
// ICE01 - simple ICE that does not test anything
UINT __stdcall ICE01(MSIHANDLE hInstall)
{
    // setup the record to describe owner and date created
    PMSIHANDLE hRecCreated = ::MsiCreateRecord(1);
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tCreated 04/29/1998 by <insert author's name here>"));

    // post the owner message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated); 
    // setup the record to describe the last time the ICE was modified
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tLast modified 05/06/1998 by <insert author's name here>"));

    // post the last modification message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated);

    // setup the record to describe what the ICE evaluates
    ::MsiRecordSetString(hRecCreated, 0, TEXT("ICE01\t3\tSimple ICE illustrating the ICE concept"));

    // post the description of evaluation message
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecCreated);
    // time value to be sent on
    TCHAR szValue[200];
    DWORD cchValue = sizeof(szValue)/sizeof(TCHAR);

    // try to get the time of this call
    if (MsiGetProperty(hInstall, TEXT("Time"), szValue, &cchValue) != ERROR_SUCCESS)
        StringCchCopy(szValue,  sizeof("(none)")/sizeof(TCHAR)+1, TEXT("none"));// no time available

    // setup the record to be sent as a message
    PMSIHANDLE hRecTime = ::MsiCreateRecord(2);
    ::MsiRecordSetString(hRecTime, 0, TEXT("ICE01\t3\tCalled at [1]."));
    ::MsiRecordSetString(hRecTime, 1, szValue);

    // send the time
    ::MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_USER), hRecTime);

    return ERROR_SUCCESS; // allows other ICEs will continue
}
```



 

 



