---
description: Con Network Monitor, la selezione di una scheda di interfaccia di rete a livello di codice è un processo in due passaggi. Per prima cosa, creare il BLOB di filtro chiamando il metodo CreateBlob. Selezionare quindi la scheda di interfaccia di rete chiamando il metodo GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Selezione di una scheda di interfaccia di rete con GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307822"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a><span data-ttu-id="c4793-105">Selezione di una scheda di interfaccia di rete con GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="c4793-105">Selecting a NIC Using GetNPPBlobFromUI</span></span>

<span data-ttu-id="c4793-106">Con Network Monitor, la selezione di una scheda di interfaccia di rete a livello di codice è un processo in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="c4793-106">With Network Monitor, selecting a NIC programmatically is a two-step process.</span></span> <span data-ttu-id="c4793-107">Per prima cosa, creare il BLOB di filtro chiamando il metodo [**CreateBlob**](createblob.md) .</span><span class="sxs-lookup"><span data-stu-id="c4793-107">First, create the filter BLOB by calling the [**CreateBlob**](createblob.md) method.</span></span> <span data-ttu-id="c4793-108">Selezionare quindi la scheda di interfaccia di rete chiamando il metodo [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="c4793-108">Then, select the NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) method.</span></span>

<span data-ttu-id="c4793-109">In questo esempio viene usato un BLOB di filtro per selezionare la scheda di interfaccia di rete necessaria:</span><span class="sxs-lookup"><span data-stu-id="c4793-109">In this example a filter BLOB is used to select the required NIC:</span></span>


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



