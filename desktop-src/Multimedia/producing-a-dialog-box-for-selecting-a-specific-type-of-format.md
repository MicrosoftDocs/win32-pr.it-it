---
title: Creazione di una finestra di dialogo per la selezione di un tipo di formato specifico
description: Creazione di una finestra di dialogo per la selezione di un tipo di formato specifico
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Gestione compressione audio,creazione di finestre di dialogo
- ACM (Audio Compression Manager), creazione di finestre di dialogo
- Esempi di ACM, creazione di finestre di dialogo
- creazione di finestre di dialogo
- Funzione acmFormatChoose
- Gestione compressione audio,selezione dei tipi di formato
- ACM (Audio Compression Manager), selezione dei tipi di formato
- Esempi di ACM, selezione dei tipi di formato
- selezione dei tipi di formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f25f7b196fcb9462a3b61dd8e351ed75276c7df7bf46cec233dd8eac7deda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037651"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>Creazione di una finestra di dialogo per la selezione di un tipo di formato specifico

È possibile che un'applicazione consenta all'utente di selezionare un formato da un elenco con restrizioni di formati in una finestra di dialogo. Le restrizioni potrebbero limitare il numero di canali, la frequenza di campionamento, il tag di formato audio-forma d'onda o il numero di bit per campione. In tutti questi casi, è possibile generare l'elenco usando la funzione [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) impostando i membri **fdwEnum** e **pwfxEnum** della [**struttura ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) Nell'esempio che segue viene illustrato questo processo.


```C++
MMRESULT            mmr; 
ACMFORMATCHOOSE     afc; 
WAVEFORMATEX        wfxSelection; 
WAVEFORMATEX        wfxEnum; 
 
// Initialize the ACMFORMATCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfx        = &wfxSelection;    // wfx to receive selection 
afc.cbwfx       = sizeof(wfxSelection); 
afc.pszTitle    = TEXT("16 Bit PCM Selection"); 
 
//  Request that all 16-bit PCM formats be displayed for the user 
//  to select from. 
memset(&wfxEnum, 0, sizeof(wfxEnum)); 
wfxEnum.wFormatTag = WAVE_FORMAT_PCM; 
wfxEnum.wBitsPerSample = 16; 
afc.fdwEnum = ACM_FORMATENUMF_WFORMATTAG | 
    ACM_FORMATENUMF_WBITSPERSAMPLE; 
afc.pwfxEnum = &wfxEnum; 
mmr = acmFormatChoose(&afc); 
if ((MMSYSERR_NOERROR != mmr) && (ACMERR_CANCELED != mmr)) 
{ 
    // There was a fatal error in bringing up the list 
    // dialog box (probably invalid input parameters). 
} 
 
```



 

 




