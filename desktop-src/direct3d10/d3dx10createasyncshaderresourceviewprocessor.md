---
description: Creare un elaboratore di dati che caricherà una risorsa e quindi crei una visualizzazione delle risorse shader. I processori di dati sono un componente della funzionalità asincrona di caricamento dei dati in D3DX10 che usa le pompe di thread.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: Funzione D3DX10CreateAsyncShaderResourceViewProcessor (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323315"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a>D3DX10CreateAsyncShaderResourceViewProcessor (funzione)

Creare un elaboratore di dati che caricherà una risorsa e quindi crei una visualizzazione delle risorse shader. I processori di dati sono un componente della funzionalità asincrona di caricamento dei dati in D3DX10 che usa le [**pompe di thread**](id3dx10threadpump.md).

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore al dispositivo Direct3D (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che verrà usato per creare una risorsa e una visualizzazione delle risorse dello shader per la risorsa.

</dd> <dt>

*pLoadInfo* \[ in\]
</dt> <dd>

Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




