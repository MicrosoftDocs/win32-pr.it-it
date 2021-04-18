---
description: Ottiene l'oggetto chiavi multimediali associato al motore multimediale o null se non è presente un oggetto chiavi multimediali.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'Metodo IMFMediaEngineEME:: get_Keys'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320754"
---
# <a name="imfmediaengineemeget_keys-method"></a>Metodo IMFMediaEngineEME:: Get \_ Keys

Ottiene l'oggetto chiavi multimediali associato al motore multimediale o **null** se non è presente un oggetto chiavi multimediali.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiavi* 
</dt> <dd>

Oggetto chiavi multimediali associato al motore multimediale o **null** se non è presente un oggetto chiavi multimediali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFMediaEngineEME**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




