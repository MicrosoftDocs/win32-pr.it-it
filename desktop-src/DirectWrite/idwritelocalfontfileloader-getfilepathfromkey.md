---
title: Metodo IDWriteLocalFontFileLoader GetFilePathFromKey
description: Ottiene il percorso del file del tipo di carattere assoluto dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Scrittura diretta metodo GetFilePathFromKey
- Metodo GetFilePathFromKey scrittura diretta, interfaccia IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader Interface Direct Write, metodo GetFilePathFromKey
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
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329142"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>Metodo IDWriteLocalFontFileLoader:: GetFilePathFromKey

Ottiene il percorso del file del tipo di carattere assoluto dalla chiave di riferimento del file del tipo di carattere.

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

*fontFileReferenceKey* \[ in\]
</dt> <dd>

Tipo: **const \* void**

Chiave di riferimento del file del tipo di carattere che identifica in modo univoco il file del tipo di carattere locale nell'ambito del caricatore del tipo di carattere utilizzato.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UInt32**

Dimensioni in byte della chiave di riferimento del file del tipo di carattere.

</dd> <dt>

*filePath* \[ out\]
</dt> <dd>

Tipo: **WCHAR \***

Matrice di caratteri che riceve il percorso del file locale.

</dd> <dt>

*filePathSize* 
</dt> <dd>

Tipo: **UInt32**

Lunghezza della matrice di caratteri del percorso del file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>DWrite. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





