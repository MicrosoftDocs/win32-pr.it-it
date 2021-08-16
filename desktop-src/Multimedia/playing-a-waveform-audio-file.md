---
title: Riproduzione di un file Waveform-Audio
description: Riproduzione di un file Waveform-Audio
ms.assetid: b28ee3e8-1633-4eb8-af1c-d1441ef752e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1581a891f07a69641338f203fb56ce57f9b3717d6cd52800b907798fce43795d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372653"
---
# <a name="playing-a-waveform-audio-file"></a>Riproduzione di un file Waveform-Audio

L'esempio seguente apre un dispositivo audio waveform e riproduce il file audio waveform specificato dal parametro *lpszWAVEFileName* usando la [**funzione mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
// Plays a specified waveform-audio file using MCI_OPEN and MCI_PLAY. 
// Returns when playback begins. Returns 0L on success, otherwise 
// returns an MCI error code.

DWORD playWAVEFile(HWND hWndNotify, LPSTR lpszWAVEFileName)
{
    UINT wDeviceID;
    DWORD dwReturn;
    MCI_OPEN_PARMS mciOpenParms;
    MCI_PLAY_PARMS mciPlayParms;

    // Open the device by specifying the device and filename.
    // MCI will choose a device capable of playing the specified file.

    mciOpenParms.lpstrDeviceType = "waveaudio";
    mciOpenParms.lpstrElementName = lpszWAVEFileName;
    if (dwReturn = mciSendCommand(0, MCI_OPEN,
       MCI_OPEN_TYPE | MCI_OPEN_ELEMENT, 
       (DWORD)(LPVOID) &mciOpenParms))
    {
        // Failed to open device. Don't close it; just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Begin playback. The window procedure function for the parent 
    // window will be notified with an MM_MCINOTIFY message when 
    // playback is complete. At this time, the window procedure closes 
    // the device.

    mciPlayParms.dwCallback = (DWORD) hWndNotify;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_PLAY, MCI_NOTIFY, 
        (DWORD)(LPVOID) &mciPlayParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    return (0L);
}
```



 

 