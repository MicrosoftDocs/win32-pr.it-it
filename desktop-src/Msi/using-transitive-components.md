---
description: Un utilizzo tipico per i componenti transitivi consiste nel preparare un prodotto da reinstallare durante un aggiornamento del sistema.
ms.assetid: 73677573-945f-4646-89d8-93e28f7856fe
title: Utilizzo di componenti transitivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35982aafd486a62ce8560e507b8b6caf88e32591
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103969012"
---
# <a name="using-transitive-components"></a>Utilizzo di componenti transitivi

Un utilizzo tipico per i componenti transitivi consiste nel preparare un prodotto da reinstallare durante un aggiornamento del sistema. L'autore del pacchetto di installazione specifica i componenti che devono essere scambiati durante un aggiornamento del sistema con l'attributo transitivo. Quando l'utente aggiorna il sistema in un secondo momento, è necessario reinstallare il prodotto. Al momento della reinstallazione, il programma di installazione rimuove i componenti precedenti e installa i componenti successivi senza dover installare l'intero prodotto.

**Per includere due componenti transitivi nel pacchetto di installazione**

1.  Includere entrambi i componenti transitivi nel pacchetto di installazione.
2.  Creare entrambi i componenti transitivi nella [tabella dei componenti](component-table.md) in modo analogo ai componenti normali. Ogni componente transitivo deve avere un proprio GUID univoco specificato nella colonna ComponentId.
3.  Includere il bit **msidbComponentAttributesTransitive** nella colonna Attributes della tabella Component per ogni componente transitivo. Se questo bit è impostato, il programma di installazione rivaluterà il valore dell'istruzione nella colonna condizione durante una reinstallazione.

    Se il valore era in precedenza false e è stato modificato in true, il programma di installazione installerà il componente.

    Se il valore era in precedenza true ed è stato modificato in false, il programma di installazione rimuove il componente anche se il componente dispone di altri prodotti come client.

    > [!Note]  
    > A meno che non sia impostato il bit transitivo, il componente rimane abilitato una volta installato anche se l'istruzione condizionale restituisce false durante un'installazione di manutenzione successiva del prodotto. Le condizioni devono essere basate solo sugli Stati del computer. Non utilizzare con le condizioni basate sugli stati utente o sulle proprietà impostate nella riga di comando, in quanto ciò può causare la reinstallazione del prodotto da parte del programma di installazione per ogni utilizzo da parte di un altro utente.

     

4.  Immettere espressioni condizionali complementari nei campi condizione della tabella dei controlli in modo che quando la condizione sul primo componente transitivo viene modificata in false, la condizione sul secondo componente transitivo diventa true. Ciò comporta la rimozione del primo componente e l'installazione del secondo componente dopo la reinstallazione dell'applicazione.

Una reinstallazione del prodotto è necessaria per cambiare i componenti transitivi. Gli autori di pacchetti devono quindi fornire agli utenti un metodo per reinstallare il prodotto e per impostare le modalità della proprietà [**REINSTALLMODE**](reinstallmode.md) . Esistono sostanzialmente tre modi per attivare la reinstallazione:

-   Eseguire e configurare la reinstallazione tramite l'interfaccia utente mediante la creazione di un pacchetto che utilizza l'interfaccia utente [*completa*](f-gly.md).
-   Eseguire la reinstallazione dalla riga di comando usando **msiexec/f** e selezionare le modalità dall'elenco per l' [opzione della riga di comando](command-line-options.md) **/f** .
-   Chiedere all'applicazione di chiamare [**MsiReInstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) o [**MsiReInstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

Il bit deve essere utilizzato solo con condizioni basate sugli Stati del computer. Non utilizzare con le condizioni basate sugli stati utente o sulle proprietà impostate nella riga di comando, in quanto ciò può causare la reinstallazione del prodotto da parte del programma di installazione per ogni utilizzo da parte di un altro utente.

> [!Note]
> A meno che non sia impostato il bit transitivo nella colonna attributi per un componente, il componente rimane abilitato una volta installato anche se l'istruzione condizionale nella colonna condizione restituisce false in un'installazione di manutenzione successiva del prodotto.
> 
> Nella maggior parte dei casi, se un'applicazione include componenti transitivi, Windows Installer richiede l'origine dell'applicazione per la riparazione o l'aggiornamento dell'applicazione. In questi casi, il CD-ROM di ripristino del sistema fornito da un produttore di apparecchiature originale non funziona ed è necessario fornire un'origine di installazione effettiva per l'applicazione.

 

 

 



