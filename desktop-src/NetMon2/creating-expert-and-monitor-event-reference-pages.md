---
description: In questa sezione viene descritto come pianificare, sviluppare e testare le pagine di riferimento per gli eventi (ERPs) e come distribuirle in un esperto o un monitoraggio. Per informazioni su ERPs e su come usarle con Network Monitor, vedere la pagina di riferimento dell'evento.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Creazione di pagine di riferimento per gli eventi Expert e monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311626"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>Creazione di pagine di riferimento per gli eventi Expert e monitor

In questa sezione viene descritto come pianificare, sviluppare e testare le pagine di riferimento per gli eventi (ERPs) e come distribuirle in un esperto o un monitoraggio. Per informazioni su ERPs e su come usarle con Network Monitor, vedere la [pagina di riferimento dell'evento](event-reference-page.md).

Per sviluppare un nuovo ERP, il primo passaggio consiste nel determinare gli eventi che richiedono singoli ERPs per il [monitoraggio](monitors.md)o l' [esperto](experts.md) personalizzato. È necessario creare ERPs separate per ogni evento che si desidera visualizzare nel Visualizzatore eventi di Network Monitor. Si supponga, ad esempio, che:

-   Si sviluppa un monitoraggio denominato Game Monitor e stock Watcher.
-   Il monitoraggio si trova in un file denominato Gamemon.dll.
-   Il monitoraggio genera due eventi, i giochi in esecuzione e le scorte Internet aumentano.
-   Si prevede di sviluppare due ERPs, Gamemon1.htm e Gamemon2.htm.

> [!Note]  
> Non è necessario avere una corrispondenza uno-a-uno tra ERPs per il monitoraggio o gli eventi esperti.

 

Dopo aver stabilito un elenco di ERPs univoche, seguire questa procedura per creare ogni ERP.

-   [Scrivere il documento di origine HTML](writing-an-event-reference-page.md).
-   [Salvare e denominare](naming-an-event-reference-page.md) il file di origine HTML come file con estensione htm.
-   [Testare il ERP](testing-an-event-reference-page.md) con l'esperto o il monitoraggio completato.

 

 



