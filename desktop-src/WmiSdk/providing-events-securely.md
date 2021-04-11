---
description: È possibile impedire a utenti non autorizzati di ricevere eventi a cui non dovrebbero avere accesso.
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: Fornire eventi in modo sicuro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2c92ed1de08dde4891365440f559544a0b26de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232904"
---
# <a name="providing-events-securely"></a>Fornire eventi in modo sicuro

È possibile impedire a utenti non autorizzati di ricevere eventi a cui non dovrebbero avere accesso. Il provider di eventi può fornire istanze delle proprie classi di evento, proprio come il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) fornisce classi quali [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Il provider di eventi può anche recapitare eventi intrinseci, ad esempio [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md). Per ulteriori informazioni, vedere [scrittura di un provider di eventi](writing-an-event-provider.md).

Un provider di eventi può controllare l'accesso ai destinatari di eventi nei modi seguenti:

-   L'uso del controllo di accesso mediante l'implementazione di [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) è il modo più efficiente.

    Il provider determina se il consumer dispone dei privilegi necessari per ricevere un evento richiesto. Se il consumer non dispone di privilegi sufficienti per la registrazione, WMI restituisce un errore di accesso negato. Usare questa modalità quando il provider può decidere chi può ricevere eventi. Ad esempio, un provider può fornire eventi correlati alla sicurezza e può richiedere che il consumer disponga dei privilegi di amministratore con il privilegio **SeSecurityPrivilege** abilitato.

-   L'implementazione di [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) sul sink usato per generare eventi consente l'impostazione di un descrittore di sicurezza (SD) su un sink per tutti gli eventi che passano.

    WMI esegue controlli di accesso basati su SD. Usare questa modalità quando il provider non è in grado di prendere decisioni in merito a chi è autorizzato a utilizzare gli eventi, ma può scegliere una SD per un sink specifico. Usare, ad esempio, [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) se il provider di eventi ha ottenuto diversi sink mediante chiamate a [**IWbemEventSink:: GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) e si desidera un descrittore di sicurezza per ogni sink.

-   L'impostazione della proprietà del **\_ descrittore di sicurezza** di un evento consente l'impostazione di una SD per ogni evento.

    Utilizzare questo approccio quando ogni evento recapitato al sink può disporre di descrittori di sicurezza diversi. Per usare questo approccio, derivare qualsiasi classe di evento estrinseca definita dal provider da [**\_ \_ Event**](--event.md) o [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) in modo che la classe contenga la proprietà del **\_ descrittore di sicurezza** . Il provider di eventi, ad esempio, può pubblicare eventi sia sicuri che normali tramite un sink. In questo caso, usare il descrittore di sicurezza dell'account Administrators per gli eventi sicuri e un descrittore di sicurezza **null** per gli eventi normali che possono essere ricevuti da chiunque.

## <a name="securing-events-by-decoupled-event-providers"></a>Sicurezza degli eventi per provider di eventi separati

I provider di eventi disaccoppiati differiscono dai provider di eventi nondecoupled nel modo in cui si registrano con WMI. La chiamata a [**IWbemEventProviderSecurity:: AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) per gli eventi da un provider disaccoppiato non propaga mai il token di accesso client. WMI gestisce il controllo di accesso in modo analogo ai provider di eventi nondecoupled. Per ulteriori informazioni sulla scrittura di un provider disaccoppiato, vedere [incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md).

Solo gli amministratori con i privilegi di **\_ scrittura completi** impostati nel **controllo WMI** del **Pannello di controllo** possono generare eventi per uno spazio dei nomi. Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> </dl>

 

 
