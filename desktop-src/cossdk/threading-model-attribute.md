---
description: COM+ gestisce automaticamente i thread. Ogni componente COM dispone di una proprietà ThreadingModel che è possibile specificare quando si sviluppa il componente. Questa proprietà determina il modo in cui gli oggetti Components vengono assegnati ai thread per l'esecuzione del metodo.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Attributo del modello di threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401398"
---
# <a name="threading-model-attribute"></a>Attributo del modello di threading

COM+ gestisce automaticamente i thread. Ogni componente COM dispone di una proprietà **ThreadingModel** che è possibile specificare quando si sviluppa il componente. Questa proprietà determina il modo in cui gli oggetti del componente vengono assegnati ai thread per l'esecuzione del metodo.

È possibile utilizzare lo strumento di amministrazione Servizi componenti per visualizzare la proprietà del modello di threading facendo clic con il pulsante destro del mouse su un componente nella cartella **componenti** , scegliendo **Proprietà**, quindi facendo clic sulla scheda **concorrenza** . In **modello di threading** i valori possibili sono i seguenti:

-   **Apartment thread principale**
-   **Apartment a thread singolo**
-   **Apartment thread libero**
-   **Apartment neutro**
-   **Qualsiasi Apartment**

Il modello di threading preferito per COM+ è l' [Apartment neutro](neutral-apartments.md). Tuttavia, se non si specifica un modello di threading per il componente, COM+ utilizza l'Apartment thread principale, che è l'impostazione predefinita.

> [!Note]  
> Per informazioni più dettagliate, vedere [scelta del modello di threading](/windows/desktop/com/choosing-the-threading-model).

 

La tabella seguente illustra il modello di programmazione per gli appartamenti in COM+.



| Modello                     | Apartment                                                 | Gratuito                               | Entrambi                               | Neutralità                      | Non specificato                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| A thread singolo, non principale | Creato nell'Apartment corrente                              | Creato in un Apartment a thread multipli | Creato nell'Apartment corrente       | Creato in un Apartment neutro | Creato nell'Apartment a thread principale |
| A thread singolo, principale     | Creato nell'Apartment corrente                              | Creato in un Apartment a thread multipli | Creato nell'Apartment corrente       | Creato in un Apartment neutro | Creato nell'Apartment corrente       |
| Multithreading             | Creato nell'Apartment a thread singolo host                 | Creato in un Apartment a thread multipli | Creato in un Apartment a thread multipli | Creato in un Apartment neutro | Creato nell'Apartment a thread principale |
| Neutro (sul thread STA)   | Creato nell'Apartment a thread singolo host per questo thread | Creato in un Apartment a thread multipli | Creato in un Apartment neutro       | Creato in un Apartment neutro | Creato nell'Apartment a thread principale |
| Neutro (su thread MTA)   | Creato nell'Apartment a thread singolo host                 | Creato in un Apartment a thread multipli | Creato in un Apartment neutro       | Creato in un Apartment neutro | Creato nell'Apartment a thread principale |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
