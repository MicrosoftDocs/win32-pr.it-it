---
description: Un uso tipico per i componenti transitivi è preparare un prodotto da reinstallare durante un aggiornamento del sistema.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Uso di componenti transitivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ad6906b3e5d29ba6c0e3f8e279f4a1df2d5578f931219b6962062efaabd375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622889"
---
# <a name="using-transitive-components"></a>Uso di componenti transitivi

Un uso tipico per i componenti transitivi è preparare un prodotto da reinstallare durante un aggiornamento del sistema. L'autore del pacchetto di installazione specifica i componenti che devono essere scambiati durante un aggiornamento del sistema come con l'attributo transitivo. Quando l'utente aggiorna il sistema in un secondo momento, il prodotto deve essere reinstallato. Al momento della reinstallazione, il programma di installazione rimuove i componenti precedenti e installa i componenti successivi, senza dover installare l'intero prodotto.

**Per includere due componenti transitivi nel pacchetto di installazione**

1.  Includere entrambi i componenti transitivi nel pacchetto di installazione.
2.  Creare entrambi i componenti transitivi nella [tabella Component](component-table.md) allo stesso modo dei componenti normali. Ogni componente transitivo deve avere il proprio GUID univoco specificato nella colonna ComponentId.
3.  Includere il bit **msidbComponentAttributesTransitive** nella colonna Attributi della tabella Component per ogni componente transitivo. Se questo bit è impostato, il programma di installazione rivaluta il valore dell'istruzione nella colonna Condizione dopo una reinstallazione.

    Se in precedenza il valore era False ed è stato modificato in True, il programma di installazione installa il componente.

    Se in precedenza il valore era True ed è stato modificato in False, il programma di installazione rimuove il componente anche se il componente ha altri prodotti come client.

    > [!Note]  
    > A meno che non sia impostato il bit transitivo, il componente rimane abilitato dopo l'installazione anche se l'istruzione condizionale restituisce False in una successiva installazione di manutenzione del prodotto. Le condizioni devono essere basate solo sugli stati del computer. Non usare con condizioni basate sugli stati utente o sulle proprietà impostate nella riga di comando perché ciò può causare la richiesta di una reinstallazione del prodotto da parte di un altro utente a ogni uso da parte del programma di installazione.

     

4.  Immettere espressioni condizionali complementari nei campi Condizione della tabella Controllo in modo che, quando la condizione del primo componente transitivo viene impostata su False, la condizione del secondo componente transitivo passi a True. Ciò comporta la rimozione del primo componente e l'installazione del secondo componente al momento della reinstallazione dell'applicazione.

Una reinstallazione del prodotto è necessaria per cambiare i componenti transitivi. Gli autori di pacchetti devono quindi fornire agli utenti un metodo per reinstallare il prodotto e impostare le modalità della [**proprietà REINSTALLMODE.**](reinstallmode.md) Esistono fondamentalmente tre modi per attivare la reinstallazione:

-   Eseguire e configurare la reinstallazione tramite l'interfaccia utente mediante la creazione di un pacchetto che usa [*l'interfaccia utente completa.*](f-gly.md)
-   Eseguire la reinstallazione dalla riga di comando usando **msiexec /f** e selezionare le modalità dall'elenco per l'opzione della riga [di comando](command-line-options.md) **/f** .
-   Fare in modo che [**l'applicazione chiami MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) [**o MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

Il bit deve essere usato solo con condizioni basate sugli stati del computer. Non usare con condizioni basate sugli stati utente o sulle proprietà impostate nella riga di comando perché ciò può causare la richiesta di una reinstallazione del prodotto da parte di un altro utente a ogni uso da parte del programma di installazione.

> [!Note]
> A meno che il bit transitivo nella colonna Attributi non sia impostato per un componente, il componente rimane abilitato dopo l'installazione anche se l'istruzione condizionale nella colonna Condizione restituisce False in una successiva installazione di manutenzione del prodotto.
> 
> Nella maggior parte dei casi, se un'applicazione include componenti transitivi, Windows programma di installazione richiede l'origine dell'applicazione per ripristinare o aggiornare l'applicazione. In questi casi, il CD-ROM di ripristino del sistema fornito da un produttore di apparecchiature originale non funziona e deve essere fornita un'origine di installazione effettiva per l'applicazione.

 

 

 



