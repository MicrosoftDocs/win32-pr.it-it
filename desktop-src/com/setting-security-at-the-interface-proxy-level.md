---
title: Impostazione della sicurezza a livello di proxy di interfaccia
description: In alcuni casi il client necessita di un controllo granulare sulla sicurezza nelle chiamate a determinate interfacce.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ef969039dcfdc12449b7a8d0a3d63729ab5f84061ade1a743d21a1b6b34331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309096"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Impostazione della sicurezza a livello di proxy di interfaccia

In alcuni casi il client necessita di un controllo granulare sulla sicurezza nelle chiamate a determinate interfacce. Ad esempio, la sicurezza potrebbe essere impostata a un livello basso per il processo, ma le chiamate a una particolare interfaccia potrebbero richiedere un livello di autenticazione superiore, ad esempio la crittografia. I metodi [**dell'interfaccia IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) consentono al client di modificare le impostazioni di sicurezza associate alle chiamate a una particolare interfaccia controllando le impostazioni di sicurezza a livello di interfaccia-proxy.

Il client può eseguire una query su un oggetto esistente per [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e quindi chiamare il metodo [**IClientSecurity::QueryBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) per individuare le impostazioni di sicurezza correnti per un proxy di interfaccia specifico. Il [**metodo IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) può essere usato per modificare le impostazioni di sicurezza per un singolo proxy di interfaccia nell'oggetto prima di chiamare uno dei metodi dell'interfaccia. Le nuove impostazioni si applicano a tutti i chiamanti futuri di questa particolare interfaccia. Il [**metodo IClientSecurity::CopyProxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) consente al client di copiare un proxy di interfaccia in modo che le chiamate successive a **SetBlanket** nella copia non influiscano sui chiamanti del proxy originale.

[**SetBlanket viene**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) comunemente usato per aumentare il livello di autenticazione per un particolare proxy di interfaccia a un livello superiore di protezione della sicurezza. Tuttavia, in alcune situazioni può essere utile anche ridurre il livello di autenticazione per un proxy di interfaccia specifico. Si supponga, ad esempio, che il livello di autenticazione predefinito per il processo sia un valore diverso da RPC C AUTHN LEVEL NONE e che il client e il server si trovano in domini separati che non si fidano \_ l'uno \_ \_ \_ dell'altro. In questo caso, le chiamate al server avranno esito negativo a meno che il client non chiami **SetBlanket** per ridurre il livello di autenticazione a RPC \_ C \_ AUTHN \_ LEVEL \_ NONE.

I client che usano l'implementazione predefinita di [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) fornita dal gestore proxy possono chiamare le funzioni helper [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)e [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) anziché chiamare direttamente i metodi **IClientSecurity.** Le funzioni helper semplificano il codice, ma sono leggermente meno efficienti rispetto alla chiamata diretta dei metodi **IClientSecurity** corrispondenti.

[**L'interfaccia IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) viene implementata in locale per il client dal gestore proxy. Alcuni oggetti con marshalling personalizzato potrebbero non supportare **IClientSecurity.**

[**IClientSecurity funziona**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) con tutti i servizi di autenticazione supportati (attualmente NTLMSSP, Schannel e il protocollo Kerberos v5).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 