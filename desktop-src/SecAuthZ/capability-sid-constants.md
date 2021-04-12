---
description: Definire per le funzionalità note per le applicazioni tramite la funzione AllocateAndInitializeSid.
ms.assetid: CD27774F-0B70-4D97-96C9-B247536CC88E
title: Costanti SID della funzionalità (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55809cbb341bcbe60578043778bc824e09b8a295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234333"
---
# <a name="capability-sid-constants"></a>Costanti SID funzionalità

Le costanti SID della funzionalità definiscono per le funzionalità note di applicazioni tramite la funzione [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .

<dl> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT"></span><span id="security_capability_internet_client"></span>**\_ \_ client Internet funzionalità di sicurezza \_**
</dt> <dd> <dl> <dt>

(0x00000001L)
</dt> <dt>



Un account ha accesso a Internet da un computer client.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_INTERNET_CLIENT_SERVER"></span><span id="security_capability_internet_client_server"></span>**\_funzionalità di \_ sicurezza \_ server client Internet \_**
</dt> <dd> <dl> <dt>

(0x00000002L)
</dt> <dt>



Un account ha accesso a Internet dai computer client e server.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PRIVATE_NETWORK_CLIENT_SERVER"></span><span id="security_capability_private_network_client_server"></span>**\_funzionalità di \_ sicurezza \_ \_ server client di rete privata \_**
</dt> <dd> <dl> <dt>

(0x00000003L)
</dt> <dt>



Un account ha accesso a Internet da una rete privata.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_PICTURES_LIBRARY"></span><span id="security_capability_pictures_library"></span>**\_ \_ Libreria immagini per le funzionalità di sicurezza \_**
</dt> <dd> <dl> <dt>

(0x00000004L)
</dt> <dt>



Un account può accedere alla raccolta immagini.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_VIDEOS_LIBRARY"></span><span id="security_capability_videos_library"></span>**\_ \_ libreria video sulle funzionalità di sicurezza \_**
</dt> <dd> <dl> <dt>

(0x00000005L)
</dt> <dt>



Un account può accedere alla raccolta video.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_MUSIC_LIBRARY"></span><span id="security_capability_music_library"></span>**\_ \_ libreria musicale della funzionalità di sicurezza \_**
</dt> <dd> <dl> <dt>

(0x00000006L)
</dt> <dt>



Un account può accedere alla raccolta musicale.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_DOCUMENTS_LIBRARY"></span><span id="security_capability_documents_library"></span>**\_ \_ raccolta documenti funzionalità di sicurezza \_**
</dt> <dd> <dl> <dt>

(0x00000007L)
</dt> <dt>



Un account ha accesso alla libreria della documentazione di.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_ENTERPRISE_AUTHENTICATION"></span><span id="security_capability_enterprise_authentication"></span>**\_ \_ autenticazione Enterprise per le funzionalità di sicurezza \_**
</dt> <dd> <dl> <dt>

(0x00000008L)
</dt> <dt>



Un account ha accesso alle credenziali di Windows predefinite.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_SHARED_USER_CERTIFICATES"></span><span id="security_capability_shared_user_certificates"></span>**\_funzionalità di \_ sicurezza \_ certificati utente condivisi \_**
</dt> <dd> <dl> <dt>

(0x00000009L)
</dt> <dt>



Un account può accedere ai certificati utente condivisi.


</dt> </dl> </dd> <dt>

<span id="SECURITY_CAPABILITY_REMOVABLE_STORAGE"></span><span id="security_capability_removable_storage"></span>**\_ \_ archiviazione rimovibile della funzionalità di sicurezza \_**
</dt> <dd> <dl> <dt>

(0x0000000AL)
</dt> <dt>



Un account può accedere all'archiviazione rimovibile.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Quando si costruisce un SID di funzionalità, è necessario includere l'autorità del pacchetto di sicurezza del \_ pacchetto dell'app \_ \_ {0,0,0,0,0,15} nella chiamata alla funzione [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) . Inoltre, è necessario il conteggio RID di base e RID per le funzionalità predefinite, SECURITY \_ Capability \_ base \_ RID (0X00000003L) e Security \_ Builtin \_ Capability \_ RID \_ Count (2L).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

