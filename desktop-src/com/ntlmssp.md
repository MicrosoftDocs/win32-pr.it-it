---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706c788f103d3d616b5a3087522b5f06b417e972
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300546"
---
# <a name="ntlmssp"></a>NTLMSSP

NTLMSSP, il cui identificatore del servizio di autenticazione è RPC \_ C \_ AuthN \_ WinNT, è un Security Support Provider disponibile in tutte le versioni di DCOM. Usa il protocollo NTLM per l'autenticazione. NTLM non trasmette mai la password dell'utente al server durante l'autenticazione. Pertanto, il server non può utilizzare la password durante la rappresentazione per accedere alle risorse di rete a cui l'utente può accedere. È possibile accedere solo alle risorse locali.

NTLM funziona sia localmente che tra computer diversi. Ovvero, se il client e il server si trovano in computer diversi, NTLM può comunque assicurarsi che il client sia quello che dichiara di essere.

Con NTLM, l'identità del client viene rappresentata da un nome di dominio, un nome utente e una password o un token. Quando un server chiama [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket), vengono restituiti il nome di dominio e il nome utente del client. Tuttavia, quando un server chiama [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), viene restituito il token del client. Se non esiste alcuna relazione di trust tra client e server e se il server dispone di un account locale con lo stesso nome e la stessa password del client, l'account verrà utilizzato per rappresentare il client.

NTLM supporta l'autenticazione reciproca e cross-process (solo in locale). Se il client specifica il nome dell'entità del server nel formato utente del dominio \\ in una chiamata a [**IClientSecurity:: seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), l'identità del server deve corrispondere al nome dell'entità o la chiamata avrà esito negativo. Se il client specifica **null**, l'identità del server non verrà controllata.

NTLM supporta inoltre il livello di rappresentazione del delegato cross-thread e cross-process (solo localmente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pacchetti COM e di sicurezza](com-and-security-packages.md)
</dt> </dl>

 

 