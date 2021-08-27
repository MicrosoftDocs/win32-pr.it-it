---
description: Windows Il programma di installazione può ripristinare, sostituire e verificare i file contenuti in un'applicazione. Potrebbe essere necessaria una reinstallazione parziale o completa dell'applicazione se alcuni file o voci del Registro di sistema associati a una funzionalità sono mancanti o danneggiati.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Reinstallazione di una funzionalità o di un'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803fc3271cb69280ae84ae096e7a411dbf599f0a321bf15baac6dbd5ca8e1512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086001"
---
# <a name="reinstalling-a-feature-or-application"></a>Reinstallazione di una funzionalità o di un'applicazione

Windows Il programma di installazione può ripristinare, sostituire e verificare i file contenuti in un'applicazione. Potrebbe essere necessaria una reinstallazione parziale o completa dell'applicazione se alcuni file o voci del Registro di sistema associati a una funzionalità sono mancanti o danneggiati.

Quando una funzionalità o un'applicazione viene reinstallata, vengono reinstallati anche tutti i servizi, le variabili di ambiente e le azioni personalizzate appartenenti alla funzionalità o all'applicazione. Si noti che ciò significa che tutte le modifiche apportate alle variabili di ambiente tra l'installazione originale e la reinstallazione andranno perse.

L'elenco seguente contiene i metodi per reinstallare una funzionalità o un prodotto. I primi due metodi sono stati automatizzati dal programma di installazione:

-   Ripristinare, sostituire o verificare i file chiamando la [**funzione MsiReinstallFeature.**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
-   Reinstallare l'intero prodotto chiamando [**la funzione MsiReinstallProduct.**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)
-   Reinstallare, sostituire o verificare i file con un pulsante di controllo dell'interfaccia utente del programma di installazione [tramite Reinstall ControlEvent](reinstall-controlevent.md).
-   Reinstallare, sostituire o verificare i file da una riga di comando impostando la [**proprietà REINSTALL**](reinstall.md) e la [**proprietà REINSTALLMODE.**](reinstallmode.md)

Per altre informazioni sulla reinstallazione di una funzionalità o di un'applicazione, vedere [Resilienza.](resiliency.md)

**Per reinstallare un prodotto usando il programma di installazione**

-   Chiamare [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta).

**Per reinstallare una funzionalità tramite il programma di installazione**

-   Chiamare [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

**Per reinstallare un prodotto o una funzionalità con un'interfaccia utente del programma di installazione**

1.  Aggiungere un pulsante alla finestra di dialogo specificata aggiungendo una voce alla [tabella Control](control-table.md).
2.  Aggiungere un [oggetto ReinstallMode ControlEvent](reinstallmode-controlevent.md) alla tabella ControlEvent, con i campi Dialog e Control che fanno riferimento al controllo \_ pulsante creato nel passaggio \_ 1. Nel campo Argomento immettere una stringa contenente le lettere corrispondenti alle modalità di reinstallazione desiderate. I valori accettabili per questo campo sono identici a quelli accettati per la [**proprietà REINSTALLMODE.**](reinstallmode.md) Il valore nella colonna Ordinamento per questo evento deve essere 1.
3.  Aggiungere un [evento Reinstall ControlEvent](reinstall-controlevent.md) alla tabella [ControlEvent](controlevent-table.md), facendo di nuovo riferimento allo stesso controllo pulsante. Il campo Argomento per questo evento sarà in genere ALL, per forzare la reinstallazione di tutte le funzionalità, ma è possibile inserire il nome di una funzionalità specifica qui. Il valore nella colonna Ordinamento per questo evento deve essere 2.
4.  Aggiungere un altro evento associato allo stesso controllo pulsante per avviare effettivamente la reinstallazione. Può trattarsi di un evento EndDialog (con un argomento Return). Più in genere, tuttavia, qui viene usato un evento NewDialog per passare a una finestra di dialogo di conferma È sicuro di voler **reinstallare?** . Il valore nella colonna Ordinamento per questo evento deve essere 3.

    Se si desidera, è possibile creare diversi pulsanti [**REINSTALL**](reinstall.md) per una singola finestra di dialogo, consentendo all'utente di selezionare il tipo di reinstallazione eseguita. In questo caso, ogni pulsante viene creato come descritto nella procedura precedente, con un parametro [ControlEvent ReinstallMode](reinstallmode-controlevent.md) diverso per ogni pulsante.

Dopo aver installato un determinato prodotto (con alcune o tutte le funzionalità del prodotto), è possibile eseguire una reinstallazione dalla riga di comando:

**Per reinstallare un prodotto o una funzionalità dalla riga di comando**

1.  Al prompt dei comandi specificare la [**proprietà REINSTALL.**](reinstall.md)
2.  Al prompt dei comandi specificare la [**proprietà REINSTALLMODE.**](reinstallmode.md)

    La specifica di queste proprietà consente all'utente di reinstallare una o tutte le funzionalità del prodotto. È anche possibile specificare il tipo di reinstallazione. Ad esempio, è possibile specificare che devono essere reinstallati solo i file completamente mancanti o che solo i file danneggiati (ad esempio, qualsiasi file eseguibile il cui checksum non corrisponde al contenuto effettivo del file) devono essere sostituiti.

 

 



