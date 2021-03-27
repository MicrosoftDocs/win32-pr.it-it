---
description: In questo argomento viene descritto come utilizzare il verificatore del tipo di file fornito in Windows 7 SDK.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Come utilizzare il tipo di file Verifier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104234395"
---
# <a name="how-to-use-the-file-type-verifier"></a>Come utilizzare il tipo di file Verifier

In questo argomento viene descritto come utilizzare il verificatore del tipo di file fornito in [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Se il programma crea tipi di file con cui gli utenti si aspettano di interagire dalla shell di Windows (in genere archiviati in una cartella nota dell'utente, ad esempio **documenti**), è molto importante testare l'applicazione e verificare che i file creati siano registrati correttamente e fornire un'esperienza utente di alta qualità durante l'esplorazione e la ricerca di file. Questo è particolarmente importante se si prevede che gli utenti eseguano le applicazioni in Windows 7, che si basa su gestori di tipi di file di alta qualità per molte delle funzionalità della shell.

Per verificare il tipo di file utilizzando il tipo di file Verifier, attenersi alla seguente procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Installare l'applicazione nell'ambiente di test e copiare il tipo di file Verifier in tale ambiente. Il verificatore del tipo di file è disponibile in [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

### <a name="step-2"></a>Passaggio 2:

Usare l'applicazione per creare un file da testare.

### <a name="step-3"></a>Passaggio 3:

Avviare il Verifier del tipo di file.

### <a name="step-4"></a>Passaggio 4:

Selezionare la categoria per il tipo di file, come illustrato nella schermata seguente.

![Screenshot che mostra la funzione di trascinamento della selezione.](images/file-assoc/filetypeverifier1.png)

La selezione della categoria determina il set di test che verranno eseguiti dallo strumento. Se il tipo può rientrare in più di una categoria, ad esempio un file TIF può essere un'immagine o un documento a seconda del contenuto, eseguire di nuovo lo strumento con ogni categoria appropriata.

### <a name="step-5"></a>Passaggio 5:

Utilizzando Esplora risorse, individuare un file da testare e utilizzare il mouse per trascinarlo nella destinazione in tipo di file Verifier, come illustrato nella schermata seguente.

![screenshot che mostra la funzione di trascinamento della selezione](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Passaggio 6:

Attendere che lo strumento File Type Verifier continui a eseguire una serie di test. Lo stato di avanzamento del test viene visualizzato dall'indicatore di stato, come nello screenshot seguente.

![screenshot che mostra l'indicatore di stato](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Passaggio 7:

Esaminare il riepilogo dei risultati dei test del tipo di file di documento, come illustrato nella schermata seguente.

![screenshot che mostra il riepilogo dei risultati](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Passaggio 8:

Fare clic su uno dei risultati nella pagina Riepilogo per visualizzare il log dettagliato. Uno dei log di esempio per un gestore di anteprime è illustrato nella schermata seguente.

![screenshot che mostra il log del gestore di anteprime](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Passaggio 9:

Per salvare una copia del file di log, fare clic su **Salva file di log** nella parte inferiore della visualizzazione del log e scegliere un percorso appropriato per archiviarlo nel computer.

### <a name="step-10"></a>Passaggio 10:

Se vengono segnalati errori, apportare le modifiche appropriate all'applicazione ed eseguire di nuovo lo strumento per verificare che gli errori non vengano più visualizzati nei test. Se vengono restituiti avvisi, valutarli e decidere se sono rilevanti per il tipo di file specifico e apportare le modifiche appropriate all'applicazione in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



