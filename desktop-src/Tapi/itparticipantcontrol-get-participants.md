---
description: Il metodo get \_ Participants crea una raccolta di partecipanti associati alla conferenza corrente.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: Metodo ITParticipantControl::get_Participants (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d61d12de18e30bd86d42fd1aa75aed2048c42e487e019eabe3da6d65e70a9f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864712"
---
# <a name="itparticipantcontrolget_participants-method"></a>Metodo ITParticipantControl::get \_ Participants

\[**get \_ I partecipanti** non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo get \_ Participants** crea una raccolta di partecipanti associati alla conferenza corrente. Questo metodo viene fornito per le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic. Le applicazioni C e C++ devono usare il [**metodo EnumerateParticipants.**](itparticipantcontrol-enumerateparticipants.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVariant* \[ Cambio\]
</dt> <dd>

Puntatore **a VARIANT** contenente un oggetto [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) di puntatori a interfaccia [**ITParticipant.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro pVariant* non è un puntatore valido.<br/>     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

TAPI chiama **il metodo AddRef** sull'interfaccia [**ITParticipant**](itparticipant.md) restituita da **ITParticipantControl::get \_ Participants.** L'applicazione deve **chiamare Release** **sull'interfaccia ITParticipant** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
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

 

 




