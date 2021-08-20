---
title: NTLMSSP
description: NTLMSSP
ms.assetid: ae434165-4429-4ef0-b083-60abdfc50de0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e786a586810a7404f242c9a129cbfccc03849a50f7ea6625288c7334e47e8787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105298"
---
# <a name="ntlmssp"></a>NTLMSSP

NTLMSSP, il cui identificatore del servizio di autenticazione è RPC \_ C AUTHN WINNT, è un provider di supporto per la sicurezza disponibile in tutte \_ le versioni di \_ DCOM. Usa il protocollo NTLM per l'autenticazione. NTLM non trasmette mai la password dell'utente al server durante l'autenticazione. Pertanto, il server non può utilizzare la password durante la rappresentazione per accedere alle risorse di rete a cui l'utente avrebbe accesso. È possibile accedere solo alle risorse locali.

NTLM funziona sia in locale che tra computer. In altri modi, se il client e il server si trova in computer diversi, NTLM può comunque assicurarsi che il client sia quello che dichiara di essere.

Con NTLM, l'identità del client è rappresentata da un nome di dominio, un nome utente e una password o un token. Quando un server chiama [**CoQueryClientBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)vengono restituiti il nome di dominio e il nome utente del client. Tuttavia, quando un server chiama [**CoImpersonateClient,**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)viene restituito il token del client. Se non esiste alcuna relazione di trust tra client e server e se il server ha un account locale con lo stesso nome e password del client, tale account verrà utilizzato per rappresentare il client.

NTLM supporta l'autenticazione reciproca tra thread e tra processi (solo localmente). Se il client specifica il nome dell'entità del server nel formato utente di dominio in una chiamata \\ a [**IClientSecurity::SetBlanket,**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)l'identità del server deve corrispondere al nome dell'entità. In caso contrario, la chiamata avrà esito negativo. Se il client specifica **NULL,** l'identità del server non verrà controllata.

NTLM supporta inoltre il livello di rappresentazione delegato tra thread e cross-process (solo localmente).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pacchetti com e di sicurezza](com-and-security-packages.md)
</dt> </dl>

 

 