---
description: Il gestore di dispenser fornisce il pool di risorse per i dispenser di risorse e garantisce che una risorsa fornita da un dispenser di risorse sia integrata correttamente nella transazione degli oggetti applicazione.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: COM+ Dispenser Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec090ba8c6324363c80a00685e4bc9cfa11185fa1b95ad5db3575608c9fe60ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991691"
---
# <a name="com-dispenser-manager"></a>COM+ Dispenser Manager

Il gestore di dispenser fornisce il pool di risorse per i dispenser di risorse e garantisce che una risorsa fornita da un dispenser di risorse sia integrata correttamente nella transazione dell'oggetto applicazione. Il gestore del dispenser recupera automaticamente le risorse che sono ancora riservate alla fine della durata di un oggetto, eliminando la possibilità di perdite di risorse. Il gestore di dispenser può chiedere a un distributore di risorse di creare una nuova risorsa o di eliminare le risorse inattive quando necessario per regolare i livelli di inventario, anziché usare impostazioni statiche.

> [!Note]  
> Poiché le interfacce del dispenser di risorse esposte all'applicazione non devono essere interfacce COM, il gestore del dispenser può essere usato in un processo senza inizializzare COM, ad esempio, per supportare il dispenser di risorse ODBC.

 

Al momento della creazione della risorsa, il dispenser di risorse può specificare per quanto tempo una risorsa inattiva può rimanere nel pool prima che venga distrutta. Un thread eseguito nel gestore del dispenser cerca sempre queste risorse inattive.

## <a name="the-inventory-statistics-manager"></a>Gestione statistiche di inventario

Il gestore del dispenser usa il *gestore delle statistiche di inventario per* gestire i livelli di inventario delle risorse del pool. Gestione statistiche di inventario mantiene un record di quando è stata usata ogni risorsa e rimuove le risorse dall'inventario quando non sono state usate per *x* secondi, dove il valore *di x* viene impostato per ogni risorsa quando viene creata la risorsa.

## <a name="the-holder-component"></a>Componente Holder

Il gestore di dispenser esegue il polling di ogni *titolare,* un componente creato dal gestore di dispenser che elenca l'inventario delle risorse per ogni dispenser di risorse, ogni 10 secondi per consentire di modificare l'inventario delle risorse. Ogni titolare chiama il gestore delle statistiche di inventario per suggerire i livelli di inventario per ogni tipo di risorsa. Di conseguenza, il titolare può chiedere al distributore di risorse di creare o eliminare un inventario.

Il titolare e il distributore di risorse comunicano per richiedere risorse di un particolare tipo. Tra il titolare e il distributore di risorse esistono le relazioni seguenti:

-   Il titolare può richiedere una risorsa dal dispenser di risorse. Il dispenser di risorse restituisce una risorsa disponibile o ne crea una nuova.
-   Il titolare può notificare al distributore di risorse che un'applicazione non necessita più di una risorsa e quindi restituirla al pool di risorse.
-   Il titolare e il distributore di risorse lavorano insieme per mantenere le dimensioni del pool di risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti del dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



