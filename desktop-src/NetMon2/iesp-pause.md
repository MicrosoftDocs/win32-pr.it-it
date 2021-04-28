---
description: "Metodo IESP::P ause: il metodo Pause sospende l'acquisizione corrente."
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: Metodo IESP::P ause (Netmon.h)
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
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084239"
---
# <a name="iesppause-method"></a>Metodo IESP::P ause

Il **metodo Pause** sospende l'acquisizione corrente.

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

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                           | Descrizione                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt> </dl> | L'acquisizione è già sospesa.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>  | Il NPP non acquisisce dati. Chiamare [IESP::Start](iesp-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>  | Il NPP non è connesso alla rete. Chiamare [IESP::Connect](iesp-connect.md) per connettere il NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ ESP**</dt> </dl>        | Il NPP è connesso alla rete, ma non con il [metodo IESP::Connect.](iesp-connect.md)<br/>                     |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione è in pausa, i nuovi dati non vengono aggiunti al [*file*](c.md) di acquisizione corrente finché non si chiama il metodo [IESP::Resume](iesp-resume.md) per riavviare l'acquisizione. Quando **sospendi** **e** riprendi vengono usati per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.

Quando si usano i metodi **IESP::P ause** e **IESP::Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione ogni volta che l'acquisizione è in esecuzione. [](c.md)

Per riavviare l'acquisizione, chiamare [IESP::Resume](iesp-resume.md). Per arrestare l'acquisizione, chiamare [IESP::Stop](iesp-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP::Connect](iesp-connect.md)
</dt> <dt>

[IESP::Resume](iesp-resume.md)
</dt> <dt>

[IESP::Start](iesp-start.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> </dl>

 

 




