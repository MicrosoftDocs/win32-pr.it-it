---
description: I membri dell'enumerazione PARTICIPANT TYPED INFO identificano il tipo di informazioni sul partecipante recuperate dal metodo \_ \_ ITParticipant::get \_ ParticipantTypedInfo. Questa enumerazione viene usata dalle applicazioni che accedono a IPConf MSP.
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: PARTICIPANT_TYPED_INFO enumerazione (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de57331cd0774409118b7253fd5705879e3b3504b04b20a16aa2df269504512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100571"
---
# <a name="participant_typed_info-enumeration"></a>Enumerazione PARTICIPANT \_ TYPED \_ INFO

\[**PARTECIPANTE \_ TYPED \_ INFO** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

I membri dell'enumerazione **PARTICIPANT \_ TYPED \_ INFO** identificano il tipo di informazioni sul partecipante recuperate dal metodo [**ITParticipant::get \_ ParticipantTypedInfo.**](itparticipant-get-participanttypedinfo.md) Questa enumerazione viene utilizzata dalle applicazioni che accedono a [IPConf MSP.](ipconf-msp.md)

## <a name="syntax"></a>Sintassi


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**
</dt> <dd>

Nome canonico del partecipante, ad esempio someone@example.com .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**NOME \_ PTI**
</dt> <dd>

Nome visualizzabile del partecipante.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EMAILADDRESS**
</dt> <dd>

Indirizzo di posta elettronica del partecipante.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**NUMERO DI \_ TELEFONO PTI**
</dt> <dd>

Indirizzo telefonico del partecipante.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**POSIZIONE \_ PTI**
</dt> <dd>

Indirizzo geografico del partecipante.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**STRUMENTO \_ PTI**
</dt> <dd>

Applicazione del partecipante.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**NOTE \_ PTI**
</dt> <dd>

Note relative al partecipante.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ PRIVATE**
</dt> <dd>

Definisce un'estensione SDES (Source Description) sperimentale o specifica dell'applicazione. Per informazioni dettagliate, vedere RFC 1889.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant::get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfacce MSP IPConf](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




