---
description: Creare una risorsa di trama da un file.
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: Funzione D3DX10CreateTextureFromFile (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322938"
---
# <a name="d3dx10createtexturefromfile-function"></a>D3DX10CreateTextureFromFile (funzione)

Creare una risorsa di trama da un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà la risorsa.

</dd> <dt>

*pSrcFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome del file che contiene la risorsa. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR. Per un elenco dei formati di file di immagine supportati, vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md) Enumeration.

</dd> <dt>

*pLoadInfo* \[ in\]
</dt> <dd>

Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***

facoltativo. Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.

</dd> <dt>

*pPump* \[ in\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)). Se viene specificato **null** , questa funzione verrà comportata in modo sincrono e non verrà restituita finché non viene completata.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***

Indirizzo di un puntatore alla risorsa di trama (vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).

</dd> <dt>

*pHResult* \[ out\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **null**. Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Per un elenco dei formati di immagine supportati, vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
