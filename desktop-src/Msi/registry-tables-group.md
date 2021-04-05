---
description: Il gruppo registro di Windows Installer tabelle contiene informazioni sulle voci del registro di sistema.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Gruppo di tabelle del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba14bdc2bc5668ce2de3ec66172c75c176ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881481"
---
# <a name="registry-tables-group"></a>Gruppo di tabelle del registro di sistema

![gruppo di tabelle del registro di sistema](images/registry.png)

Per ulteriori informazioni su questo diagramma, vedere la [legenda del diagramma delle relazioni tra entità](entity-relationship-diagram-legend.md).

Il programma di installazione dispone di tabelle specifiche per i diversi tipi di voci del registro di sistema. Quando si popola il gruppo di tabelle del registro di sistema è importante provare a ridurre al minimo il numero di voci inserite nella [tabella del registro di sistema](registry-table.md) e ottimizzare l'utilizzo delle altre tabelle specifiche del registro di sistema. Questo perché il programma di installazione non è in grado di distinguere tra tipi diversi di voci del registro di sistema nella tabella del registro di sistema e non può usare la logica interna necessaria per sfruttare appieno tutte le funzionalità del programma di installazione, ad esempio l' [*annuncio*](a-gly.md). La creazione di voci del registro di sistema relative a COM e Shell in questo modo fornisce anche un'organizzazione più logica e consente di ridurre al minimo la registrazione errata delle informazioni sul server COM.

Nella figura è illustrato il gruppo voce del registro di sistema delle tabelle, nonché la tabella dei [componenti](component-table.md), la [tabella delle funzionalità](feature-table.md)e la [tabella dei file](file-table.md). Sebbene queste ultime non siano direttamente associate al popolamento del registro di sistema, sono incluse nella figura perché sono essenziali per la logica del gruppo di voci del registro di sistema.

Il gruppo voce del registro di sistema contiene le seguenti tabelle di voci del registro di sistema specifiche.

-   La [tabella di estensione](extension-table.md) contiene tutte le estensioni del nome file utilizzate dall'applicazione insieme alle funzionalità e ai componenti associati.
-   La [tabella Verb](verb-table.md) associa le informazioni sui verbi di comando con le estensioni di file elencate nella [tabella di estensione](extension-table.md). Viene fornito un collegamento indiretto tra il verbo e la tabella delle funzionalità necessari per l'annuncio delle funzionalità.
-   La [tabella TypeLib](typelib-table.md) fornisce informazioni che il programma di installazione inserisce nel registro di sistema per la registrazione delle librerie dei tipi. Le voci della libreria dei tipi non vengono scritte al momento dell'annuncio. Il programma di installazione scrive le voci della libreria dei tipi al momento dell'installazione dei componenti associati alla libreria.
-   La [tabella MIME](mime-table.md) associa un tipo di contesto MIME a un CLSID o a un'estensione del nome di file. In questo modo viene fornito un percorso tra la tabella MIME e la tabella delle funzionalità necessaria per l'annuncio delle funzionalità.
-   La [tabella SelfReg](selfreg-table.md) fornisce le informazioni necessarie per la registrazione automatica dei moduli. La registrazione automatica viene fornita dal programma di installazione solo per compatibilità con le versioni precedenti e non è consigliata come metodo per popolare il registro di sistema, tuttavia, se nell'applicazione sono presenti moduli che devono registrarsi, utilizzare la tabella SelfReg.
-   La [tabella delle classi](class-table.md) viene utilizzata per registrare gli ID di classe e altre informazioni per gli oggetti com. Questa tabella contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto.
-   La [tabella ProgId](progid-table.md) associa gli ID del programma agli ID di classe.
-   La [tabella AppID](appid-table.md) viene utilizzata per registrare le impostazioni di configurazione e sicurezza comuni per gli oggetti DCOM.
-   La [tabella Environment](environment-table.md) viene utilizzata per impostare i valori delle variabili di ambiente e in Windows 2000 anche la tabella Environment scrive nel registro di sistema.
-   La [tabella del registro](registry-table.md) di sistema include tutte le altre informazioni che l'applicazione deve inserire nel registro di sistema. Sono incluse le impostazioni predefinite, le informazioni utente o i dati oppure la registrazione COM non supportata dalle tabelle precedenti.
-   La [tabella RemoveRegistry](removeregistry-table.md) contiene le informazioni del registro di sistema che l'applicazione deve eliminare dal registro di sistema al momento dell'installazione.

 

 



