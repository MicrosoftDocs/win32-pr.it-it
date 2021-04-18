---
title: Metodo IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Ottiene l'ora dell'ultima scrittura del file dalla chiave di riferimento del file del tipo di carattere.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Scrittura diretta metodo GetLastWriteTimeFromKey
- Metodo GetLastWriteTimeFromKey scrittura diretta, interfaccia IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader Interface Direct Write, metodo GetLastWriteTimeFromKey
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
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330158"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>Metodo IDWriteLocalFontFileLoader:: GetLastWriteTimeFromKey

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

*LastWriteTime* \[ out\]
</dt> <dd>

Tipo: **FILEtime \***

Ora dell'Ultima modifica del file del tipo di carattere.

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

 

 





