---
description: Definire per le applicazioni funzionalità note usando la funzione AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Costanti SID funzionalità (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37a06c0bd0115c4f7d05753825477b5de4948d1ddb9576aea46933a63cbf409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783215"
---
# <a name="capability-sid-constants"></a>Costanti SID funzionalità

Le costanti SID delle funzionalità definiscono per le applicazioni funzionalità note tramite la [**funzione AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**FUNZIONALITÀ \_ DI SICUREZZA CLIENT \_ INTERNET \_**
</dt> <dd> <dl> <dt>

(0x00000001L)
</dt> <dt>



Un account ha accesso a Internet da un computer client.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**FUNZIONALITÀ \_ DI SICUREZZA SERVER \_ CLIENT INTERNET \_ \_**
</dt> <dd> <dl> <dt>

(0x00000002L)
</dt> <dt>



Un account ha accesso a Internet dai computer client e server.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**FUNZIONALITÀ \_ DI SICUREZZA SERVER CLIENT DI RETE \_ \_ \_ \_ PRIVATA**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Un account ha accesso a Internet da una rete privata.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**RACCOLTA \_ IMMAGINI DELLE FUNZIONALITÀ DI \_ \_ SICUREZZA**
</dt> <dd> <dl> <dt>

(0x00000004L)
</dt> <dt>



Un account ha accesso alla raccolta immagini.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**RACCOLTA \_ VIDEO SULLA FUNZIONALITÀ DI \_ \_ SICUREZZA**
</dt> <dd> <dl> <dt>

(0x00000005L)
</dt> <dt>



Un account ha accesso alla raccolta video.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**LIBRERIA \_ MUSIC PER LE FUNZIONALITÀ DI \_ \_ SICUREZZA**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Un account ha accesso alla raccolta musicale.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**RACCOLTA \_ DOCUMENTI DELLE FUNZIONALITÀ DI \_ \_ SICUREZZA**
</dt> <dd> <dl> <dt>

(0x00000007L)
</dt> <dt>



Un account ha accesso alla libreria della documentazione.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**SECURITY \_ CAPABILITY \_ ENTERPRISE \_ AUTHENTICATION**
</dt> <dd> <dl> <dt>

(0x00000008L)
</dt> <dt>



Un account ha accesso alle credenziali Windows predefinite.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**CERTIFICATI \_ UTENTE CONDIVISI DELLE FUNZIONALITÀ DI \_ \_ \_ SICUREZZA**
</dt> <dd> <dl> <dt>

(0x00000009L)
</dt> <dt>



Un account ha accesso ai certificati utente condivisi.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**FUNZIONALITÀ \_ DI SICUREZZA ARCHIVI \_ \_ RIMOVIBILI**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Un account ha accesso all'archiviazione rimovibile.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Quando si costruisce un SID di funzionalità, è necessario includere l'autorità del pacchetto, SECURITY APP PACKAGE AUTHORITY, nella chiamata alla \_ \_ funzione \_ {0,0,0,0,0,15} [**AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) Sono inoltre necessari il numero di RID e RID di base per le funzionalità incorporate, SECURITY \_ CAPABILITY \_ BASE RID \_ (0x00000003L) e SECURITY \_ BUILTIN \_ CAPABILITY RID COUNT \_ \_ (2L).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Winnt.h</dt> </dl> |



 

