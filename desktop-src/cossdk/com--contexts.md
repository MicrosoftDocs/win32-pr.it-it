---
description: Per i componenti configurati in esecuzione all'interno di applicazioni COM+, i contesti sono la base su cui vengono forniti i servizi COM+.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: Contesti COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c48e2fb9a118bff5fe4d6590ff859f0f053ab29687d4f4a2a070d44af37b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730651"
---
# <a name="com-contexts"></a>Contesti COM+

Per i componenti configurati in  esecuzione all'interno di applicazioni COM+, i contesti sono la base su cui vengono forniti i servizi COM+. In COM+, un contesto è definito come set di proprietà di run-time associate a uno o più oggetti COM utilizzati per fornire servizi per tali oggetti.

In COM+, ogni oggetto COM è associato esattamente a un contesto durante l'esecuzione (ovvero tra l'attivazione e la disattivazione) e ogni contesto risiede esattamente all'interno di un apartment COM. Più oggetti possono essere eseguiti all'interno dello stesso contesto e più contesti possono risiedere all'interno dello stesso apartment. Inizializzato quando viene attivato un oggetto , le proprietà di contesto, ad esempio le proprietà del contesto di sicurezza, rappresentano le esigenze di run-time di un oggetto.

> [!Note]  
> Per i componenti non configurati che non usano servizi COM+, il contesto viene, nella maggior parte dei casi, ignorato.

 

COM+ usa le proprietà di contesto come base per fornire servizi di run-time. Queste proprietà contengono lo stato che determina come l'ambiente di esecuzione esegue i servizi per gli oggetti all'interno del contesto. In alcuni casi, è possibile interagire direttamente con le proprietà di contesto di un oggetto per indicare uno stato rilevante per un servizio fornito per l'oggetto. Ad esempio, questa operazione viene eseguito quando un oggetto che partecipa a una transazione automatica vota il risultato della transazione.

Per una descrizione dettagliata della base COM di questi concetti, vedere [Processi, thread e apartment.](/windows/desktop/com/processes--threads--and-apartments)

## <a name="programmatic-interaction-with-context-properties"></a>Interazione a livello di codice con le proprietà di contesto

A ogni contesto è associato [**un oggetto ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) che tiene traccia delle relative proprietà. È possibile accedere **a ObjectContext** chiamando la [**funzione GetObjectContext.**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) Dopo aver eseguito **l'accesso a ObjectContext,** è possibile chiamare i metodi sull'interfaccia [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) che espone per modificare le proprietà di contesto.

Ad esempio, la chiamata [**a IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ha l'effetto di impostare il bit di coerenza della transazione su "coerente" e il bit eseguito dall'attivazione [JIT](com--just-in-time-activation.md) su "done" nel contesto associato all'oggetto. "Consistent" segnala a COM+ che si vota per eseguire il commit della transazione e "done" indica che l'oggetto è pronto per essere disattivato quando il metodo viene restituito.

Oltre a [**IObjectContext,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)altre interfacce specializzate che forniscono l'accesso alle proprietà di contesto sono [**IObjectContextInfo,**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo) [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)e [**IObjectContextActivity.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity) In una certa misura, [**anche ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) accede alle proprietà di contesto. È possibile usare [**IGetSecurityCallContext::GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) per ottenere **ISecurityCallContext.**

## <a name="understanding-activation-and-interception"></a>Informazioni su attivazione e intercettazione

In genere, è necessario pensare al contesto solo nella misura in cui rappresenta una serie di proprietà, alcune delle quali è possibile impostare o ottenere, che vengono usate per fornire servizi COM+ per i componenti. In alcuni casi, tuttavia, potrebbe essere necessario prendere in considerazione i due facet di contesti correlati seguenti in modo più dettagliato:

-   [Attivazione del contesto](context-activation.md)o inizializzazione di un oggetto in un contesto appropriato.
-   [Intercettazione](interception-of-cross-context-calls.md)o cosa fa COM+ sulle chiamate attraverso un limite di contesto.

## <a name="relation-to-mts-context-wrappers"></a>Relazione con i wrapper di contesto MTS

I contesti sostituiscono in modo efficace i wrapper di contesto MTS. Lo scopo che hanno fornito, fornendo servizi automatici tramite il trapping delle richieste di creazione, è ora una funzionalità integrata di COM+. Di conseguenza, non è più necessario usare la [**funzione SafeRef.**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) In MTS è stato usato **SafeRef** per ottenere un riferimento all'oggetto che può essere passato all'esterno del relativo wrapper di contesto. In COM+, questa operazione non è necessaria. I riferimenti a oggetti normali **(puntatori** this) funzionano.

 

 
