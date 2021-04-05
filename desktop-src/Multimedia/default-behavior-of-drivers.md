---
title: Comportamento predefinito dei driver
description: Comportamento predefinito dei driver
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726562"
---
# <a name="default-behavior-of-drivers"></a><span data-ttu-id="4c0ea-103">Comportamento predefinito dei driver</span><span class="sxs-lookup"><span data-stu-id="4c0ea-103">Default Behavior of Drivers</span></span>

<span data-ttu-id="4c0ea-104">In molte situazioni, le specifiche del comando MCI definiscono i valori predefiniti e il comportamento per i driver di un particolare tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-104">In many situations, the MCI command specifications define the default values and behavior for drivers of a particular device type.</span></span> <span data-ttu-id="4c0ea-105">Poiché i dispositivi multimediali possono avere un'ampia gamma di funzionalità e limitazioni, è possibile che si verifichino aree di comportamento indefinite.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-105">Since multimedia devices can have a wide range of features (and limitations), there can be undefined areas of behavior.</span></span> <span data-ttu-id="4c0ea-106">Inoltre, i driver possono gestire le eccezioni in modo diverso, in base alle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-106">Also, drivers might handle exceptions differently, based on the capabilities of the device.</span></span>

<span data-ttu-id="4c0ea-107">Si considerino, ad esempio, i comandi seguenti inviati a un driver audio Waveform usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="4c0ea-107">For example, consider the following commands sent to a waveform-audio driver using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="4c0ea-108">Il comando [**record**](record.md) restituisce un valore "Parameter out-of-range" e interrompe la riproduzione avviata dal comando [**Play**](play.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-108">The [**record**](record.md) command returns a "Parameter out of range" value and stops the playback started by the previous [**play**](play.md) command.</span></span> <span data-ttu-id="4c0ea-109">Si può prevedere che il driver convalidi il comando record prima di arrestare la riproduzione, ma il driver interrompe prima la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="4c0ea-109">One might expect the driver to validate the record command before stopping playback, but the driver stops the playback first.</span></span>

 

 