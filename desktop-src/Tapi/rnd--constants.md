---
description: Le costanti seguenti possono essere restituite come errori.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Costanti RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327403"
---
# <a name="rnd_-constants"></a>\_Costanti Rnd

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Le costanti seguenti possono essere restituite come errori.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**\_ora non valida per RND \_**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



Il valore di ora immesso non è valido.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**\_nome del \_ Server Rnd null \_**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



Il nome del server è **null**, probabilmente perché [**ITConferenceBlob:: init**](itconferenceblob-init.md) non è stato eseguito o non è riuscito.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ già \_ connesso**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



È stato chiamato il metodo [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) , ma esiste già una connessione.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ non \_ connesso**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



Il metodo [**ITDirectory:: Connect**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) non è stato chiamato o non è riuscito.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                               |
| Intestazione<br/>       | <dl> <dt>Rnderr. h</dt> </dl> |



 

 




