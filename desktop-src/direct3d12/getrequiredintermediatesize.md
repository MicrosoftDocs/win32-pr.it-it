---
title: Funzione GetRequiredIntermediateSize (D3dx12.h)
description: Restituisce le dimensioni richieste di un buffer da utilizzare per il caricamento dei dati.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- Funzione GetRequiredIntermediateSize
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f6fe927d49bb50d6bdea2889d946c5d9c60b1b703299c2717b881afe1aa7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124179"
---
# <a name="getrequiredintermediatesize-function"></a>Funzione GetRequiredIntermediateSize

Restituisce le dimensioni richieste di un buffer da utilizzare per il caricamento dei dati.

## <a name="syntax"></a>Sintassi


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDestinationResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Puntatore [**all'interfaccia ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa di destinazione.

</dd> <dt>

*FirstSubresource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice della prima sottorisorsa nella risorsa. L'intervallo di valori validi è compreso tra 0 e D3D12 \_ REQ \_ SUBRESOURCES.

</dd> <dt>

*NumSubresources* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di sottorisorse nella risorsa. L'intervallo di valori validi è compreso tra 0 e (D3D12 \_ REQ \_ SUBRESOURCES - *FirstSubresource).*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Dimensioni del buffer, in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

