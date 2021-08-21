---
description: È possibile impedire a utenti non autorizzati di ricevere eventi a cui non devono avere accesso.
ms.assetid: 59788643-f57d-458f-91ab-26552218523b
ms.tgt_platform: multiple
title: Fornire eventi in modo sicuro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e485f0c4d7610be9908155b6f20c315d53b8358f0e0c5c9baff244d2399b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992651"
---
# <a name="providing-events-securely"></a>Fornire eventi in modo sicuro

È possibile impedire a utenti non autorizzati di ricevere eventi a cui non devono avere accesso. Il provider di eventi può fornire istanze delle [](/previous-versions/windows/desktop/regprov/system-registry-provider) proprie classi di evento, proprio come il provider del Registro di sistema fornisce classi come [**RegistryKeyChangeEvent.**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) Il provider di eventi può anche recapitare eventi intrinseci, ad [**\_ \_ esempio InstanceCreationEvent.**](--instancecreationevent.md) Per altre informazioni, vedere [Scrittura di un provider di eventi.](writing-an-event-provider.md)

Un provider di eventi può controllare l'accesso ai destinatari degli eventi nei modi seguenti:

-   L'uso del controllo di accesso [**mediante l'implementazione di IWbemEventProviderSecurity::AccessCheck**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) è il modo più efficiente.

    Il provider determina se il consumer dispone dei privilegi per ricevere un evento richiesto. Se il consumer non dispone di privilegi sufficienti per la registrazione, WMI restituisce un errore di accesso negato. Utilizzare questa modalità quando il provider può decidere chi può ricevere eventi. Ad esempio, un provider può fornire eventi correlati alla sicurezza e può richiedere che il consumer abbia privilegi di amministratore con il privilegio **SeSecurityPrivilege** abilitato.

-   L'implementazione di [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) nel sink usato per generare eventi consente l'impostazione di un descrittore di sicurezza (SD) in un sink per tutti gli eventi che passano.

    WMI esegue i controlli di accesso in base alla DS. Usare questa modalità quando il provider non può prendere la decisione relativa a chi è autorizzato a utilizzare i propri eventi, ma può decidere una DS per un sink specifico. Ad esempio, usare [**IWbemEventSink::SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) se il provider di eventi ha ottenuto diversi sink tramite chiamate a [**IWbemEventSink::GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink) e si vuole un descrittore di sicurezza per ogni sink.

-   **L'impostazione della proprietà SECURITY \_ DESCRIPTOR** di un evento consente l'impostazione di una DS per ogni evento.

    Usare questo approccio quando ogni evento recapitato al sink può avere descrittori di sicurezza diversi. Per usare questo approccio, derivare una delle classi di eventi estensivi definite dal provider da [**\_ \_ Event**](--event.md) o [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) in modo che la classe contenga la proprietà **SECURITY \_ DESCRIPTOR.** Ad esempio, il provider di eventi può pubblicare eventi normali e sicuri tramite un sink. In questo caso, usare il descrittore di sicurezza dell'account Administrators per gli eventi protetti e un descrittore di sicurezza **NULL** per gli eventi normali che possono essere ricevuti da chiunque.

## <a name="securing-events-by-decoupled-event-providers"></a>Protezione degli eventi tramite provider di eventi disaccoccodati

I provider di eventi disaccoccodati differiscono dai provider di eventi non dichiarati per la modalità di registrazione in WMI. La chiamata a [**IWbemEventProviderSecurity::AccessCheck**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovidersecurity-accesscheck) per gli eventi da un provider disaccoccodato non propaga mai il token di accesso client. WMI gestisce il controllo di accesso come per i provider di eventi non dichiarati. Per altre informazioni sulla scrittura di un provider disaccoccodato, vedere [Incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md).

Solo gli amministratori con **il \_ privilegio FULL WRITE** impostato in Controllo **WMI** Pannello di controllo **possono** generare eventi per uno spazio dei nomi. Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi con il controllo WMI.](setting-namespace-security-with-the-wmi-control.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Protezione degli eventi WMI](securing-wmi-events.md)
</dt> </dl>

 

 
