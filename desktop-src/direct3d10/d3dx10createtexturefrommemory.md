---
description: Creare una risorsa trama da un file che risiede nella memoria di sistema.
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: Funzione D3DX10CreateTextureFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7b64c3c429ef356fa4ab8c206682c3b1711a14fe29ee6b2024b92b8113951062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753351"
---
# <a name="d3dx10createtexturefrommemory-function"></a>Funzione D3DX10CreateTextureFromMemory

Creare una risorsa trama da un file che risiede nella memoria di sistema.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore al dispositivo (vedere [**ID3D10 InterfaceDevice)**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)che userà la risorsa.

</dd> <dt>

*pSrcData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore alla risorsa nella memoria di sistema.

</dd> <dt>

*SrcDataSize* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**

Dimensioni della risorsa nella memoria di sistema.

</dd> <dt>

*pLoadInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) quando viene creato il processore di dati. Impostare questo valore su **NULL** per leggere le caratteristiche di una trama quando viene caricata la trama.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntatore a un'interfaccia thread pump (vedere [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)). Se si specifica **NULL,** questa funzione si comporterà in modo sincrono e non restituirà finché non viene completata.

</dd> <dt>

*ppTexture* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***

Indirizzo di un puntatore alla risorsa creata. Vedere [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere un percorso di memoria valido fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Per un elenco dei formati di immagine supportati, vedere [**D3DX10 \_ IMAGE \_ FILE \_ FORMAT**](d3dx10-image-file-format.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
