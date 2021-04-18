---
title: ID3D12Resource metodo getdesc
description: Ottiene la descrizione della risorsa.
ms.assetid: B8D84D69-6B13-4E86-8EF6-A841354B1E5C
keywords:
- Metodo getdesc
- Metodo getdesc, interfaccia ID3D12Resource
- Interfaccia ID3D12Resource, metodo getdesc
topic_type:
- apiref
api_name:
- ID3D12Resource.GetDesc
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
api_location:
- d3d12.h
ms.openlocfilehash: 5be3f6f825370c467388805c84096240441d09a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299157"
---
# <a name="id3d12resourcegetdesc-method"></a>Metodo ID3D12Resource:: getdesc

Ottiene la descrizione della risorsa.

## <a name="syntax"></a>Sintassi


```C++
D3D12_RESOURCE_DESC GetDesc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **D3D12 \_ Resource \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)**

Struttura di descrizione della risorsa Direct3D 12.

## <a name="examples"></a>Esempio

Restituisce le dimensioni richieste di un buffer da usare per il caricamento dei dati.


```C++
// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}
```



Vedere il [codice di esempio nella Guida di riferimento a D3D12](notes-on-example-code.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)
</dt> </dl>

 

 




