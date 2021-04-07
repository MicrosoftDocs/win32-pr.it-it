---
description: Una delle prime attività che è necessario scrivere per un provider è il processo di inizializzazione, che include tutte le attività che il provider deve eseguire, che consente di inviare e ricevere informazioni da WMI, controllare un oggetto gestito ed eseguire altre attività.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inizializzazione di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885394"
---
# <a name="initializing-a-provider"></a>Inizializzazione di un provider

Una delle prime attività che è necessario scrivere per un provider è il processo di inizializzazione, che include tutte le attività che il provider deve eseguire, che consente di inviare e ricevere informazioni da WMI, controllare un oggetto gestito ed eseguire altre attività. Ogni tipo di provider dispone di un set diverso di attività che deve eseguire e dispone di un set di interfacce univoche associato.

Tuttavia, tutti i provider vengono inizializzati tramite l'interfaccia [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e indicano a WMI lo stato di inizializzazione tramite l'interfaccia [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .

Nella procedura riportata di seguito viene descritto come inizializzare un provider.

**Per inizializzare un provider**

1.  Implementare [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) per il provider.

    Quando WMI stabilisce che un client richiede i servizi di un provider, WMI carica il provider chiamando il metodo [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .

2.  Implementare qualsiasi interfaccia univoca per il tipo di provider.
3.  Informare WMI che il provider è terminato con l'inizializzazione chiamando [**IWbemProviderInitSink:: sestato**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).

    Tutte le implementazioni di [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) devono chiamare [**IWbemProviderInitSink:: sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) per segnalare lo stato di inizializzazione a WMI. Il metodo **sestatus** consente a WMI di determinare se un provider è pronto a ricevere le richieste e il tipo di richieste che il provider è pronto a ricevere.

Nella procedura riportata di seguito viene descritto come segnalare un'inizializzazione riuscita.

**Per segnalare una corretta inizializzazione**

-   Impostare il parametro *istatus* di [**sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) su **WBEM \_ S \_ Initialized**.

    Restituendo **l' \_ \_ inizializzazione di WBEM**, un provider indica una preparazione per la gestione delle richieste provenienti da applicazioni, WMI e altri provider. Dopo la ricezione \_ di WBEM S \_ Initialized, WMI effettua una chiamata al metodo [**IWbemProviderInit:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) nel provider. Questa query recupera un puntatore all'interfaccia principale del provider.

Nella procedura riportata di seguito viene descritto come segnalare un errore durante l'inizializzazione.

**Per segnalare un errore durante l'inizializzazione**

-   Impostare il parametro *istatus* di [**sestatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) su **WBEM \_ E \_ failed**. I provider di viste WMI che restituiscono **WBEM E non sono \_ \_ riusciti** a funzionare.

    WMI rilascia il puntatore [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) dopo che WMI ha ottenuto un puntatore all'interfaccia principale del provider o dopo che l'inizializzazione non è riuscita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sicurezza del provider](securing-your-provider.md)
</dt> </dl>

 

 



