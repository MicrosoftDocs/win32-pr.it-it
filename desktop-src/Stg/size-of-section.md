---
title: Dimensione della sezione
description: Il tipo di dati della sezione dimensione indica le dimensioni, in byte, della sezione.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221999"
---
# <a name="size-of-section"></a><span data-ttu-id="55c65-103">Dimensione della sezione</span><span class="sxs-lookup"><span data-stu-id="55c65-103">Size of Section</span></span>

<span data-ttu-id="55c65-104">Il tipo di dati della sezione dimensione indica le dimensioni, in byte, della sezione.</span><span class="sxs-lookup"><span data-stu-id="55c65-104">The section size data type indicates the size, in bytes, of the section.</span></span> <span data-ttu-id="55c65-105">Poiché le dimensioni della sezione sono i primi 4 byte, le sezioni possono essere copiate come una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="55c65-105">Because the section size is the first 4 bytes, sections can be copied as an array of bytes.</span></span> <span data-ttu-id="55c65-106">Le dimensioni della sezione devono essere sempre un multiplo di quattro.</span><span class="sxs-lookup"><span data-stu-id="55c65-106">The section size should always be a multiple of four.</span></span>

<span data-ttu-id="55c65-107">Ad esempio, una sezione vuota, ovvero una con zero proprietà, avrà un numero di byte pari a otto (il conteggio dei byte **DWORD** e il numero **DWORD** di proprietà).</span><span class="sxs-lookup"><span data-stu-id="55c65-107">For example, an empty section, that is, one with zero properties in it, would have a byte count of eight (the **DWORD** byte count and the **DWORD** count of properties).</span></span> <span data-ttu-id="55c65-108">La sezione stessa conterrebbe gli 8 byte: **08 00 00 00 00 00 00 00**.</span><span class="sxs-lookup"><span data-stu-id="55c65-108">The section itself would contain the 8 bytes: **08 00 00 00 00 00 00 00**.</span></span>

 

 




