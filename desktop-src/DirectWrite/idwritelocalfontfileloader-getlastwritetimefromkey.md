---
title: Metodo IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Metodo GetLastWriteTimeFromKey Direct Write
- Metodo GetLastWriteTimeFromKey Scrittura diretta, interfaccia IDWriteLocalFontFileLoader
- Metodo GetLastWriteTimeFromKey dell'interfaccia IDWriteLocalFontFileLoader
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2fb3d79475a943c3a635b347cfd6dbe41e8b3a8903022bae9089e1d6a9847c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816315"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>Metodo IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey

Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
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

Dimensioni della chiave di riferimento al file del tipo di carattere in byte.

</dd> <dt>

*lastWriteTime* \[ Cambio\]
</dt> <dd>

Tipo: **FILETIME \***

Ora dell'ultima modifica del file del tipo di carattere.

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

 

 





