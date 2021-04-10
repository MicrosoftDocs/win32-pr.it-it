---
description: In COM+ ogni oggetto COM viene creato con un contesto associato.
ms.assetid: e5602af2-5852-4c34-a792-6742e90b7d41
title: Attivazione del contesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a652615d6c1288887085c857817e32e3a3b4081c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127150"
---
# <a name="context-activation"></a>Attivazione del contesto

In COM+ ogni oggetto COM viene creato con un contesto associato. Ciò significa che è necessario creare e inizializzare un nuovo contesto oppure utilizzare un contesto esistente appropriato. Questo processo è noto come *attivazione*. In COM+, un oggetto viene attivato nel proprio contesto o in quello del creatore (un oggetto che ha richiesto l'attivazione dell'oggetto, ad esempio chiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)).

In alcune circostanze, ad esempio con il [pool di oggetti](com--object-pooling.md), un oggetto viene attivato senza essere creato da zero. In questo caso, un'istanza in esecuzione viene attivata all'interno di un contesto. Per tutta la durata, è possibile che venga attivata ripetutamente in contesti diversi.

Il meccanismo di base è lo stesso in entrambi i casi, ovvero un oggetto è associato a un contesto e tale contesto viene inizializzato correttamente per rappresentare le esigenze di run-time dell'oggetto.

## <a name="flowing-of-context-properties"></a>Propagazione delle proprietà di contesto

Quando un oggetto viene attivato in risposta a una richiesta di creazione da un altro oggetto, COM+ deve intermediare tra di essi per attivare correttamente l'oggetto downstream. COM+ deve confrontare il contesto del chiamante con la configurazione del componente chiamato, quindi decidere dove attivare il componente downstream e come inizializzare le proprietà di contesto.

Per individuare la configurazione del componente, COM+ lo cerca nel database di registrazione della classe COM+, ottimizzato per le ricerche in fase di esecuzione estremamente veloci. Questa operazione è determinata dalla configurazione di un componente durante l'installazione in un'applicazione COM+. La configurazione del componente viene quindi esaminata in base allo stato delle proprietà di contesto del chiamante.

In alcuni casi, la configurazione è coerente con il contesto del chiamante e il componente può essere attivato nel contesto del chiamante. Questa situazione può verificarsi solo se il contesto del chiamante soddisfa tutti i requisiti della fase di esecuzione del nuovo oggetto.

Quando il componente downstream non può essere attivato all'interno del contesto del chiamante, viene attivato nel relativo contesto in un Apartment appropriato. In tal caso, è possibile che determinate proprietà di contesto vengano propagate dal chiamante al chiamato. Se, ad esempio, il chiamante è associato a una transazione e il chiamato supporta le transazioni, il nuovo oggetto ottiene il proprio contesto (per votare la transazione, deve disporre di un proprio flag coerente) ed eredita l'ID di transazione e l'ID attività del chiamante (che si trovano all'interno della stessa transazione e del dominio di sincronizzazione).

## <a name="ignored-context-properties"></a>Proprietà di contesto ignorate

A seconda della modalità di configurazione di un componente, alcune proprietà di contesto potrebbero non essere in grado di determinare se è attivata nel contesto del creatore o nel contesto. Ad esempio, le transazioni disabilitate e sincronizzate le impostazioni disabilitate, che indicano la presenza di una transazione o di un dominio di sincronizzazione, non svolgeranno alcun ruolo nell'attivazione del componente. Queste proprietà vengono ignorate in base alla propagazione del contesto. In alternativa, se un componente usa solo il controllo di accesso a livello di processo, la relativa proprietà del contesto di sicurezza viene ignorata. la configurazione di sicurezza del componente non svolgerà mai un ruolo nell'attivazione.

## <a name="forcing-activation-in-the-callers-context"></a>Forzare l'attivazione nel contesto del chiamante

In alcune circostanze, è possibile che un oggetto venga attivato solo nel contesto del chiamante, ovvero mai attivato nel contesto. Ad esempio, potrebbe essere necessario controllare il comportamento dell'oggetto quando viene chiamato attraverso un limite del contesto.

È possibile verificare che un oggetto non possa essere attivato nel proprio contesto selezionando l'opzione di **contesto deve essere attivato in chiamanti** nella scheda **attivazione** della pagina **proprietà** componente, usando lo strumento di amministrazione Servizi componenti. Per istruzioni dettagliate, vedere [applicazione dell'attivazione nel contesto del chiamante](enforcing-activation-in-the-caller-s-context.md) . Quando si seleziona questa opzione, se l'oggetto non può essere attivato nel contesto del chiamante, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha esito negativo, restituendo un \_ \_ tentativo \_ di creazione al di \_ fuori del \_ \_ \_ contesto client.

## <a name="default-context"></a>Contesto predefinito

Sono disponibili contesti predefiniti per supportare componenti non configurati, ovvero componenti COM non installati nelle applicazioni COM+ e non registrati nel database di registrazione della classe COM+. Se i componenti non configurati hanno un modello di threading compatibile, vengono attivati nel contesto del chiamante. In caso contrario, vengono attivati in un contesto predefinito nell'Apartment appropriato. Ogni Apartment dispone di un contesto predefinito per supportare gli oggetti COM che non utilizzano servizi COM+.

## <a name="hooking-activation"></a>Attivazione dell'hook

Implementando [**IObjectControl:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e [**IObjectControl::D ttiva**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), è possibile associare l'attivazione e la disattivazione insieme per eseguire un'inizializzazione speciale nel nuovo contesto. Questi metodi vengono chiamati da COM+ in determinati punti del ciclo di vita di un oggetto, quando l'oggetto è configurato per l'utilizzo dell'attivazione JIT o del pool di oggetti. Per informazioni più dettagliate, vedere [attivazione JIT di com+](com--just-in-time-activation.md) e [pool di oggetti com+](com--object-pooling.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Intercettazione di chiamate tra contesti](interception-of-cross-context-calls.md)
</dt> </dl>

 

 
