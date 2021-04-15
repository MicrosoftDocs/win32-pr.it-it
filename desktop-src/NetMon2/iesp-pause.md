---
description: Il metodo pause sospende l'acquisizione corrente.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: Metodo IESP::P ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525117"
---
# <a name="iesppause-method"></a>IESP::P metodo ause

Il metodo **pause** sospende l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpStats* 
</dt> <dd>

Obsoleta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_acquisizione NMERR \_ sospesa**</dt> </dl> | Acquisizione già sospesa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ non \_ acquisizione**</dt> </dl>  | L'oggetto NPP non sta acquisendo dati. Chiamare [IESP:: Start](iesp-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connesso**</dt> </dl>  | L'oggetto NPP non è connesso alla rete. Chiamare [IESP:: Connect](iesp-connect.md) per connettere l'oggetto NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>        | L'oggetto NPP è connesso alla rete, ma non con il metodo [IESP:: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono aggiunti al [*file di acquisizione*](c.md) corrente fino a quando non viene chiamato il metodo [IESP:: Resume](iesp-resume.md) per riavviare l'acquisizione. Quando si utilizzano **pause** e **Resume** per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si usano i metodi **IESP::P ause** e **IESP:: Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) ogni volta che viene eseguita l'acquisizione.

Per riavviare l'acquisizione, chiamare [IESP:: Resume](iesp-resume.md). Per arrestare l'acquisizione, chiamare [IESP:: Stop](iesp-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP:: Resume](iesp-resume.md)
</dt> <dt>

[IESP:: Start](iesp-start.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> </dl>

 

 




