---
description: Questo argomento descrive come usare File Type Verifier fornito in Windows 7 SDK.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Come usare Il verificatore del tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af06de30d4fca2a9f5209d20e200153c061248576e7e94c8342cf9ae60e4f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223373"
---
# <a name="how-to-use-the-file-type-verifier"></a>Come usare Il verificatore del tipo di file

Questo argomento descrive come usare Il verificatore del tipo di file fornito in [Windows 7 SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Se il programma crea tipi di file con cui gli utenti dovrebbero interagire da Windows Shell (in genere archiviati nella cartella nota di un utente, ad esempio **Documenti**), è molto importante testare l'applicazione e verificare che i file creati siano registrati correttamente e offrire un'esperienza utente di alta qualità durante l'esplorazione e la ricerca dei file. Ciò è particolarmente importante se si prevede che gli utenti esercitino le applicazioni in Windows 7, che si basa su gestori di tipi di file di alta qualità per molte delle funzionalità di Shell.

Per verificare il tipo di file usando File Type Verifier, seguire questa procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Installare l'applicazione nell'ambiente di test e copiare File Type Verifier in tale ambiente. File Type Verifier è disponibile in [Windows 7 SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

### <a name="step-2"></a>Passaggio 2:

Usare l'applicazione per creare un file da testare.

### <a name="step-3"></a>Passaggio 3:

Avviare Il verificatore del tipo di file.

### <a name="step-4"></a>Passaggio 4:

Selezionare la categoria per il tipo di file, come illustrato nello screenshot seguente.

![Screenshot che mostra la funzione di trascinamento della selezione.](images/file-assoc/filetypeverifier1.png)

La selezione della categoria determina il set di test che verranno eseguiti dallo strumento. Se il tipo può rientrare in più categorie (ad esempio, un file TIF potrebbe essere un'immagine o un documento a seconda del contenuto), eseguire di nuovo lo strumento con ogni categoria appropriata.

### <a name="step-5"></a>Passaggio 5:

Usando Windows Explorer, individuare un file da testare e usare il mouse per trascinarlo nella destinazione in File Type Verifier, come illustrato nello screenshot seguente.

![Screenshot che mostra la funzione di trascinamento della selezione](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>Passaggio 6:

Attendere che lo strumento File Type Verifier proceda con una serie di test. Lo stato del test viene visualizzato dall'indicatore di stato, come nell'immagine riportata di seguito.

![Screenshot che mostra l'indicatore di stato](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>Passaggio 7:

Esaminare il riepilogo dei risultati dei test del tipo di file di documento, come illustrato nello screenshot seguente.

![Screenshot che mostra il riepilogo dei risultati](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>Passaggio 8:

Fare clic su uno dei risultati nella pagina di riepilogo per visualizzare il log dettagliato. Un log di esempio per un gestore di anteprima è illustrato nello screenshot seguente.

![Screenshot che mostra il log del gestore di anteprima](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>Passaggio 9:

Per salvare una copia del file di log, fare clic su Salva **file** di log nella parte inferiore della visualizzazione del log e scegliere un percorso appropriato per archiviarlo nel computer.

### <a name="step-10"></a>Passaggio 10:

Se vengono segnalati errori, apportare le modifiche appropriate nell'applicazione ed eseguire di nuovo lo strumento per verificare che gli errori non siano più visualizzati nei test. Se vengono segnalati avvisi, valutarli e decidere se sono rilevanti per il tipo di file specifico e apportare le modifiche appropriate all'applicazione in base alle esigenze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



