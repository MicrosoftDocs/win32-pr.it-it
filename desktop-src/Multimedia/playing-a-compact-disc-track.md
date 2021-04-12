---
title: Riproduzione di una traccia Compact Disc
description: Riproduzione di una traccia Compact Disc
ms.assetid: 05f68361-7fec-4c45-b434-a8b654f2d0c3
keywords:
- mciSendCommand (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8e54337dc6a47db81fad125222a33e24cca7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398857"
---
# <a name="playing-a-compact-disc-track"></a><span data-ttu-id="78aa7-104">Riproduzione di una traccia Compact Disc</span><span class="sxs-lookup"><span data-stu-id="78aa7-104">Playing a Compact Disc Track</span></span>

<span data-ttu-id="78aa7-105">Nell'esempio seguente viene aperto un dispositivo audio CD, viene riprodotta la traccia specificata dal parametro *bTrack* e il dispositivo viene chiuso al termine della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="78aa7-105">The following example opens a CD audio device, plays the track specified by the *bTrack* parameter, and closes the device after playback is complete.</span></span> <span data-ttu-id="78aa7-106">Usa la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="78aa7-106">It uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
// Plays a specified audio track using MCI_OPEN, MCI_PLAY. Returns as 
// soon as playback begins. The window procedure function for the 
// specified window will be notified when playback is complete. 
// Returns 0L on success; otherwise, returns an MCI error code.

DWORD playCDTrack(HWND hWndNotify, BYTE bTrack)
{
    UINT wDeviceID;
    DWORD dwReturn;
    MCI_OPEN_PARMS mciOpenParms;
    MCI_SET_PARMS mciSetParms;
    MCI_PLAY_PARMS mciPlayParms;

    // Open the CD audio device by specifying the device name.
    mciOpenParms.lpstrDeviceType = "cdaudio";
    if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
        MCI_OPEN_TYPE, (DWORD)(LPVOID) &mciOpenParms))
    {
        // Failed to open device. Don't close it; just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Set the time format to track/minute/second/frame (TMSF).
    mciSetParms.dwTimeFormat = MCI_FORMAT_TMSF;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_SET, 
        MCI_SET_TIME_FORMAT, (DWORD)(LPVOID) &mciSetParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    } 
    // Begin play from the specified track and play to the beginning 
    // of the next track. The window procedure function for the parent 
    // window will be notified with an MM_MCINOTIFY message when 
    // playback is complete. Unless the play command fails, the window 
    // procedure closes the device.

    mciPlayParms.dwFrom = 0L;
    mciPlayParms.dwTo = 0L;
    mciPlayParms.dwFrom = MCI_MAKE_TMSF(bTrack, 0, 0, 0);
    mciPlayParms.dwTo = MCI_MAKE_TMSF(bTrack + 1, 0, 0, 0);
    mciPlayParms.dwCallback = (DWORD) hWndNotify;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_PLAY,
        MCI_FROM | MCI_TO | MCI_NOTIFY, 
        (DWORD)(LPVOID) &mciPlayParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    return (0L);
}
```



<span data-ttu-id="78aa7-107">Per specificare una posizione relativa a una traccia in un disco Compact, è necessario usare il formato di ora Track/minute/second/frame (TMSF).</span><span class="sxs-lookup"><span data-stu-id="78aa7-107">To specify a position relative to a track on a compact disc, you must use the track/minute/second/frame (TMSF) time format.</span></span>

 

 