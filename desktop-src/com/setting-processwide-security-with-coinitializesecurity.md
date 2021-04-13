---
title: Impostazione Process-Wide sicurezza con CoInitializeSecurity
description: La funzione CoInitializeSecurity consente di controllare scenari di sicurezza complessi impostando la sicurezza per un'applicazione a livello di codice.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567a6dfaf47dbd278fc248558cd25969c733b24a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399784"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Impostazione Process-Wide sicurezza con CoInitializeSecurity

La funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) consente di controllare scenari di sicurezza complessi impostando la sicurezza per un'applicazione a livello di codice. Questo argomento descrive gli scenari in cui è possibile usare **CoInitializeSecurity** e fornisce alcuni dettagli su come usarlo.

Esistono diversi motivi per cui è consigliabile usare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza a livello di processo all'interno del programma. Ad esempio, anche se è possibile impostare il livello di autenticazione e le autorizzazioni di accesso per l'applicazione tramite dcomcnfg.exe, il livello di rappresentazione predefinito per il computer potrebbe non essere quello desiderato per il processo. L'unico modo per modificare questa impostazione per il processo consiste nel chiamare **CoInitializeSecurity**.

Se si desidera utilizzare il provider di sicurezza Schannel, è necessario specificarlo come servizio di autenticazione in una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Un altro scenario comune in cui è possibile impostare la sicurezza a livello di processo a livello di programmazione è quando si desidera impostare la sicurezza predefinita per l'intero processo, ma si dispone di uno o più oggetti all'interno di tale processo che espongono interfacce con requisiti di sicurezza speciali. In questo caso, è possibile chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza per il processo, consentendo a com di gestire la maggior parte dei controlli di sicurezza ed è possibile chiamare altri metodi per impostare la sicurezza per gli oggetti con particolari esigenze di sicurezza. La chiamata di questi metodi e funzioni è descritta in [impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).

Se l'applicazione presenta requisiti di sicurezza molto specializzati, ad esempio consentendo a determinati gruppi di accedere a oggetti diversi a seconda dell'ora del giorno, potrebbe essere necessario gestire la sicurezza a livello di codice, assicurandosi che COM non esegue alcuna verifica automatica. A tale scopo, è necessario chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), impostando il parametro *dwAuthnLevel* su None e il parametro *PVOID* su **null**. Se si dispone di un pacchetto di sicurezza personalizzato, è necessario registrarlo anche nel parametro *pAuthnSvc* . È quindi possibile gestire tutta la propria sicurezza a livello di codice tramite chiamate all'interfaccia a livello di proxy e funzioni descritte in [impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) offre un set completo di funzionalità. Se si chiama **CoInitializeSecurity**, i valori del registro di sistema vengono ignorati e vengono invece usati i valori di inizializzazione di sicurezza passati alla chiamata. A seconda del risultato desiderato, il primo parametro, *PVOID*, può puntare a tre tipi diversi di valori: un [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , un oggetto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) o un puntatore a un AppID. Nella maggior parte dei casi, si utilizzeranno le funzioni di Windows per creare un **\_ descrittore di sicurezza** a cui punterà *PVOID* .

Tuttavia, *PVOID* può puntare anche a un oggetto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) .

Per indicare a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) che si sta passando un oggetto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) a *PVOID*, è necessario passare il \_ \_ valore di controllo di accesso EOAC al parametro *dwCapabilities* . Poiché **CoInitializeSecurity** memorizza nella cache i risultati dei controlli di accesso, l'elenco di controllo di accesso non deve essere modificato dopo aver chiamato **CoInitializeSecurity**.

Un altro tipo di valore che è possibile passare al parametro *PVOID* è un puntatore a un GUID, ovvero l'AppID dell'applicazione. Se *PVOID* è un puntatore a un AppID, è necessario specificare EOAC \_ AppID nel parametro *pCapabilities* in modo che la funzione sappia quale valore prevedere in *PVOID*. Se *PVOID* punta a un AppID, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) usa solo il registro di sistema per i valori di autenticazione e ignora tutti gli altri parametri in **CoInitializeSecurity**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza Process-Wide](setting-processwide-security.md)
</dt> </dl>

 

 