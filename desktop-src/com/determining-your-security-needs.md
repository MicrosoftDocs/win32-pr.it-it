---
title: Determinazione delle esigenze di sicurezza
description: La modalità di configurazione della sicurezza COM per l'applicazione dipende dal tipo di sicurezza necessario per l'applicazione. Esistono diverse situazioni comuni che determinano le operazioni da eseguire.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57ccbbc8fc96b7c94e90fd3925dfb2ffff07225c34ebe1da34353f42b08b3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993231"
---
# <a name="determining-your-security-needs"></a>Determinazione delle esigenze di sicurezza

La modalità di configurazione della sicurezza COM per l'applicazione dipende dal tipo di sicurezza necessario per l'applicazione. Esistono diverse situazioni comuni che determinano le operazioni da eseguire.

Se si decide di usare le impostazioni predefinite per la sicurezza COM, non è necessario eseguire alcun'operazione. Per informazioni su queste impostazioni predefinite, vedere [Impostazioni predefinite per la sicurezza COM.](com-security-defaults.md)

È anche possibile impedire qualsiasi chiamata remota nel computer disabilitando completamente DCOM (COM tra computer remoti). Per altre informazioni, vedere [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Per le applicazioni legacy o nuove, è possibile impostare la sicurezza a livello di processo nel Registro di sistema. Per altre informazioni, vedere [Impostazione della sicurezza a livello di processo tramite il Registro di sistema.](setting-processwide-security-through-the-registry.md)

È anche possibile eseguire l'override delle impostazioni di sicurezza predefinite per le chiamate a determinate interfacce durante il processo durante l'impostazione della sicurezza predefinita per il resto del processo (per consentire a COM di gestire i casi generali). Per altre informazioni, vedere [Impostazione della sicurezza a livello di proxy di interfaccia.](setting-security-at-the-interface-proxy-level.md)

Per requisiti di sicurezza complessi, è possibile gestire tutta la sicurezza a livello di codice anziché consentire a COM di gestirla. A tale scopo, chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per disabilitare l'autenticazione automatica e quindi controllare tutte le impostazioni di sicurezza impostando la sicurezza in base al proxy per interfaccia. Per altre informazioni, vedere Impostazione della sicurezza a livello di processo [con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) e [Impostazione della sicurezza a livello di proxy di interfaccia.](setting-security-at-the-interface-proxy-level.md)

In alcuni scenari può essere necessario disattivare completamente la sicurezza. È possibile decidere che l'applicazione non richiede alcuna sicurezza oppure disabilitare la sicurezza in fase di sviluppo in modo da abilitare singolarmente le funzionalità di sicurezza. Per informazioni su come disabilitare la sicurezza COM, vedere [Disattivazione della sicurezza.](turning-off-security.md)

La sicurezza in COM si basa sui servizi di autenticazione amministrati dai pacchetti di sicurezza. NTLMSSP funziona bene per molte applicazioni, ma non offre la sicurezza più affidabile offerta da altri pacchetti. Com supporta quindi il pacchetto di sicurezza Schannel e il protocollo di sicurezza Kerberos v5. Per altre informazioni sull'uso di questi pacchetti di sicurezza, vedere [COM e Pacchetti di sicurezza.](com-and-security-packages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




