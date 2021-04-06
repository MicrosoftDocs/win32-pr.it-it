---
description: Un aggiornamento secondario è un aggiornamento che apporta modifiche a molte risorse.
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: Aggiornamenti secondari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833bb46e2cafe0545f83c0ed0f8ff8aba00f0695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883930"
---
# <a name="minor-upgrades"></a>Aggiornamenti secondari

Un aggiornamento secondario è un aggiornamento che apporta modifiche a molte risorse. Nessuna delle modifiche può richiedere la modifica di [**ProductCode**](productcode.md). Un aggiornamento richiede un [aggiornamento principale](major-upgrades.md) per modificare il **ProductCode**. È possibile usare un aggiornamento secondario per aggiungere nuove funzionalità e componenti, ma non è possibile riorganizzare l'albero dei componenti della funzionalità. Gli aggiornamenti secondari offrono una differenziazione del prodotto senza definire effettivamente un prodotto diverso. Un aggiornamento secondario tipico include tutte le correzioni negli aggiornamenti piccoli precedenti combinati in una patch. Un aggiornamento secondario è noto anche come aggiornamento di Service Pack (SP). Per ulteriori informazioni sugli aggiornamenti che non richiedono la modifica del **ProductCode** , vedere [modifica del codice del prodotto](changing-the-product-code.md).

Un aggiornamento secondario modifica la proprietà [**ProductVersion**](productversion.md) . La modifica della versione del prodotto dell'applicazione significa che i diversi aggiornamenti hanno un ordine. Ad esempio, se era disponibile una patch per l'aggiornamento dalla versione 9,0 alla versione 9,1 e un'altra patch per la patch v 9,1 a v 9,2, il programma di installazione può applicare l'ordine corretto controllando la versione del prodotto prima di applicare la patch. Questa operazione impedisce inoltre l'applicazione della patch v 9,1 a v 9,2 a v 9,0. Per le patch, questo ordinamento viene applicato attraverso la versione del prodotto, ovvero i bit di convalida impostati nelle trasformazioni incluse nel [pacchetto di patch](patch-packages.md).

Un aggiornamento secondario e un aggiornamento di dimensioni ridotte variano a seconda che un aggiornamento secondario modifichi il codice del pacchetto e la versione del prodotto. Vedere [piccoli aggiornamenti](small-updates.md) per le linee guida sui tipi di aggiornamenti che possono essere gestiti da un piccolo aggiornamento o da un aggiornamento secondario. Gli aggiornamenti secondari vengono spediti come pacchetto di installazione completo del prodotto o come [pacchetto di patch](patch-packages.md). Tuttavia, un aggiornamento secondario non può usare un'etichetta di volume diversa per la nuova versione.

Per informazioni su come applicare un aggiornamento secondario, vedere gli argomenti seguenti:

-   [Applicazione di piccoli aggiornamenti con l'applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Applicazione di piccoli aggiornamenti con la reinstallazione del prodotto](applying-small-updates-by-reinstalling-the-product.md)
-   [Applicazione di piccoli aggiornamenti con l'applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)

 

 



