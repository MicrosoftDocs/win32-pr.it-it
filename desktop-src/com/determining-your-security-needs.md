---
title: Determinazione delle esigenze di sicurezza
description: La modalità di configurazione della sicurezza COM per l'applicazione dipende dal tipo di sicurezza necessario per l'applicazione. Esistono diverse situazioni comuni che determinano le operazioni da eseguire.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714434"
---
# <a name="determining-your-security-needs"></a>Determinazione delle esigenze di sicurezza

La modalità di configurazione della sicurezza COM per l'applicazione dipende dal tipo di sicurezza necessario per l'applicazione. Esistono diverse situazioni comuni che determinano le operazioni da eseguire.

Se si decide di utilizzare le impostazioni predefinite di sicurezza COM, non è necessario eseguire anythingâ. Per informazioni sulle impostazioni predefinite, vedere [valori predefiniti di sicurezza com](com-security-defaults.md).

È anche possibile impedire qualsiasi chiamata remota nel computer disabilitando completamente DCOM (COM tra computer remoti). Per ulteriori informazioni, vedere [impostazione di System-Wide sicurezza tramite DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Per le applicazioni legacy o nuove, è possibile impostare la sicurezza a livello di processo nel registro di sistema. Per ulteriori informazioni, vedere [impostazione della sicurezza Processwide tramite il registro di sistema](setting-processwide-security-through-the-registry.md).

È anche possibile eseguire l'override delle impostazioni di sicurezza predefinite per le chiamate a determinate interfacce nel processo, impostando la sicurezza predefinita per la parte restante del processo, in modo da consentire a COM di gestire i casi generali. Per ulteriori informazioni, vedere [impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).

Per i requisiti di sicurezza complessi, è possibile gestire tutta la sicurezza a livello di codice anziché consentire a COM di gestirla. A tale scopo, chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per disabilitare l'autenticazione automatica e quindi controllare tutte le impostazioni di sicurezza impostando la sicurezza in base al proxy per interfaccia. Per altre informazioni, vedere [impostazione della sicurezza Processwide con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) e [impostazione della sicurezza a livello di proxy di interfaccia](setting-security-at-the-interface-proxy-level.md).

In alcuni scenari potrebbe essere necessario disattivare completamente la protezione. Si potrebbe decidere che l'applicazione non necessita di alcuna sicurezza oppure è possibile disabilitare la sicurezza durante il tempo di sviluppo, in modo da poter abilitare le funzionalità di sicurezza singolarmente. Per informazioni su come disabilitare la sicurezza COM, [vedere Disattivazione della sicurezza.](turning-off-security.md)

La sicurezza in COM si basa sui servizi di autenticazione amministrati dai pacchetti di sicurezza. NTLMSSP funziona bene per molte applicazioni, ma non offre una sicurezza più affidabile offerta da altri pacchetti. Pertanto, COM supporta il pacchetto di sicurezza Schannel e il protocollo di sicurezza Kerberos V5. Per altri dettagli sull'uso di questi pacchetti di sicurezza, vedere [pacchetti com e di sicurezza](com-and-security-packages.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




