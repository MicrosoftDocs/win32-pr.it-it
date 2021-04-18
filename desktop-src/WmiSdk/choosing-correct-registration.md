---
description: WMI supporta diversi modelli di threading a seconda della modalità di hosting del provider e del tipo di funzionalità del provider, ad esempio la classe o la proprietà.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Scelta della registrazione corretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313201"
---
# <a name="choosing-correct-registration"></a>Scelta della registrazione corretta

WMI supporta diversi modelli di threading a seconda della modalità di hosting del provider e del tipo di funzionalità del provider, ad esempio la [classe](writing-a-class-provider.md) o la [Proprietà](writing-a-property-provider.md). I [*provider disaccoppiati*](gloss-d.md) , ad esempio, non supportano tutti i tipi di funzionalità del provider. Per altre informazioni sui diversi modelli di hosting e su come configurarli, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

## <a name="in-process-providers"></a>Provider di In-Process

I provider in-process vengono eseguiti in un processo host condiviso Wmiprvse.exe. La maggior parte dei tipi di provider in-process utilizza il modello di Apartment a thread multipli (MTA).

Il modello MTA è supportato per i seguenti tipi di funzionalità del provider:

-   [Provider di classi](writing-a-class-provider.md)
-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di proprietà](writing-a-property-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

Il modello di Apartment a thread singolo (STA) è supportato per alcuni tipi di funzionalità del provider:

-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Provider out-of-process

I provider ospitati in un altro host del servizio condiviso supportano le funzionalità del provider seguenti:

-   [Provider di classi](writing-a-class-provider.md)
-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di proprietà](writing-a-property-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

Per ulteriori informazioni sugli host dei servizi condivisi, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

## <a name="decoupled-providers"></a>Provider disaccoppiati

I provider disaccoppiati sono ospitati in un'applicazione. Per ulteriori informazioni, vedere [incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md). I provider creati utilizzando WMI nel .NET Framework sono disaccoppiati. I provider disaccoppiati supportano le funzionalità del provider seguenti:

-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hosting e sicurezza del provider](provider-hosting-and-security.md)
</dt> </dl>

 

 



