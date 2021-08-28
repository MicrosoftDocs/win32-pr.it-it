---
description: Con Network Monitor, la selezione di una scheda di interfaccia di rete a livello di codice è un processo in due passaggi. Creare prima di tutto il BLOB del filtro chiamando il metodo CreateBlob. Selezionare quindi la scheda di interfaccia di rete chiamando il metodo GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Selezione di una scheda di interfaccia di rete tramite GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3bd02ef5085bba511fb0d05844840eb92d85ef83c67f244ab321570fae4ad8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128901"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Selezione di una scheda di interfaccia di rete tramite GetNPPBlobFromUI

Con Network Monitor, la selezione di una scheda di interfaccia di rete a livello di codice è un processo in due passaggi. Creare prima di tutto il BLOB del filtro chiamando [**il metodo CreateBlob.**](createblob.md) Selezionare quindi la scheda di interfaccia di rete chiamando [**il metodo GetNPPBlobFromUI.**](getnppblobfromui.md)

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



 

 



