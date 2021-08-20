---
description: Il metodo Pause arresta temporaneamente l'acquisizione corrente.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: Metodo IStats::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d1bab0d66a081c175d997e093d7dd1ff2b0d1c9622ecff73e0b3b1473edc885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495211"
---
# <a name="istatspause-method"></a>Metodo IStats::P ause

Il **metodo Pause** arresta temporaneamente l'acquisizione corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:



| Codice restituito                                                                                            | Descrizione                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt> </dl>  | L'acquisizione è già sospesa.<br/>                                                                                                    |
| <dl> <dt>**NMERR \_ NON \_ ACQUISISCE**</dt> </dl>   | NPP non acquisisce dati. Chiamare il [metodo IStats::Start](istats-start.md) per avviare l'acquisizione.<br/>                            |
| <dl> <dt>**NMERR \_ NON \_ CONNESSO**</dt> </dl>   | NPP non è connesso alla rete. Chiamare il [metodo IStats::Connessione](istats-connect.md) per connettere NPP alla rete.<br/> |
| <dl> <dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt> </dl> | NPP è connesso alla rete, ma non con il [metodo IStats::Connessione.](istats-connect.md)<br/>                                |



 

## <a name="remarks"></a>Commenti

Mentre l'acquisizione è sospesa, i nuovi frame non vengono acquisiti fino a quando una chiamata al metodo [IStats::Resume](istats-resume.md) non riavvia l'acquisizione.

Quando si usano i metodi **IStats::P ause** e **IStats::Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione ogni volta che l'acquisizione è in esecuzione. [](c.md)

Per riavviare l'acquisizione, [chiamare IStats::Resume](istats-resume.md). Per arrestare l'acquisizione, chiamare [IStats::Stop](istats-stop.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Connessione](istats-connect.md)
</dt> <dt>

[IStats::Resume](istats-resume.md)
</dt> <dt>

[IStats::Start](istats-start.md)
</dt> <dt>

[IStats::Stop](istats-stop.md)
</dt> </dl>

 

 




