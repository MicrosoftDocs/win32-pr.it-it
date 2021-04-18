---
description: Passa un valore di chiave con tutti i dati associati richiesti dal modulo di decrittografia del contenuto per il sistema di chiavi specificato.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: 'Metodo IMFMediaKeySession:: Update'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 15bc06523f0cf9a7dc433381dd596cea89608ce7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320788"
---
# <a name="imfmediakeysessionupdate-method"></a>Metodo IMFMediaKeySession:: Update

Passa un valore di chiave con tutti i dati associati richiesti dal modulo di decrittografia del contenuto per il sistema di chiavi specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*key* 
</dt> <dd></dd> <dt>

*CB* 
</dt> <dd>

Conteggio in byte della *chiave*.

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

 

 




