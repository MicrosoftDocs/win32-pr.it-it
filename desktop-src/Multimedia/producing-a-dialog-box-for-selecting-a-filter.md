---
title: Creazione di una finestra di dialogo per la selezione di un filtro
description: Creazione di una finestra di dialogo per la selezione di un filtro
ms.assetid: 4cbb9276-6ce6-4cf4-a000-2b4f9ac42b31
keywords:
- Gestione compressione audio,creazione di finestre di dialogo
- ACM (Audio Compression Manager), creazione di finestre di dialogo
- Esempi di ACM, creazione di finestre di dialogo
- creazione di finestre di dialogo
- Funzione acmFilterChoose
- gestione compressione audio(ACM), selezione dei filtri
- ACM (Audio Compression Manager), selezione dei filtri
- Esempi di ACM, selezione di filtri
- selezione di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70015f7e546337983725ae85c683acf5e9b75423e0de0734de4e1293480933ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136605"
---
# <a name="producing-a-dialog-box-for-selecting-a-filter"></a>Creazione di una finestra di dialogo per la selezione di un filtro

Un'applicazione può consentire agli utenti di selezionare un'operazione di filtro arbitraria e applicarla ai dati audio waveform. Nell'esempio seguente l'applicazione alloca un buffer per contenere il filtro e quindi usa la [**funzione acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) per selezionare il filtro. Le funzioni in questo esempio devono essere chiamate con il filtro o il tag di filtro appropriato.


```C++
MMRESULT        mmr; 
ACMFILTERCHOOSE afc; 
PWAVEFILTER     pwfltr; 
DWORD           cbwfltr; 
 
// Determine the maximum size required for any valid filter 
// for which the ACM has a driver installed and enabled. 
mmr = acmMetrics(NULL, ACM_METRIC_MAX_SIZE_FILTER, &cbwfltr); 
if (MMSYSERR_NOERROR != mmr) { 
 
    // The ACM probably has no drivers installed and 
    // enabled for filter operations. 
    return (mmr); 
} 
 
// Dynamically allocate a structure large enough to hold the 
// maximum sized filter enabled in the system. 
pwfltr = (PWAVEFILTER)LocalAlloc(LPTR, (UINT)cbwfltr); 
if (NULL == pwfltr) { 
    return (MMSYSERR_NOMEM); 
} 
 
// Initialize the ACMFILTERCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfltr      = pwfltr;           // wfltr to receive selection 
afc.cbwfltr     = cbwfltr;          // size of wfltr buffer 
afc.pszTitle    = TEXT("Any Filter Selection"); 
 
// Call the ACM to bring up the filter-selection dialog box. 
mmr = acmFilterChoose(&afc); 
if (MMSYSERR_NOERROR == mmr) { 
    // The user selected a valid filter. The pwfltr buffer, 
    // allocated above, contains the complete filter description. 
} 
 
// Clean up and exit. 
LocalFree((HLOCAL)pwfltr); 
return (mmr); 
 
```



 

 




