---
description: WMI supporta modelli di threading diversi a seconda della modalità di hosting del provider e del tipo di funzionalità del provider, ad esempio Classe o Proprietà.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Scelta della registrazione corretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3e9a252e9013e828f5dc2c6e4c7228919d0834d0edb3da5f699cbe0306a38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131803"
---
# <a name="choosing-correct-registration"></a>Scelta della registrazione corretta

WMI supporta modelli di threading diversi a seconda della modalità di hosting del provider e del tipo di funzionalità del provider, ad esempio [Classe](writing-a-class-provider.md) [o Proprietà](writing-a-property-provider.md). Ad esempio, [*i provider disaccoccodati*](gloss-d.md) non supportano tutti i tipi di funzionalità del provider. Per altre informazioni sui diversi modelli di hosting e su come configurarli, vedere [Hosting e sicurezza del provider.](provider-hosting-and-security.md)

## <a name="in-process-providers"></a>In-Process provider

I provider in-process vengono eseguiti in un processo host condiviso, Wmiprvse.exe. La maggior parte dei tipi di provider in-process usa il modello di apartment a thread singolo (MTA).

Il modello MTA è supportato per i tipi di funzionalità del provider seguenti:

-   [Provider di classi](writing-a-class-provider.md)
-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di proprietà](writing-a-property-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

Il modello apartment a thread singolo (STA) è supportato per alcuni tipi di funzionalità del provider:

-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Provider out-of-process

I provider ospitati in un host del servizio condiviso diverso supportano le funzionalità del provider seguenti:

-   [Provider di classi](writing-a-class-provider.md)
-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di proprietà](writing-a-property-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

Per altre informazioni sugli host del servizio condiviso, vedere [Hosting e sicurezza del provider.](provider-hosting-and-security.md)

## <a name="decoupled-providers"></a>Provider disaccoccodati

I provider disaccoccodati sono ospitati in un'applicazione. Per altre informazioni, vedere [Incorporamento di un provider in un'applicazione.](incorporating-a-provider-in-an-application.md) I provider creati usando WMI nel .NET Framework sono disaccoccodati. I provider disaccoccodati supportano le funzionalità del provider seguenti:

-   [Provider di istanze](writing-an-instance-provider.md)
-   [Provider di metodi](writing-a-method-provider.md)
-   [Provider di eventi](writing-an-event-provider.md)
-   [Provider di consumer di eventi](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hosting e sicurezza dei provider](provider-hosting-and-security.md)
</dt> </dl>

 

 



