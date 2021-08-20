---
title: Metodo IDWriteLocalFontFileLoader GetFilePathLengthFromKey
description: Ottiene la lunghezza del percorso assoluto del file dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Metodo GetFilePathLengthFromKey Direct Write
- Metodo GetFilePathLengthFromKey Direct Write, interfaccia IDWriteLocalFontFileLoader
- Metodo GetFilePathLengthFromKey dell'interfaccia IDWriteLocalFontFileLoader
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587f432f006493097ec8262fcc2201e2c3b67abe7115c395332671ec35efeba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816352"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>Metodo IDWriteLocalFontFileLoader::GetFilePathLengthFromKey

Ottiene la lunghezza del percorso assoluto del file dalla chiave di riferimento del file del tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fontFileReferenceKey* \[ Pollici\]
</dt> <dd>

Tipo: **const \* void**

Chiave di riferimento del file del tipo di carattere che identifica in modo univoco il file del tipo di carattere locale nell'ambito del caricatore del tipo di carattere in uso.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UINT32**

Dimensione in byte della chiave di riferimento del file del tipo di carattere.

</dd> <dt>

*filePathLength* \[ Cambio\]
</dt> <dd>

Tipo: **UINT32 \***

Lunghezza della stringa del percorso del file, senza includere il carattere **NULL** terminato.

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

 

 





