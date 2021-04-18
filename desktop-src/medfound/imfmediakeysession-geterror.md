---
description: Ottiene lo stato di errore associato alla sessione del tasto multimediale.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'Metodo IMFMediaKeySession:: GetError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320789"
---
# <a name="imfmediakeysessiongeterror-method"></a>Metodo IMFMediaKeySession:: GetError

Ottiene lo stato di errore associato alla sessione del tasto multimediale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*code* 
</dt> <dd>

Codice di errore.

</dd> <dt>

*systemCode* 
</dt> <dd>

Informazioni sugli errori specifici della piattaforma.

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

[**IMFMediaKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




