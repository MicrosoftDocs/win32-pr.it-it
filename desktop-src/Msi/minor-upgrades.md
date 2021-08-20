---
description: Un aggiornamento secondario è un aggiornamento che apporta modifiche a molte risorse.
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: Aggiornamenti secondari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ea964f7aabefb04337770d6483c33d7072d34e72fffa5bad44519ee0bdbb7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804576"
---
# <a name="minor-upgrades"></a>Aggiornamenti secondari

Un aggiornamento secondario è un aggiornamento che apporta modifiche a molte risorse. Nessuna delle modifiche può richiedere la modifica di [**ProductCode**](productcode.md). Un aggiornamento richiede un [aggiornamento importante per](major-upgrades.md) modificare **ProductCode**. Un aggiornamento secondario può essere usato per aggiungere nuove funzionalità e componenti, ma non può riorganizzare l'albero dei componenti delle funzionalità. Gli aggiornamenti secondari forniscono la differenziazione del prodotto senza definire effettivamente un prodotto diverso. Un tipico aggiornamento secondario include tutte le correzioni negli aggiornamenti di piccole dimensioni precedenti combinate in una patch. Un aggiornamento secondario è noto anche come aggiornamento del Service Pack (SP). Per altre informazioni sugli aggiornamenti che non richiedono la modifica di **ProductCode,** vedere [Modifica del codice prodotto](changing-the-product-code.md).

Un aggiornamento secondario modifica la [**proprietà ProductVersion.**](productversion.md) La modifica della versione del prodotto dell'applicazione implica che i diversi aggiornamenti hanno un ordine. Ad esempio, se esisteva una patch per l'aggiornamento da v 9.0 a v 9.1 e esisteva un'altra patch per applicare la patch da 9.1 a v 9.2, il programma di installazione può applicare l'ordine corretto controllando la versione del prodotto prima di applicare la patch. Ciò impedisce anche l'applicazione della patch da v 9.1 a v 9.2 alla versione 9.0. Per le patch, questo ordinamento viene applicato tramite i bit di convalida della versione del prodotto impostati nelle trasformazioni incluse nel [pacchetto patch](patch-packages.md).

Un aggiornamento secondario e un piccolo aggiornamento sono diversi in base al fatto che un aggiornamento secondario modifica il codice del pacchetto e la versione del prodotto. Vedere [Aggiornamenti di](small-updates.md) piccole dimensioni per le linee guida sui tipi di aggiornamenti che possono essere gestiti da un aggiornamento di piccole dimensioni o da un aggiornamento secondario. Gli aggiornamenti secondari vengono forniti come pacchetto di installazione completo del prodotto o come [pacchetto di patch.](patch-packages.md) Tuttavia, un aggiornamento secondario non può usare un'etichetta di volume diversa per la nuova versione.

Per informazioni su come applicare un aggiornamento secondario, vedere gli argomenti seguenti:

-   [Applicazione di piccoli aggiornamenti tramite applicazione di patch all'installazione locale del prodotto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Applicazione di piccoli aggiornamenti reinstallando il prodotto](applying-small-updates-by-reinstalling-the-product.md)
-   [Applicazione di piccoli aggiornamenti tramite applicazione di patch a un'immagine amministrativa](applying-small-updates-by-patching-an-administrative-image.md)

 

 



