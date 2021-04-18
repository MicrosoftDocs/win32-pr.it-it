---
description: Il \_ metodo Get participates crea una raccolta di partecipanti associati alla conferenza corrente.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'Metodo ITParticipantControl:: get_Participants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327308"
---
# <a name="itparticipantcontrolget_participants-method"></a>Metodo ITParticipantControl:: Get \_ participates

\[**ottenere \_ I partecipanti** non sono disponibili per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ participates** crea una raccolta di partecipanti associati alla conferenza corrente. Questo metodo viene fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic. Le applicazioni C e C++ devono usare il metodo [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVariant* \[ out\]
</dt> <dd>

Puntatore a **Variant** contenente un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) di puntatori dell'interfaccia [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pVariant* non è un puntatore valido.<br/>     |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

TAPI chiama il metodo **AddRef** sull'interfaccia [**ITParticipant**](itparticipant.md) restituita da **ITParticipantControl:: Get \_ participates**. L'applicazione deve chiamare **Release** sull'interfaccia **ITParticipant** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




