---
description: Il gestore di dispenser fornisce il pool di risorse per i distributori di risorse e assicura che una risorsa fornita da un dispenser di risorse sia correttamente integrata nella transazione oggetti applicazione.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Gestore di distribuzioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523578"
---
# <a name="com-dispenser-manager"></a>Gestore di distribuzioni COM+

Il responsabile del dispenser fornisce il pool di risorse per i distributori di risorse e assicura che una risorsa fornita da un dispenser di risorse sia correttamente integrata nella transazione dell'oggetto applicazione. Il gestore del dispenser recupera automaticamente le risorse ancora riservate alla fine della durata di un oggetto, eliminando la possibilità di perdita di risorse. Il responsabile del dispenser può richiedere a un dispenser di risorse di creare una nuova risorsa o eliminare le risorse inattive quando necessario per modificare i livelli di inventario, anziché usare impostazioni statiche.

> [!Note]  
> Poiché le interfacce del dispenser di risorse esposte all'applicazione non devono essere interfacce COM, il gestore di dispenser può essere usato in un processo senza inizializzare COM, ad esempio per supportare il dispenser di risorse ODBC.

 

Al momento della creazione delle risorse, il dispenser di risorse può specificare per quanto tempo è consentita la permanenza di una risorsa inattiva nel pool prima che venga distrutta. Un thread che viene eseguito in Gestione dispenser cerca sempre queste risorse inattive.

## <a name="the-inventory-statistics-manager"></a>Gestione statistiche inventario

Il gestore di dispenser USA *Inventory Statistics Manager* per gestire i livelli di inventario delle risorse del pool. Inventory Statistics Manager mantiene un record del momento in cui ogni risorsa è stata usata e rimuove le risorse dall'inventario quando non sono state usate per *x* secondi, in cui il valore di *x* viene impostato per ogni risorsa quando viene creata la risorsa.

## <a name="the-holder-component"></a>Componente del contenitore

Il responsabile del dispenser esegue il polling di ogni *titolare*, un componente creato dal responsabile del dispenser, che elenca l'inventario delle risorse per ogni dispenser di risorse, ogni 10 secondi per consentire la modifica dell'inventario delle risorse. Ogni titolare chiama Inventory Statistics Manager per suggerire i livelli di inventario per ogni tipo di risorsa. Di conseguenza, il titolare può richiedere al dispenser di risorse di creare o distruggere un inventario.

Il titolare e il dispenser di risorse comunicano per richiedere risorse di un determinato tipo. Tra il titolare e il dispenser di risorse esistono le relazioni seguenti:

-   Il titolare può richiedere una risorsa dal dispenser di risorse. Il dispenser di risorse restituisce una risorsa disponibile o ne crea uno nuovo.
-   Il titolare può notificare al dispenser di risorse che un'applicazione non necessita più di una risorsa e quindi restituirla al pool di risorse.
-   Il titolare e il dispenser di risorse interagiscono per mantenere le dimensioni del pool di risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi al dispenser di risorse COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



