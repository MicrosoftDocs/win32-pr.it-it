---
description: Windows Installer possibile ripristinare, sostituire e verificare i file contenuti in un'applicazione. Potrebbe essere necessaria una reinstallazione parziale o completa dell'applicazione se eventuali file o voci del registro di sistema associate a qualsiasi funzionalità sono mancanti o danneggiati.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Reinstallazione di una funzionalità o di un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f7dbf95204d96202c71a120eafb6e6e054ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131614"
---
# <a name="reinstalling-a-feature-or-application"></a>Reinstallazione di una funzionalità o di un'applicazione

Windows Installer possibile ripristinare, sostituire e verificare i file contenuti in un'applicazione. Potrebbe essere necessaria una reinstallazione parziale o completa dell'applicazione se eventuali file o voci del registro di sistema associate a qualsiasi funzionalità sono mancanti o danneggiati.

Quando una funzionalità o un'applicazione viene reinstallata, vengono reinstallati anche tutti i servizi, le variabili di ambiente e le azioni personalizzate appartenenti alla funzionalità o all'applicazione. Si noti che questo significa che tutte le modifiche apportate alle variabili di ambiente tra l'installazione originale e la reinstallazione vengono perse.

Nell'elenco seguente sono inclusi i metodi di reinstallazione di una funzionalità o di un prodotto. I primi due metodi sono stati automatizzati dal programma di installazione:

-   Ripristinare, sostituire o verificare i file chiamando la funzione [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) .
-   Reinstallare l'intero prodotto chiamando la funzione [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) .
-   Reinstallare, sostituire o verificare i file con un pulsante di controllo dell'interfaccia utente del programma di installazione tramite la [Reinstallazione ControlEvent](reinstall-controlevent.md).
-   Reinstallare, sostituire o verificare i file da una riga di comando impostando la proprietà [**REINSTALL**](reinstall.md) e la proprietà [**REINSTALLMODE**](reinstallmode.md) .

Per ulteriori informazioni sulla reinstallazione di una funzionalità o di un'applicazione, vedere [resilienza](resiliency.md).

**Per reinstallare un prodotto utilizzando il programma di installazione**

-   Chiamare [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta).

**Per reinstallare una funzionalità tramite il programma di installazione**

-   Chiamare [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

**Per reinstallare un prodotto o una funzionalità con un'interfaccia utente del programma di installazione**

1.  Aggiungere un pulsante alla finestra di dialogo specificata aggiungendo una voce alla tabella del [controllo](control-table.md).
2.  Aggiungere un [ControlEvent REINSTALLMODE](reinstallmode-controlevent.md) alla tabella ControlEvent, con i campi finestra di dialogo \_ e controllo che \_ fanno riferimento al controllo Button creato nel passaggio 1. Nel campo argomento immettere una stringa contenente le lettere corrispondenti alle modalità di reinstallazione desiderate. i valori accettabili per questo campo sono identici a quelli accettati per la proprietà [**REINSTALLMODE**](reinstallmode.md) . Il valore nella colonna Ordering per questo evento deve essere 1.
3.  Aggiungere un evento [REINSTALL ControlEvent](reinstall-controlevent.md) alla [tabella ControlEvent](controlevent-table.md), facendo nuovamente riferimento allo stesso controllo Button. Il campo argomento per questo evento sarà in genere tutto, per forzare la reinstallazione di tutte le funzionalità, ma qui è possibile inserire il nome di una funzionalità specifica. Il valore nella colonna Ordering per questo evento deve essere 2.
4.  Aggiungere un altro evento associato allo stesso controllo Button per avviare effettivamente la reinstallazione. Può trattarsi di un evento EndDialog (con un argomento di Return). In genere, tuttavia, viene usato un evento NewDialog per passare a una finestra di dialogo di conferma che si **vuole reinstallare?** . Il valore nella colonna Ordering per questo evento deve essere 3.

    Se lo si desidera, è possibile creare diversi pulsanti di [**Reinstallazione**](reinstall.md) per una singola finestra di dialogo, in modo da consentire all'utente di selezionare il tipo di reinstallazione eseguito. In questo caso, ogni pulsante viene creato come descritto nella procedura precedente, con un parametro [REINSTALLMODE ControlEvent](reinstallmode-controlevent.md) diverso per ogni pulsante.

Una volta installato un particolare prodotto (con alcune o tutte le funzionalità del prodotto), è possibile eseguire una reinstallazione dalla riga di comando:

**Per reinstallare un prodotto o una funzionalità da una riga di comando**

1.  Al prompt dei comandi specificare la proprietà [**REINSTALL**](reinstall.md) .
2.  Al prompt dei comandi specificare la proprietà [**REINSTALLMODE**](reinstallmode.md) .

    L'impostazione di queste proprietà consente all'utente di reinstallare una o tutte le funzionalità del prodotto. È anche possibile specificare il tipo di reinstallazione. Ad esempio, è possibile specificare che solo i file completamente mancanti devono essere reinstallati o che solo i file danneggiati, ad esempio file eseguibili il cui checksum non corrisponde al contenuto effettivo del file, vengano sostituiti.

 

 



