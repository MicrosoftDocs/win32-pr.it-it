---
title: Per disabilitare l'indicizzazione automatica
description: Per disabilitare l'indicizzazione automatica
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Media Format SDK, disabilitazione dell'indicizzazione automatica
- Windows Media Format SDK, indicizzazione automatica
- Advanced Systems Format (ASF), disabilitazione dell'indicizzazione automatica
- ASF (Advanced Systems Format), disabilitazione dell'indicizzazione automatica
- Advanced Systems Format (ASF), indicizzazione automatica
- ASF (Advanced Systems Format), indicizzazione automatica
- indici, disabilitazione dell'indicizzazione automatica
- indici, indicizzazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3b63d58b8f9a0fbbdff88369832b67abca7d9f11a39c56613c6e5d867d6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699911"
---
# <a name="to-disable-automatic-indexing"></a>Per disabilitare l'indicizzazione automatica

È possibile che non sempre venga generato un indice per impostazione predefinita quando si scrive un file ASF. È possibile disabilitare l'indicizzazione automatica usando il [**metodo IWMWriterFileSink3::SetAutoIndexing.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing)

Il codice di esempio seguente illustra come disabilitare l'indicizzazione automatica dal writer.


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

 

 




