---
description: Per i componenti configurati in esecuzione all'interno di applicazioni COM+, i contesti rappresentano la base in cui vengono forniti i servizi COM+.
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: Contesti COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0ae1228f89797f9124e817db07f11a23dbec12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401489"
---
# <a name="com-contexts"></a>Contesti COM+

Per i componenti configurati in esecuzione all'interno di applicazioni COM+, i *contesti* rappresentano la base in cui vengono forniti i servizi com+. In COM+ un contesto viene definito come set di proprietà di runtime associate a uno o più oggetti COM utilizzati per fornire servizi per tali oggetti.

In COM+ ogni oggetto COM è associato esattamente a un contesto in cui viene eseguito, ovvero tra l'attivazione e la disattivazione, e ogni contesto risiede all'interno di un solo apartment COM. Più oggetti possono essere eseguiti nello stesso contesto e più contesti possono trovarsi all'interno dello stesso Apartment. Inizializzata quando un oggetto viene attivato, le proprietà di contesto, ad esempio le proprietà del contesto di sicurezza, rappresentano le esigenze di runtime di un oggetto.

> [!Note]  
> Per i componenti non configurati che non utilizzano servizi COM+, il contesto è, nella maggior parte dei casi, ignorato.

 

COM+ utilizza le proprietà di contesto come base per la fornitura di servizi in fase di esecuzione. Queste proprietà contengono lo stato che determina il modo in cui l'ambiente di esecuzione esegue i servizi per gli oggetti all'interno del contesto. In alcuni casi, è possibile interagire direttamente con le proprietà di contesto di un oggetto per indicare uno stato pertinente per un servizio fornito per l'oggetto. Questa operazione può essere eseguita, ad esempio, quando un oggetto che partecipa a una transazione automatica Vota il risultato della transazione.

Per una descrizione dettagliata dei concetti di base di questi concetti, vedere [processi, thread e Apartment](/windows/desktop/com/processes--threads--and-apartments).

## <a name="programmatic-interaction-with-context-properties"></a>Interazione a livello di codice con le proprietà di contesto

A ogni contesto è associato un oggetto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) che tiene traccia delle relative proprietà. È possibile accedere a **ObjectContext** chiamando la funzione [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext) . Dopo aver eseguito l'accesso a **ObjectContext**, è possibile chiamare i metodi sull'interfaccia [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) che espone per modificare le proprietà di contesto.

Ad esempio, la chiamata di [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ha l'effetto di impostare il bit di coerenza della transazione su "coerente" e il bit di [attivazione JIT](com--just-in-time-activation.md) su "Done" nel contesto associato all'oggetto. "Coerente" segnala a COM+ che si vota per eseguire il commit della transazione e "Done" indica che l'oggetto è pronto per essere disattivato quando il metodo restituisce.

Oltre a [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext), altre interfacce specializzate che forniscono accesso alle proprietà di contesto sono [**IObjectContextInfo**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo), [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)e [**IObjectContextActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity). A un certo punto, [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) accede anche alle proprietà di contesto. È possibile usare [**IGetSecurityCallContext:: GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) per ottenere **ISecurityCallContext**.

## <a name="understanding-activation-and-interception"></a>Informazioni sull'attivazione e l'intercettazione

In genere, è necessario considerare il contesto solo nella misura in cui rappresenta un certo numero di proprietà, alcune delle quali è possibile impostare o ottenere, utilizzate per fornire servizi COM+ per i componenti. In alcune circostanze, tuttavia, potrebbe essere necessario considerare in modo più dettagliato i due facet correlati seguenti di contesti:

-   [Attivazione del contesto](context-activation.md)o inizializzazione di un oggetto in un contesto appropriato.
-   [Intercettazione](interception-of-cross-context-calls.md)o operazione eseguita da com+ sulle chiamate attraverso un limite del contesto.

## <a name="relation-to-mts-context-wrappers"></a>Relazione ai wrapper del contesto MTS

I contesti sostituiscono in modo efficace i wrapper del contesto MTS. Lo scopo che ha servito, ovvero fornire servizi automatici tramite l'intercettazione delle richieste di creazione, è ora una funzionalità integrata di COM+. Di conseguenza, non è più necessario usare la funzione [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) . In MTS è stato usato **SafeRef** per ottenere un riferimento all'oggetto che può essere passato all'esterno del relativo wrapper di contesto. In COM+ questa operazione non è necessaria. i riferimenti agli oggetti normali (**questo** puntatori) funzionano.

 

 
