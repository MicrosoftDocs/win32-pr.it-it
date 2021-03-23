---
title: Uso di una firma radice
description: La firma radice è la definizione di una raccolta disposta in modo arbitrario di tabelle dei descrittori (incluso il relativo layout), costanti radice e descrittori radice.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105092"
---
# <a name="using-a-root-signature"></a>Uso di una firma radice

La firma radice è la definizione di una raccolta disposta in modo arbitrario di tabelle dei descrittori (incluso il relativo layout), costanti radice e descrittori radice. Ogni voce ha un costo verso un limite massimo, pertanto l'applicazione può comportare un compromesso tra il numero di ogni tipo di voce che la firma radice conterrà.

-   [Semantica elenco comandi](#command-list-semantic)
-   [Semantica bundle](#bundle-semantics)
-   [Argomenti correlati](#related-topics)

La firma radice è un oggetto che può essere creato dalla specifica manuale nell'API. Tutti gli shader in un oggetto PSO devono essere compatibili con il layout radice specificato con l'oggetto PSO. in caso contrario, i singoli shader devono includere layout radice incorporati che corrispondono tra loro. in caso contrario, la creazione di PSO non riuscirà. Una proprietà della firma radice è che non è necessario che gli shader ne siano a conoscenza quando vengono creati, sebbene le firme radice possano essere create direttamente in shader, se lo si desidera. Per gli asset shader esistenti non è necessario che le modifiche siano compatibili con le firme radice. Il modello di shader 5,1 è stato introdotto per offrire una flessibilità aggiuntiva (indicizzazione dinamica dei descrittori dall'interno degli shader), che può essere adottata in modo incrementale a partire dalle risorse dello shader esistenti, se lo si desidera.

## <a name="command-list-semantic"></a>Semantica elenco comandi

All'inizio di un elenco di comandi, la firma radice non è definita. Gli shader grafici hanno una firma radice separata dal compute shader, ciascuno assegnato in modo indipendente in un elenco di comandi. La firma radice impostata in un elenco di comandi o in un bundle deve corrispondere anche all'oggetto PSO attualmente impostato al momento dell'estrazione. in caso contrario, il comportamento non è definito. Mancata corrispondenza della firma radice temporanea prima che il metodo di creazione/invio sia corretto, ad esempio impostando un oggetto PSO incompatibile prima di passare a una firma radice compatibile (purché siano compatibili con l'ora di creazione/invio). L'impostazione di un oggetto PSO non comporta la modifica della firma radice. Per impostare la firma radice, l'applicazione deve chiamare un'API dedicata.

Una volta impostata una firma radice in un elenco di comandi, il layout definisce il set di binding che l'applicazione deve fornire e quali PSO possono essere utilizzati (quelli compilati con lo stesso layout) per le successive chiamate di disegno/invio. Una firma radice, ad esempio, può essere definita dall'applicazione per includere le voci seguenti. Ogni voce viene definita "slot".

-   \[0 \] un descrittore CBV inline (descrittori radice)
-   \[1 \] tabella descrittore contenente 2 SRVs, 1 CBVs e 1 UAV
-   \[2 \] tabella descrittore contenente 1 campionatore
-   \[3 \] raccolta a 4x32 bit di costanti radice
-   \[4 \] tabella descrittore contenente un numero di SRVs non specificato

In questo caso, prima di poter emettere un progetto/dispatch, è previsto che l'applicazione imposti l'associazione appropriata a ognuno degli slot \[ 0.. 4 \] definiti dall'applicazione con la firma radice corrente. Ad esempio, in corrispondenza dello slot \[ 1 \] , è necessario associare una tabella dei descrittori, che è un'area contigua in un heap descrittore che contiene (o conterrà at execution) 2 SRVs, 1 CBVs e 1 UAV. Analogamente, le tabelle del descrittore devono essere impostate negli slot \[ 2 \] e \[ 4 \] .

L'applicazione può modificare parte delle associazioni della firma radice alla volta (il resto rimane invariato). Se, ad esempio, l'unico elemento che deve cambiare tra le estrazioni è una delle costanti in corrispondenza dello slot \[ 2 \] , è necessario riassociare l'applicazione. Come illustrato in precedenza, le versioni del driver/hardware di tutte le firme radice associano lo stato modificato automaticamente. Se una firma radice viene modificata in un elenco di comandi, tutte le associazioni di firma radice precedenti diventano obsolete e tutte le associazioni appena previste devono essere impostate prima di creare/inviare. in caso contrario, il comportamento non è definito. Se la firma radice è impostata in modo ridondante sullo stesso oggetto attualmente impostato, le associazioni della firma radice esistenti non diventano obsolete.

## <a name="bundle-semantics"></a>Semantica bundle

I bundle ereditano i binding della firma radice dell'elenco di comandi (i binding ai vari slot nell'esempio di elenco dei comandi precedente). Se un bundle deve modificare alcune delle associazioni di firma radice ereditate, deve innanzitutto impostare la firma radice in modo che corrisponda all'elenco dei comandi chiamante (le associazioni ereditate non diventano obsolete). Se il bundle imposta la firma radice in modo che sia diverso dall'elenco dei comandi chiamante, che ha lo stesso effetto della modifica della firma radice nell'elenco dei comandi descritto in precedenza: tutti i binding della firma radice precedenti sono obsoleti e le associazioni appena previste devono essere impostate prima di creare/inviare. in caso contrario, il comportamento non è definito. Se non è necessario che un bundle modifichi le associazioni della firma radice, non è necessario impostare la firma radice.

Il codice seguente mostra un esempio di flusso di chiamate in un bundle.

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

Quando si esce da un bundle, le modifiche apportate al layout radice e/o le modifiche di binding apportate dal bundle vengono ereditate nuovamente nell'elenco dei comandi chiamante al termine dell'esecuzione di un bundle.

Per altre informazioni sull'ereditarietà, vedere la sezione **ereditarietà dello stato della pipeline grafica** di [gestione dello stato della pipeline grafica in Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Firme radice](root-signatures.md)
</dt> </dl>

 

 




