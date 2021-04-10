---
title: Per disabilitare l'indicizzazione automatica
description: Per disabilitare l'indicizzazione automatica
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Media Format SDK, disabilitazione dell'indicizzazione automatica
- Windows Media Format SDK, indicizzazione automatica
- Formato Advanced Systems (ASF), disabilitazione dell'indicizzazione automatica
- ASF (Advanced Systems Format), disabilitazione dell'indicizzazione automatica
- ASF (Advanced Systems Format), indicizzazione automatica
- ASF (formato avanzato dei sistemi), indicizzazione automatica
- indici, disabilitazione dell'indicizzazione automatica
- indici, indicizzazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0235ddac8093d9b1c6d40fde341ee32d078b84b7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956197"
---
# <a name="to-disable-automatic-indexing"></a>Per disabilitare l'indicizzazione automatica

Quando si scrive un file ASF, è possibile che non si desideri sempre generare un indice per impostazione predefinita. È possibile disabilitare l'indicizzazione automatica usando il metodo [**IWMWriterFileSink3:: SetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing) .

Nell'esempio di codice seguente viene illustrato come disabilitare l'indicizzazione automatica da parte del writer.


```C++
IWMWriterFileSink*  pBaseFileSink = NULL;
IWMWriterFileSink3* pMySink       = NULL;

BOOL    fAutoIndex;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer file sink.
hr = WMCreateWriterFileSink(&pBaseFileSink);

// Retrieve an IWMWriterFileSink3 interface pointer for the new sink.
hr = pBaseFileSink->QueryInterface(IID_IWMWriterFileSink3,
                                    (void**)&pMySink);

// Release the base file sink.
pBaseFileSink->Release();
pBaseFileSink = NULL;

// Check the state of automatic indexing.
hr = pMySink->GetAutoIndexing(&fAutoIndex);

// If auto indexing is enabled, turn it off.
if(fAutoIndex)
   pMySink->SetAutoIndexing(FALSE);

// You can now write to this sink and the file will not have an index.

// Release the remaining interface.
pMySink->Release();
pMySink = NULL;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMWriterFileSink3::GetAutoIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




