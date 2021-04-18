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
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Selezione di una scheda di interfaccia di rete con GetNPPBlobFromUI

Con Network Monitor, la selezione di una scheda di interfaccia di rete a livello di codice è un processo in due passaggi. Per prima cosa, creare il BLOB di filtro chiamando il metodo [**CreateBlob**](createblob.md) . Selezionare quindi la scheda di interfaccia di rete chiamando il metodo [**GetNPPBlobFromUI**](getnppblobfromui.md) .

In questo esempio viene usato un BLOB di filtro per selezionare la scheda di interfaccia di rete necessaria:


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



 

 



