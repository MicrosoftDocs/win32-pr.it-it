---
title: Impostazione della sicurezza a livello di proxy di interfaccia
description: A volte il client necessita di un controllo accurato della sicurezza sulle chiamate a interfacce particolari.
ms.assetid: 72925ca2-78c9-47d9-8760-63f6379326d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b38fe83e8ce8841cc9029808a6947ec67d4eaf4
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300508"
---
# <a name="setting-security-at-the-interface-proxy-level"></a>Impostazione della sicurezza a livello di proxy di interfaccia

A volte il client necessita di un controllo accurato della sicurezza sulle chiamate a interfacce particolari. Ad esempio, la sicurezza potrebbe essere impostata a un livello basso per il processo, ma le chiamate a un'interfaccia specifica potrebbero richiedere un livello di autenticazione superiore, ad esempio la crittografia. I metodi dell'interfaccia [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) consentono al client di modificare le impostazioni di sicurezza associate alle chiamate a una particolare interfaccia controllando le impostazioni di sicurezza a livello di interfaccia-proxy.

Il client può eseguire una query su un oggetto esistente per [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e quindi chiamare il metodo [**IClientSecurity:: QueryBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-queryblanket) per individuare le impostazioni di sicurezza correnti per un particolare proxy di interfaccia. Il metodo [**IClientSecurity:: Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) può essere usato per modificare le impostazioni di sicurezza per un singolo proxy di interfaccia nell'oggetto prima di chiamare uno dei metodi dell'interfaccia. Le nuove impostazioni si applicano a tutti i chiamanti futuri di questa particolare interfaccia. Il metodo [**IClientSecurity:: CopyProxy**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-copyproxy) fornisce un modo per il client di copiare un proxy di interfaccia in modo che le chiamate successive a **seblankt** sulla copia non influiscano sui chiamanti del proxy originale.

Il metodo [**Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) viene comunemente usato per aumentare il livello di autenticazione per un particolare proxy di interfaccia a un livello superiore di protezione della sicurezza. In alcune situazioni, tuttavia, può essere utile anche abbassare il livello di autenticazione per un particolare proxy di interfaccia. Si supponga, ad esempio, che il livello di autenticazione predefinito per il processo sia un valore diverso dal \_ livello auth C di RPC \_ \_ \_ e che il client e il server si trovino in domini distinti che non si considerano attendibili reciprocamente. In questo caso, le chiamate al server avranno esito negativo a meno che il client non chiami il metodo **Seblankt** per abbassare il livello di autenticazione al \_ livello auth C di RPC \_ \_ \_ .

I client che usano l'implementazione predefinita di [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) fornita da gestione proxy possono chiamare le funzioni di supporto [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)e [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) invece di chiamare direttamente i metodi **IClientSecurity** . Le funzioni di supporto semplificano il codice, ma sono leggermente meno efficienti rispetto alla chiamata diretta dei metodi **IClientSecurity** corrispondenti.

L'interfaccia [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) viene implementata localmente per il client da gestione proxy. Alcuni oggetti con marshalling personalizzato potrebbero non supportare **IClientSecurity**.

[**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) funziona con tutti i servizi di autenticazione supportati (attualmente NTLMSSP, Schannel e il protocollo Kerberos V5).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 