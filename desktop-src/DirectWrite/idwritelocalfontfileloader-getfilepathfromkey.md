---
title: Metodo GetFilePathFromKey di IDWriteLocalFontFileLoader
description: Ottiene il percorso assoluto del file del tipo di carattere dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Metodo GetFilePathFromKey Direct Write
- Metodo GetFilePathFromKey Direct Write, interfaccia IDWriteLocalFontFileLoader
- Metodo GetFilePathFromKey dell'interfaccia DIRECT Write dell'interfaccia IDWriteLocalFontFileLoader
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7739cfa4a03abb3506bd63a84e0c747021110198f7d0ffefa69116656cbfa616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928031"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>Metodo IDWriteLocalFontFileLoader::GetFilePathFromKey

Ottiene il percorso assoluto del file del tipo di carattere dalla chiave di riferimento del file del tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fontFileReferenceKey* \[ Pollici\]
</dt> <dd>

Tipo: **const \* void**

Chiave di riferimento del file del tipo di carattere che identifica in modo univoco il file del tipo di carattere locale all'interno dell'ambito del caricatore del tipo di carattere in uso.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

Dimensione in byte della chiave di riferimento del file del tipo di carattere.

</dd> <dt>

*filePath* \[ Cambio\]
</dt> <dd>

Tipo: **WCHAR \***

Matrice di caratteri che riceve il percorso del file locale.

</dd> <dt>

*filePathSize* 
</dt> <dd>

Tipo: **UINT32**

Lunghezza della matrice di caratteri del percorso del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





