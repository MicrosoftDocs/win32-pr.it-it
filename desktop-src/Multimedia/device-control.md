---
title: Controllo del dispositivo (Windows Multimedia)
description: Controllo dei dispositivi
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047741"
---
# <a name="device-control-windows-multimedia"></a><span data-ttu-id="11ac7-103">Controllo del dispositivo (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="11ac7-103">Device Control (Windows Multimedia)</span></span>

<span data-ttu-id="11ac7-104">Per controllare un dispositivo MCI, aprire il dispositivo, inviare i comandi necessari e quindi chiudere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="11ac7-104">To control an MCI device, you open the device, send the necessary commands to it, and then close the device.</span></span> <span data-ttu-id="11ac7-105">I comandi possono essere molto simili, anche per i dispositivi MCI completamente diversi.</span><span class="sxs-lookup"><span data-stu-id="11ac7-105">The commands can be very similar, even for completely different MCI devices.</span></span> <span data-ttu-id="11ac7-106">Ad esempio, la serie seguente di comandi MCI riproduce la sesta traccia di un CD audio usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="11ac7-106">For example, the following series of MCI commands plays the sixth track of an audio CD by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="11ac7-107">Nell'esempio riportato di seguito viene illustrata una serie simile di comandi MCI che riproduce i primi 10.000 esempi di un file Waveform-Audio:</span><span class="sxs-lookup"><span data-stu-id="11ac7-107">The next example shows a similar series of MCI commands that plays the first 10,000 samples of a waveform-audio file:</span></span>


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="11ac7-108">Questi esempi illustrano alcuni aspetti interessanti sui comandi MCI:</span><span class="sxs-lookup"><span data-stu-id="11ac7-108">These examples illustrate some interesting facts about MCI commands:</span></span>

-   <span data-ttu-id="11ac7-109">Gli stessi comandi di base ([**apertura**](open.md), [**impostazione**](set.md), [**riproduzione**](play.md)e [**chiusura**](close.md)) vengono usati con i dispositivi audio CD e Waveform-Audio.</span><span class="sxs-lookup"><span data-stu-id="11ac7-109">The same basic commands ([**open**](open.md), [**set**](set.md), [**play**](play.md), and [**close**](close.md)) are used with CD audio and waveform-audio devices.</span></span> <span data-ttu-id="11ac7-110">Gli stessi comandi MCI vengono usati con tutti i dispositivi MCI.</span><span class="sxs-lookup"><span data-stu-id="11ac7-110">The same MCI commands are used with all MCI devices.</span></span>
-   <span data-ttu-id="11ac7-111">Il comando Apri per il dispositivo Waveform-Audio include una specifica del nome file.</span><span class="sxs-lookup"><span data-stu-id="11ac7-111">The open command for the waveform-audio device includes a filename specification.</span></span> <span data-ttu-id="11ac7-112">Il dispositivo Waveform-Audio è un *dispositivo composto* (uno associato a un file di dati), mentre il dispositivo audio CD è un *dispositivo semplice* (uno senza un file di dati associato).</span><span class="sxs-lookup"><span data-stu-id="11ac7-112">The waveform-audio device is a *compound device* (one associated with a data file), while the CD audio device is a *simple device* (one without an associated data file).</span></span>
-   <span data-ttu-id="11ac7-113">Il comando set specifica i formati di ora in ogni caso, ma il flag di formato time per il dispositivo audio CD specifica il formato Tracks/minutes/seconds/frames (TMSF), mentre il formato dell'ora usato con il dispositivo Waveform-Audio specifica "Samples".</span><span class="sxs-lookup"><span data-stu-id="11ac7-113">The set command specifies time formats in each case, but the time-format flag for the CD audio device specifies tracks/minutes/seconds/frames (TMSF) format, while the time format used with the waveform-audio device specifies "samples".</span></span>
-   <span data-ttu-id="11ac7-114">Le variabili utilizzate con i flag "from" e "to" sono appropriate per il rispettivo formato di ora.</span><span class="sxs-lookup"><span data-stu-id="11ac7-114">The variables used with the "from" and "to" flags are appropriate to the respective time format.</span></span> <span data-ttu-id="11ac7-115">Per il dispositivo audio CD, ad esempio, le variabili specificano un intervallo di tracce, ma per il dispositivo Waveform-Audio le variabili specificano un intervallo di campioni.</span><span class="sxs-lookup"><span data-stu-id="11ac7-115">For example, for the CD audio device, the variables specify a range of tracks, but for the waveform-audio device, the variables specify a range of samples.</span></span>

 

 
