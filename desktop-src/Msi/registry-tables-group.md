---
description: Il gruppo del Registro di sistema di Windows installer contiene informazioni sulle voci del Registro di sistema.
ms.assetid: 31a75c20-79e4-4bcf-bcc1-34a7d191fa90
title: Gruppo tabelle del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7ab4d3447ec727271d53fabe44fee11bf96663170c89a2210d80bb02bd8c7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128977"
---
# <a name="registry-tables-group"></a>Gruppo tabelle del Registro di sistema

![gruppo di tabelle del Registro di sistema](images/registry.png)

Per altre informazioni su questo diagramma, vedere la [legenda del](entity-relationship-diagram-legend.md)diagramma delle relazioni tra entità .

Il programma di installazione include tabelle specifiche per i diversi tipi di voci del Registro di sistema. Quando si popola il gruppo di tabelle del Registro di sistema, [](registry-table.md) è importante provare a ridurre al minimo il numero di voci presenti nella tabella del Registro di sistema e ottimizzare l'uso delle altre tabelle del Registro di sistema specifiche. Ciò è dovuto al fatto che il programma di installazione non può distinguere tra tipi diversi di voci del Registro di sistema nella tabella Del Registro di sistema e non può usare la logica interna necessaria per sfruttare al meglio tutte le funzionalità del programma di installazione, ad esempio la [*pubblicità*](a-gly.md)di . La creazione di voci del Registro di sistema com e correlate alla shell in questo modo offre anche un'organizzazione più logica e consente di ridurre al minimo la registrazione errata delle informazioni sul server COM.

La figura mostra il gruppo di voci del Registro di sistema di tabelle, nonché [la tabella Component](component-table.md), la tabella [Feature](feature-table.md)e la [tabella File](file-table.md). Anche se questi ultimi non sono direttamente coinvolti nel popolamento del Registro di sistema, sono inclusi nella figura perché sono essenziali per la logica del gruppo di voci del Registro di sistema.

Il gruppo di voci del Registro di sistema contiene le tabelle seguenti di voci del Registro di sistema specifiche.

-   La [tabella Extension contiene](extension-table.md) tutte le estensioni di file utilizzate dall'applicazione insieme alle funzionalità e ai componenti associati.
-   La [tabella Verb](verb-table.md) associa le informazioni del verbo di comando alle estensioni di file elencate nella tabella [Estensione](extension-table.md). In questo modo viene fornito un collegamento indiretto tra la tabella Verbo e Funzionalità necessaria per l'annuncio delle funzionalità.
-   La [tabella TypeLib fornisce](typelib-table.md) informazioni che il programma di installazione inserisce nel Registro di sistema per la registrazione delle librerie dei tipi. Le voci della libreria dei tipi non vengono scritte al momento dell'annuncio. Il programma di installazione scrive le voci della libreria dei tipi al momento dell'installazione dei componenti associati alla libreria.
-   La [tabella MIME associa](mime-table.md) un tipo di contesto MIME a un CLSID o a un'estensione di file. In questo modo viene fornito un percorso tra MIME e La tabella delle funzionalità necessaria per l'annuncio delle funzionalità.
-   La [tabella SelfReg fornisce](selfreg-table.md) le informazioni necessarie per la registrazione automatica dei moduli. La registrazione automatica viene fornita dal programma di installazione solo per compatibilità con le versioni precedenti e non è consigliabile come metodo per popolare il Registro di sistema, tuttavia se nell'applicazione sono presenti moduli che devono registrarsi, usare la tabella SelfReg.
-   La [tabella Class viene](class-table.md) usata per registrare gli ID di classe e altre informazioni per gli oggetti COM. Questa tabella contiene informazioni relative al server COM che devono essere generate come parte dell'annuncio del prodotto.
-   La [tabella ProgId](progid-table.md) associa gli ID programma agli ID di classe.
-   La [tabella AppId viene](appid-table.md) usata per registrare le impostazioni di sicurezza e configurazione comuni per gli oggetti DCOM.
-   La [tabella Environment](environment-table.md) viene usata per impostare i valori delle variabili di ambiente e Windows 2000 la tabella Environment scrive anche nel Registro di sistema.
-   La [tabella Registro di](registry-table.md) sistema contiene tutte le altre informazioni che l'applicazione deve inserire nel Registro di sistema. Ciò include le impostazioni predefinite, le informazioni utente o i dati o la registrazione COM non supportata dalle tabelle precedenti.
-   La [tabella RemoveRegistry contiene](removeregistry-table.md) le informazioni del Registro di sistema che l'applicazione deve eliminare dal Registro di sistema in fase di installazione.

 

 



