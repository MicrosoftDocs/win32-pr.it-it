---
title: Compilazione di un manifesto di strumentazione
description: Dopo aver scritto il manifesto, usare il compilatore di messaggi per convalidare il manifesto e generare i file di risorse e di intestazione inclusi nel provider.
ms.assetid: ecb72942-08fc-470d-b4d6-f5f1a70de3fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9db6c02705a203c6836bf3a2c56f5049a00038
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221323"
---
# <a name="compiling-an-instrumentation-manifest"></a><span data-ttu-id="cf644-103">Compilazione di un manifesto di strumentazione</span><span class="sxs-lookup"><span data-stu-id="cf644-103">Compiling an Instrumentation Manifest</span></span>

<span data-ttu-id="cf644-104">Dopo aver [scritto il manifesto](writing-an-instrumentation-manifest.md), usare il compilatore di messaggi per convalidare il manifesto e generare i file di risorse e di intestazione inclusi nel provider.</span><span class="sxs-lookup"><span data-stu-id="cf644-104">After [writing your manifest](writing-an-instrumentation-manifest.md), use the message compiler to validate the manifest and generate the resource and header files that you include in your provider.</span></span> <span data-ttu-id="cf644-105">Per informazioni dettagliate sull'uso del compilatore, vedere [**compilatore di messaggi**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="cf644-105">For details on using the compiler, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span> <span data-ttu-id="cf644-106">Includere i file di intestazione e di risorse generati dal compilatore nel progetto che contiene il resto del codice sorgente del provider.</span><span class="sxs-lookup"><span data-stu-id="cf644-106">Include the header and resource files that the compiler generates in the project that contains the rest of your provider's source code.</span></span> <span data-ttu-id="cf644-107">Per informazioni su come scrivere gli eventi definiti nel manifesto, vedere [sviluppo di un provider](developing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cf644-107">For information on how to write the events that are defined in your manifest, see [Developing a Provider](developing-a-provider.md).</span></span>

 

 




