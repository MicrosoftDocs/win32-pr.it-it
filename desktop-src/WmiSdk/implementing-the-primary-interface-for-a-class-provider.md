---
description: "Esistono due modi per implementare un provider di classi: implementare l'interfaccia come provider push o come provider di pull."
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ef1b31e1228b832e4d23945f3af0c4df223ddd3edebdd1ec6e34e0e0e8d449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030441"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>Implementazione dell'interfaccia primaria per un provider di classi

Esistono due modi per implementare un provider di classi: implementare l'interfaccia come provider push o come provider di pull.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Implementazione dell'interfaccia primaria per un provider di classi push](#implementing-the-primary-interface-for-a-push-class-provider)
-   [Implementazione dell'interfaccia primaria per un provider di classi pull](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>Implementazione dell'interfaccia primaria per un provider di classi push

Mentre tutti i provider [**implementano IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) per l'inizializzazione e almeno un'altra interfaccia come interfaccia primaria, un provider push implementa solo **IWbemProviderInit.**

Assicurarsi che l'implementazione esegua le attività seguenti:

-   Recupera i dati della classe appropriati.
-   Inserisce i dati nel repository WMI.
-   Elimina i dati obsoleti.

Dopo aver completato il processo di inizializzazione, WMI gestisce tutte le richieste dell'applicazione per le classi appartenenti al provider di push senza ulteriori interazioni con il provider. In seguito, il provider di push funge effettivamente da client di WMI anziché da provider. Per altre informazioni sull'implementazione [**di IWbemProviderInit,**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)vedere [Inizializzazione di un provider.](initializing-a-provider.md)

> [!Note]  
> Quando si chiama WMI per creare, aggiornare o rimuovere dati in un provider push, impostare il parametro *lFlags* in modo da includere il flag **WBEM \_ FLAG OWNER \_ \_ UPDATE** in tutte le chiamate ai metodi [**IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>Implementazione dell'interfaccia primaria per un provider di classi pull

Un provider di pull di classi deve [**implementare IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) come interfaccia primaria. **L'interfaccia IWbemServices** supporta il recupero, l'aggiornamento dei dati, la rimozione dei dati, l'enumerazione e l'elaborazione delle query. Tuttavia, poiché **IWbemServices** viene usato anche da applicazioni e provider per richiedere servizi di WMI, **IWbemServices** contiene molti metodi irrilevanti per un provider di classi. L'implementazione deve supportare il recupero e l'enumerazione delle classi, rispettivamente tramite i metodi [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) Nella tabella seguente sono elencati i metodi **IWbemServices** asincroni aggiuntivi che è possibile implementare per un provider di classi.



| Metodo                                                     | Funzionalità      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | Modifica |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | Eliminazione     |



 

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile usare la comunicazione semisincrono anziché asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

Il provider di classi deve fornire un'implementazione stub che restituisce **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** per tutti gli altri metodi [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) che non supportano il set di funzionalità. In particolare, WMI non supporta l'elaborazione delle query per i provider di classi. Di conseguenza, un provider di classi deve restituire **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** dall'implementazione di [**IWbemServices::ExecQueryAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)impostare la proprietà di registrazione **QuerySupportLevels** su **NULL** o su entrambi.

Le interfacce implementate da un provider di classi sono molto simili alle interfacce per un provider di istanze e un provider di metodi. In realtà, un singolo provider può fungere da tutti e tre i tipi di provider implementando tutti i metodi e registrando correttamente.

 

 



