---
title: Recupero di una stringa che descrive un filtro
description: Recupero di una stringa che descrive un filtro
ms.assetid: 47390448-eaa6-4bea-bd90-549fa37e739a
keywords:
- Gestione compressione audio,recupero di stringhe che descrivono i filtri
- ACM (Audio Compression Manager), recupero di stringhe che descrivono i filtri
- Esempi di ACM, recupero di stringhe che descrivono i filtri
- recupero di stringhe che descrivono i filtri
- Funzione acmFilterTagDetails
- Funzione acmFilterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bf182846da280f4810c84c75a02e76baaae9082ecaf2df8ea1797fd867e8b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689131"
---
# <a name="retrieving-a-string-that-describes-a-filter"></a>Recupero di una stringa che descrive un filtro

Un'applicazione deve spesso visualizzare una stringa che descrive il formato corrente. Questa attività può essere eseguita facilmente con le [**funzioni acmFilterTagDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails) [**e acmFilterDetails.**](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails) Queste funzioni devono essere chiamate con il filtro o il tag di filtro appropriato. L'esempio seguente illustra come usare queste funzioni.


```C++
#include <mmsystem.h>
#include <mmreg.h>
#include <msacm.h>

BOOL GetFilterDescription 
( 
    LPWAVEFILTER  pwfltr, 
    LPTSTR        pszFilterTag, 
    DWORD         cchFilterTag, // Size of pszFilterTag buffer.
    LPTSTR        pszFilter,
    DWORD         cchFilter     // Size of pszFilter buffer.

) 
{ 
    MMRESULT      mmr; 
    errno_t       errno;
 
    // Retrieve the name for the filter tag of the specified filter. 
    if (NULL != pszFilterTag) { 
        ACMFILTERTAGDETAILS aftd; 
 
        // Initialize all unused members of the ACMFILTERTAGDETAILS 
        // structure to zero. 
        memset(&aftd, 0, sizeof(aftd)); 
 
        // Fill in the required members of the ACMFILTERTAGDETAILS 
        // structure for the ACM_FILTERTAGDETAILSF_FILTERTAG query. 
        aftd.cbStruct = sizeof(aftd); 
        aftd.dwFilterTag = pwfltr->dwFilterTag; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter tag. 
        mmr = acmFilterTagDetails(NULL, &aftd, 
            ACM_FILTERTAGDETAILSF_FILTERTAG); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter tag. 
            return FALSE; 
        } 
 
        // Copy the filter tag name into the calling application's 
        // buffer. 

        errno = wcscpy_s(pszFilterTag, cchFilterTag, aftd.szFilterTag); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    // Retrieve the description of the attributes for the specified 
    // filter. 
    if (NULL != pszFilter) { 
        ACMFILTERDETAILS afd; 
 
        // Initialize all unused members of the ACMFILTERDETAILS 
        // structure to zero. 
        memset(&afd, 0, sizeof(afd)); 
 
        // Fill in the required members of the ACMFILTERDETAILS 
        // structure for the ACM_FILTERDETAILSF_FILTER query. 
        afd.cbStruct    = sizeof(afd); 
        afd.dwFilterTag = pwfltr->dwFilterTag; 
        afd.pwfltr      = pwfltr; 
        afd.cbwfltr     = pwfltr->cbStruct; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter. 
        mmr = acmFilterDetails(NULL, &afd, ACM_FILTERDETAILSF_FILTER); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter. 
            return FALSE; 
        } 
 
        // Copy the description string into the caller's buffer. 
        errno = wcscpy_s(pszFilter, cchFilter, afd.szFilter); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    return TRUE; 
}
 
```



 

 




