---
description: Una delle prime attività che è necessario codificare per un provider è il processo di inizializzazione, che copre tutte le attività che il provider deve eseguire che consente di inviare e ricevere informazioni da WMI, controllare un oggetto gestito ed eseguire altre attività.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Inizializzazione di un provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e373cf72d4715919a9d7fc59064d156e80a1f2371c585d698a7c6edff4f22fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097281"
---
# <a name="initializing-a-provider"></a>Inizializzazione di un provider

Una delle prime attività che è necessario codificare per un provider è il processo di inizializzazione, che copre tutte le attività che il provider deve eseguire che consente di inviare e ricevere informazioni da WMI, controllare un oggetto gestito ed eseguire altre attività. Ogni tipo di provider ha un set diverso di attività che deve eseguire e ha un set di interfacce univoche.

Tuttavia, tutti i provider vengono inizializzati tramite [**l'interfaccia IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) e informano WMI del relativo stato di inizializzazione tramite l'interfaccia [**IWbemProviderInitSink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink)

La procedura seguente descrive come inizializzare un provider.

**Per inizializzare un provider**

1.  Implementare [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) per il provider.

    Quando WMI determina che un client richiede i servizi di un provider, WMI carica il provider chiamando il [**metodo IWbemProviderInit::Initialize.**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)

2.  Implementare qualsiasi interfaccia univoca per il tipo di provider.
3.  Informare WMI che il provider è stato completato con l'inizializzazione chiamando [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).

    Tutte le implementazioni di [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) devono chiamare [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) per segnalare lo stato di inizializzazione a WMI. Il **metodo SetStatus** consente a WMI di determinare se un provider è pronto per ricevere richieste e il tipo di richieste che il provider è pronto per ricevere.

La procedura seguente descrive come segnalare un'inizializzazione riuscita.

**Per segnalare l'esito positivo dell'inizializzazione**

-   Impostare il *parametro IStatus* di [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) su **WBEM \_ S \_ INITIALIZED**.

    Se si restituisce **WBEM \_ S \_ INITIALIZED,** un provider indica la conformità alla gestione delle richieste da applicazioni, WMI e altri provider. Dopo aver ricevuto WBEM S INITIALIZED, WMI esegue una chiamata al metodo \_ \_ [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) nel provider. Questa query recupera un puntatore all'interfaccia primaria del provider.

La procedura seguente descrive come segnalare un errore durante l'inizializzazione.

**Per segnalare un errore durante l'inizializzazione**

-   Impostare il *parametro IStatus* di [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) su **WBEM \_ E \_ FAILED**. Wmi visualizza i provider che **restituiscono WBEM \_ E \_ FAILED** come non funzionante.

    WMI rilascia il [**puntatore IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) dopo che WMI ha ottenuto un puntatore all'interfaccia primaria del provider o dopo che l'inizializzazione ha avuto esito negativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di un provider WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Impostazione dei descrittori di sicurezza di Namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protezione del provider](securing-your-provider.md)
</dt> </dl>

 

 



