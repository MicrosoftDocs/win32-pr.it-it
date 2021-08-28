---
title: Impostazione Process-Wide sicurezza con CoInitializeSecurity
description: La funzione CoInitializeSecurity consente di controllare scenari di sicurezza complessi impostando la sicurezza per un'applicazione a livello di codice.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c3e601897e9f2313682a3474c1760bc211285d8fa81a82f67d114681a7a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610891"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Impostazione Process-Wide sicurezza con CoInitializeSecurity

La [**funzione CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) consente di controllare scenari di sicurezza complessi impostando la sicurezza per un'applicazione a livello di codice. Questo argomento descrive gli scenari in cui è possibile usare **CoInitializeSecurity** e fornisce alcuni dettagli su come usarlo.

Esistono diversi motivi per cui è consigliabile usare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza a livello di processo all'interno del programma. Ad esempio, anche se è possibile impostare il livello di autenticazione e le autorizzazioni di accesso per l'applicazione utilizzando dcomcnfg.exe, il livello di rappresentazione predefinito per il computer potrebbe non essere quello desiderato per il processo. L'unico modo per modificare questa impostazione per il processo è chiamare **CoInitializeSecurity.**

Se si vuole usare il provider di sicurezza Schannel, è necessario specificarlo come servizio di autenticazione in una chiamata a [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

Un altro scenario comune in cui è possibile impostare la sicurezza a livello di processo a livello di codice è quando si vuole impostare la sicurezza predefinita per l'intero processo, ma si dispone di uno o più oggetti all'interno del processo che espongono interfacce con requisiti di sicurezza speciali. In questo caso, è possibile chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza per il processo, consentendo a COM di gestire la maggior parte dei controlli di sicurezza, ed è possibile chiamare altri metodi per impostare la sicurezza per gli oggetti con esigenze di sicurezza speciali. La chiamata di questi metodi e funzioni è descritta in [Impostazione della sicurezza a livello di proxy di interfaccia.](setting-security-at-the-interface-proxy-level.md)

Se l'applicazione ha requisiti di sicurezza molto specializzati, ad esempio consentire a determinati gruppi di accedere a oggetti diversi a seconda dell'ora del giorno, è possibile gestire tutta la sicurezza a livello di codice, assicurandosi che COM non eserviti alcun controllo automatico. A tale scopo, è necessario chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), impostando il *parametro dwAuthnLevel* su none e il *parametro pVoid* su **NULL.** Se si dispone di un pacchetto di sicurezza personalizzato, è necessario registrarlo anche nel *parametro pAuthnSvc.* È quindi possibile gestire tutta la sicurezza a livello di codice tramite chiamate all'interfaccia a livello di proxy e le funzioni descritte in Impostazione della sicurezza a [livello di proxy di interfaccia.](setting-security-at-the-interface-proxy-level.md)

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) offre un set di funzionalità avanzate. Se si chiama **CoInitializeSecurity,** i valori del Registro di sistema vengono ignorati e vengono usati i valori di inizializzazione di sicurezza passati alla chiamata. A seconda del risultato desiderato, il primo parametro, *pVoid*, può puntare a tre tipi diversi di valori: [**un \_ DESCRIPTOR DI SICUREZZA,**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) un [**oggetto IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntatore a un AppID. Nella maggior parte dei casi, si useranno Windows per creare **un \_ DESCRITTORE DI SICUREZZA** a cui *pVoid* farà riferimento.

Tuttavia, *pVoid* può anche puntare a un [**oggetto IAccessControl.**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol)

Per indicare a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) che si sta passando un oggetto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) a *pVoid,* è necessario passare il valore EOAC ACCESS CONTROL al \_ parametro \_ *dwCapabilities.* Poiché **CoInitializeSecurity memorizza** nella cache i risultati dei controlli di accesso, l'elenco di controllo di accesso non deve essere modificato dopo aver chiamato **CoInitializeSecurity.**

Un altro tipo di valore che è possibile passare al *parametro pVoid* è un puntatore a un GUID, ovvero l'AppID dell'applicazione. Se *pVoid* è un puntatore a un AppID, è necessario specificare EOAC APPID nel parametro pCapabilities in modo che la funzione conosca il valore previsto \_ in *pVoid*.  Se *pVoid punta* a un AppID, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) usa solo il Registro di sistema per i valori di autenticazione e ignora tutti gli altri parametri di **CoInitializeSecurity.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della Process-Wide sicurezza](setting-processwide-security.md)
</dt> </dl>

 

 