---
description: 'Funzione D3DX10GetImageInfoFromResource: recupera informazioni su una determinata immagine in una risorsa.'
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: Funzione D3DX10GetImageInfoFromResource (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af4dea966b63549c4bcef913175c6c97e1c49d73e3d5694cfcd0f7b6c8170497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989161"
---
# <a name="d3dx10getimageinfofromresource-function"></a>Funzione D3DX10GetImageInfoFromResource

Recupera informazioni su una determinata immagine in una risorsa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSrcModule* \[ Pollici\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Modulo in cui viene caricata la risorsa. Impostare questo parametro su **NULL** per specificare il modulo associato all'immagine usata dal sistema operativo per creare il processo corrente.

</dd> <dt>

*pSrcResource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Pump di thread facoltativo che può essere usato per caricare le informazioni in modo asincrono. Può essere **NULL.** Vedere [**ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> <dt>

*pSrcInfo* \[ Pollici\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***

Puntatore a una struttura D3DX10 IMAGE INFO da riempire con la descrizione dei \_ dati nel file di \_ origine.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere un percorso di memoria valido fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in D3DX10GetImageInfoFromResourceW. In caso contrario, la chiamata di funzione viene risolta in D3DX10GetImageInfoFromResourceA perché vengono usate stringhe ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di trama in D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
