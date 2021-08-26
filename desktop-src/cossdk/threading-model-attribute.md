---
description: COM+ gestisce i thread per l'utente. Ogni componente COM ha una proprietà ThreadingModel che è possibile specificare quando si sviluppa il componente. Questa proprietà determina il modo in cui gli oggetti componenti vengono assegnati ai thread per l'esecuzione del metodo.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Attributo del modello di threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba6ae625e4413516066f7180a4eb6870fe4f90df38947fc2476cfbcc7dfadb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070241"
---
# <a name="threading-model-attribute"></a>Attributo del modello di threading

COM+ gestisce i thread per l'utente. Ogni componente COM ha una **proprietà ThreadingModel** che è possibile specificare quando si sviluppa il componente. Questa proprietà determina il modo in cui gli oggetti del componente vengono assegnati ai thread per l'esecuzione del metodo.

È possibile usare lo strumento amministrativo Servizi componenti per visualizzare la proprietà del modello di threading facendo clic con il pulsante destro del mouse su un componente nella cartella **Componenti** , scegliendo Proprietà **e** quindi facendo clic sulla scheda **Concorrenza** . In **Modello di threading** i valori possibili sono i seguenti:

-   **Apartment del thread principale**
-   **Apartment a thread singolo**
-   **Free Thread Apartment**
-   **Neutral Apartment**
-   **Qualsiasi apartment**

Il modello di threading preferito per COM+ è [l'apartment neutro.](neutral-apartments.md) Tuttavia, se non si specifica un modello di threading per il componente, COM+ usa l'apartment di thread principale, che è l'impostazione predefinita.

> [!Note]  
> Per informazioni più dettagliate, vedere [Scelta del modello di threading](/windows/desktop/com/choosing-the-threading-model).

 

La tabella seguente illustra il modello di programmazione per apartment in COM+.



| Modellare                     | Appartamento                                                 | Gratuito                               | Entrambe                               | Neutralità                      | Non specificato                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| A thread singolo, non principale | Creato nell'apartment corrente                              | Creato nell'apartment multithreading | Creato nell'apartment corrente       | Creato in un apartment neutro | Creato nell'apartment con thread principale |
| A thread singolo, main     | Creato nell'apartment corrente                              | Creato nell'apartment multithreading | Creato nell'apartment corrente       | Creato in un apartment neutro | Creato nell'apartment corrente       |
| Multithreading             | Creato nell'apartment a thread singolo dell'host                 | Creato nell'apartment multithreading | Creato nell'apartment multithreading | Creato in un apartment neutro | Creato nell'apartment con thread principale |
| Neutro (nel thread STA)   | Creato nell'apartment a thread singolo host per questo thread | Creato nell'apartment multithreading | Creato in un apartment neutro       | Creato in un apartment neutro | Creato nell'apartment con thread principale |
| Neutro (nel thread MTA)   | Creato nell'apartment a thread singolo dell'host                 | Creato nell'apartment multithreading | Creato in un apartment neutro       | Creato in un apartment neutro | Creato nell'apartment con thread principale |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Threadingmodel**](components.md)
</dt> </dl>

 

 
