---
title: Variabili per gestire il buffer di ritardo
description: Variabili per gestire il buffer di ritardo
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Plug-in di Windows Media Player, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione dei segnali digitali, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
- Esempio di plug-in Echo DSP, buffer di ritardo
- buffer ritardato
- buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221596"
---
# <a name="variables-to-manage-the-delay-buffer"></a><span data-ttu-id="92a04-111">Variabili per gestire il buffer di ritardo</span><span class="sxs-lookup"><span data-stu-id="92a04-111">Variables to Manage the Delay Buffer</span></span>

<span data-ttu-id="92a04-112">È necessario aggiungere le dichiarazioni per le variabili membro necessarie per gestire il buffer di ritardo.</span><span class="sxs-lookup"><span data-stu-id="92a04-112">You must add the declarations for the member variables you need to manage the delay buffer.</span></span> <span data-ttu-id="92a04-113">Aggiungere le seguenti dichiarazioni a Echo. h nella sezione "private":</span><span class="sxs-lookup"><span data-stu-id="92a04-113">Add the following declarations to Echo.h in the "private" section:</span></span>


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



<span data-ttu-id="92a04-114">Aggiungere il codice seguente al costruttore CEcho per inizializzare le variabili del buffer di ritardo:</span><span class="sxs-lookup"><span data-stu-id="92a04-114">Add the following code to the CEcho constructor to initialize the delay buffer variables:</span></span>


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a><span data-ttu-id="92a04-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="92a04-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92a04-116">**Uso delle risorse di streaming**</span><span class="sxs-lookup"><span data-stu-id="92a04-116">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




