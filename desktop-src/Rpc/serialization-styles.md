---
title: Stili di serializzazione
description: Sono disponibili tre stili che è possibile usare per modificare gli handle di serializzazione.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396398"
---
# <a name="serialization-styles"></a><span data-ttu-id="289cd-103">Stili di serializzazione</span><span class="sxs-lookup"><span data-stu-id="289cd-103">Serialization Styles</span></span>

<span data-ttu-id="289cd-104">Sono disponibili tre stili che è possibile usare per modificare gli handle di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="289cd-104">There are three styles you can use to manipulate serialization handles.</span></span> <span data-ttu-id="289cd-105">Si tratta di:</span><span class="sxs-lookup"><span data-stu-id="289cd-105">These are:</span></span>

-   [<span data-ttu-id="289cd-106">Serializzazione del buffer fissa</span><span class="sxs-lookup"><span data-stu-id="289cd-106">Fixed Buffer Serialization</span></span>](fixed-buffer-serialization.md)
-   [<span data-ttu-id="289cd-107">Serializzazione dinamica del buffer</span><span class="sxs-lookup"><span data-stu-id="289cd-107">Dynamic Buffer Serialization</span></span>](dynamic-buffer-serialization.md)
-   [<span data-ttu-id="289cd-108">Serializzazione incrementale</span><span class="sxs-lookup"><span data-stu-id="289cd-108">Incremental Serialization</span></span>](incremental-serialization.md)

<span data-ttu-id="289cd-109">Indipendentemente dallo stile usato, è necessario creare un handle di serializzazione, serializzare i dati e quindi liberare l'handle.</span><span class="sxs-lookup"><span data-stu-id="289cd-109">Regardless of the style you use, you must create a serialization handle, serialize the data, and then free the handle.</span></span> <span data-ttu-id="289cd-110">Lo stile viene impostato quando il programma crea l'handle e definisce la modalità di manipolazione di un buffer.</span><span class="sxs-lookup"><span data-stu-id="289cd-110">The style is set when your program creates the handle and defines the way a buffer is manipulated.</span></span> <span data-ttu-id="289cd-111">L'handle gestisce il contesto appropriato associato a ognuno dei tre stili di serializzazione.</span><span class="sxs-lookup"><span data-stu-id="289cd-111">The handle maintains the appropriate context associated with each of the three serialization styles.</span></span>

 

 




