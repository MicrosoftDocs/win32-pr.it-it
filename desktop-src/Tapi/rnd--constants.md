---
description: Le costanti seguenti possono essere restituite come errori.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: RND_ costanti (Rnderr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ed1b55b0ed18215fb17e27504c309c67b0cea3351acea6cffadc4b3ff31c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773371"
---
# <a name="rnd_-constants"></a>Costanti \_ RND

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Le costanti seguenti possono essere restituite come errori.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**TEMPO RND \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



Il valore di ora immesso non è valido.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**RND NULL SERVER NAME (NOME \_ SERVER NULL RND) \_ \_**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



Il nome del server **è NULL,** probabilmente perché [**ITConferenceBlob::Init**](itconferenceblob-init.md) non è stato eseguito o non è riuscito.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ GIÀ \_ CONNESSO**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



È [**stato chiamato il metodo ITDirectory::Connessione,**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) ma esiste già una connessione.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ NON \_ CONNESSO**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



Il [**metodo ITDirectory::Connessione**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) non è stato chiamato o ha avuto esito negativo.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                               |
| Intestazione<br/>       | <dl> <dt>Rnderr.h</dt> </dl> |



 

 




