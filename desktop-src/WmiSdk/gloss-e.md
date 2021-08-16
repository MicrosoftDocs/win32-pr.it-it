---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd1ce4685ee9901dfedca2a4b3a1b948d91c8f5b56def28494eb6c4c63e726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319220"
---
# <a name="e-wmi"></a>E (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) T [U](gloss-t.md) V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**classe di evento**
</dt> <dd>

Classe WMI che i *consumer di eventi possono* sottoscrivere tramite una query di *eventi*. La classe segnala un tipo specifico di occorrenza. Ad esempio, la [**classe Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) segnala che un processo specifico è stato arrestato.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consumer di eventi**
</dt> <dd>

Destinatario delle notifiche che segnalano il verificarsi di un evento. Un consumer di eventi è [*temporaneo*](gloss-t.md) o [*permanente.*](gloss-p.md)

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**provider di consumer di eventi**
</dt> <dd>

Provider che determina il consumer di eventi permanente che gestisce un dato evento. Un provider di consumer di eventi viene registrato con WMI da un'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), che contiene un elenco delle classi [*consumer*](gloss-l.md) logiche supportate dal provider di consumer di eventi. Un provider di consumer di eventi è un server COM che esegue il mapping [*dei consumer fisici*](gloss-p.md) ai consumer *logici*. Un provider di consumer di eventi supporta [**l'interfaccia IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) ed è un componente dell'architettura consumer permanente.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtro eventi**
</dt> <dd>

Istanza della classe di [**\_ \_ sistema EventFilter**](--eventfilter.md) che descrive un tipo di evento e le condizioni per il recapito di una notifica. Un consumer usa un filtro eventi per registrarsi per ricevere la notifica di un tipo specifico di evento.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**provider di eventi**
</dt> <dd>

Provider WMI che monitora un'origine di eventi e invia una notifica a WMI quando si verificano eventi. Un provider di eventi implementa [**le interfacce IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) e talvolta [**IWbemEventProviderQuerySink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink)

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**query di eventi**
</dt> <dd>

Istruzione [*WMI Query Language*](gloss-w.md) che i consumer di eventi usano per registrarsi per ricevere la notifica di eventi specifici. Un provider di eventi utilizza una query di eventi per eseguire la registrazione per generare notifiche di specifici eventi.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**schema di estensione**
</dt> <dd>

Terzo livello dello [*schema CIM,*](gloss-c.md)che include estensioni specifiche della piattaforma dello schema CIM, ad esempio Windows, UNIX e Exchange Server. Vedere anche [*modello comune e*](gloss-c.md) modello di base.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**evento estrinsic**
</dt> <dd>

Notifica di eventi da un provider. La maggior parte dei provider crea un'istanza di una classe di evento definita nei file MOF del provider. Un evento etrinsic eredita da [**\_ \_ ExtrinsicEvent.**](--extrinsicevent.md) Ad esempio, il [provider del registro eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider) definisce la classe di evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Vedere anche [*evento intrinseco*](gloss-i.md).

</dd> </dl>

 

 
