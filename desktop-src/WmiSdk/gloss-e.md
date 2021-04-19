---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd162feb3936712b396db016de036f78aea35a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317556"
---
# <a name="e-wmi"></a>E (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [d](gloss-d.md) E [F](gloss-f.md) G [H](gloss-h.md) [i](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**classe di evento**
</dt> <dd>

Classe WMI che *i consumer di eventi* possono sottoscrivere da una *query di eventi*. La classe segnala un tipo di occorrenza specifico. Ad esempio, la classe [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) segnala che un processo specifico è stato interrotto.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**consumer di eventi**
</dt> <dd>

Destinatario delle notifiche che segnalano il verificarsi di un evento. Un consumer di eventi può essere [*temporaneo*](gloss-t.md) o [*permanente*](gloss-p.md).

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**provider di consumer di eventi**
</dt> <dd>

Provider che determina il consumer di eventi permanente che gestisce un dato evento. Un provider di consumer di eventi viene registrato con WMI da un'istanza di [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md), che contiene un elenco delle classi di [*consumer logiche*](gloss-l.md) supportate dal provider di consumer di eventi. Un provider di consumer di eventi è un server COM che esegue il mapping di [*consumer fisici*](gloss-p.md) a *utenti logici*. Un provider di consumer di eventi supporta l'interfaccia [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) ed è un componente dell'architettura del consumer permanente.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**filtro eventi**
</dt> <dd>

Istanza della classe di sistema [**\_ \_ EventFilter**](--eventfilter.md) che descrive un tipo di evento e le condizioni per il recapito di una notifica. Un consumer utilizza un filtro eventi per eseguire la registrazione per ricevere la notifica di un tipo specifico di evento.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**provider di eventi**
</dt> <dd>

Provider WMI che monitora un'origine di eventi e notifica a WMI quando si verificano gli eventi. Un provider di eventi implementa le interfacce [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) e talvolta [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**query di eventi**
</dt> <dd>

Istruzione [*WMI Query Language*](gloss-w.md) utilizzata dai consumer di eventi per la registrazione per la ricezione di notifiche di eventi specifici. Un provider di eventi utilizza una query di eventi per eseguire la registrazione per generare notifiche di specifici eventi.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**schema estensione**
</dt> <dd>

Terzo livello dello [*schema CIM*](gloss-c.md), che include le estensioni specifiche della piattaforma dello schema CIM, ad esempio Windows, UNIX ed Exchange Server. Vedere anche modello [*comune*](gloss-c.md) e modello di base.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**evento estrinseco**
</dt> <dd>

Notifica degli eventi da un provider. La maggior parte dei provider crea un'istanza di una classe di evento definita nei file MOF del provider. Un evento estrinseco eredita da [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md). Il [provider del registro eventi](/previous-versions/windows/desktop/eventlogprov/event-log-provider) , ad esempio, definisce la classe di evento [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Vedere anche [*evento intrinseco*](gloss-i.md).

</dd> </dl>

 

 
