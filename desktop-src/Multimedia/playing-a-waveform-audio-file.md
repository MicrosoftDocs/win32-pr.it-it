---
title: Riproduzione di un file di Waveform-Audio
description: Riproduzione di un file di Waveform-Audio
ms.assetid: b28ee3e8-1633-4eb8-af1c-d1441ef752e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6cd1bf32de7ae9002dc3691d342af360f29455
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398856"
---
# <a name="playing-a-waveform-audio-file"></a><span data-ttu-id="671a8-103">Riproduzione di un file di Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="671a8-103">Playing a Waveform-Audio File</span></span>

<span data-ttu-id="671a8-104">Nell'esempio seguente viene aperto un dispositivo Waveform-Audio e viene riprodotto il file Waveform-Audio specificato dal parametro *lpszWAVEFileName* usando la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="671a8-104">The following example opens a waveform-audio device and plays the waveform-audio file specified by the *lpszWAVEFileName* parameter using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


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



 

 