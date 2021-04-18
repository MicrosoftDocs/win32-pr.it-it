---
title: Metodo IDWriteLocalFontFileLoader GetFilePathLengthFromKey
description: Ottiene la lunghezza del percorso del file assoluto dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Scrittura diretta metodo GetFilePathLengthFromKey
- Metodo GetFilePathLengthFromKey scrittura diretta, interfaccia IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader Interface Direct Write, metodo GetFilePathLengthFromKey
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
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330159"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>Metodo IDWriteLocalFontFileLoader:: GetFilePathLengthFromKey

Ottiene la lunghezza del percorso del file assoluto dalla chiave di riferimento del file del tipo di carattere.

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

*fontFileReferenceKey* \[ in\]
</dt> <dd>

Tipo: **const \* void**

Chiave di riferimento del file del tipo di carattere che identifica in modo univoco il file del tipo di carattere locale nell'ambito del caricatore del tipo di carattere utilizzato.

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

Tipo: **UInt32**

Dimensione della chiave di riferimento del file del tipo di carattere in byte.

</dd> <dt>

*filePathLength* \[ out\]
</dt> <dd>

Tipo: **UInt32 \***

Lunghezza della stringa del percorso del file, escluso il carattere **null** terminato.

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

 

 





