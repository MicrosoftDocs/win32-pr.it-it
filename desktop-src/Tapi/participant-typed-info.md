---
description: "I membri dell'enum del \\_ partecipante \\_ informazioni tipizzate identificano il tipo di informazioni del partecipante recuperato dal metodo ITParticipant:: Get \\_ ParticipantTypedInfo. Questa enumerazione viene utilizzata dalle applicazioni che accedono al IPConf MSP."
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: Enumerazione PARTICIPANT_TYPED_INFO (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327489"
---
# <a name="participant_typed_info-enumeration"></a>\_Enumerazione informazioni tipizzate partecipante \_

\[**Partecipante \_ Le \_ informazioni tipizzate** non sono disponibili per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

I membri dell'enum **del \_ partecipante \_ informazioni tipizzate** identificano il tipo di informazioni del partecipante recuperato dal metodo [**ITParticipant:: Get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) . Questa enumerazione viene utilizzata dalle applicazioni che accedono al [IPConf msp](ipconf-msp.md).

## <a name="syntax"></a>Sintassi


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**\_formato canonico PTI**
</dt> <dd>

Nome canonico del partecipante, ad esempio someone@example.com .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**\_nome PTI**
</dt> <dd>

Nome visualizzabile del partecipante.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**\_EMAILADDRESS PTI**
</dt> <dd>

Indirizzo di posta elettronica del partecipante.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**\_PhoneNumber PTI**
</dt> <dd>

Indirizzo telefonico del partecipante.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_località PTI**
</dt> <dd>

Indirizzo geografico del partecipante.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_strumento PTI**
</dt> <dd>

Applicazione del partecipante.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**\_Note PTI**
</dt> <dd>

Note relative al partecipante.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**\_privato PTI**
</dt> <dd>

Definisce un'estensione memoria SDES (Experimental Source Description) sperimentale o specifica dell'applicazione. Per informazioni dettagliate, vedere RFC 1889.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant:: Get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> <dt>

[Interfacce MSP IPConf](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




