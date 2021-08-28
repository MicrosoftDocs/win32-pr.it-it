---
description: È possibile eseguire il debug di azioni personalizzate basate su librerie a collegamento dinamico usando gli strumenti di debug per Windows. Non è possibile usare il debug dinamico con azioni personalizzate basate su file eseguibili o script.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Debug di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781aaa5bfc8303175e7addfee730908c581575fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887015"
---
# <a name="debugging-custom-actions"></a>Debug di azioni personalizzate

È possibile eseguire il debug di azioni personalizzate basate su [librerie a collegamento dinamico](dynamic-link-libraries.md) usando gli [strumenti di debug per Windows](https://www.microsoft.com/?ref=go). Non è possibile usare il debug dinamico con azioni personalizzate basate su [file eseguibili](executable-files.md) o [script](scripts.md).

Le tecniche descritte in questa sezione consentono di eseguire il debug Windows azioni personalizzate del programma di installazione. Per informazioni sugli strumenti di debug per Windows, vedere la [](https://www.microsoft.com/?ref=go)sezione Driver Development Tools (Strumenti di sviluppo driver) di Windows Driver Kit (WDK).

Windows Il programma di installazione usa la variabile di ambiente MsiBreak per determinare l'azione personalizzata di cui eseguire il debug. Se si ha accesso al codice sorgente dell'azione personalizzata, è possibile usare il debug senza MsiBreak. Per avviare il debug senza MsiBreak, inserire una finestra di messaggio temporanea all'inizio del codice dell'azione. Quando viene visualizzata la finestra di messaggio durante l'installazione, collegare il debugger al processo proprietario della finestra di messaggio. È quindi possibile impostare i punti di interruzione necessari e chiudere la finestra di messaggio per riprendere l'esecuzione. Non è possibile eseguire il debug delle parti precedenti dell'azione personalizzata con questo metodo.

Per usare la variabile di ambiente MsiBreak per eseguire il debug dell'azione personalizzata, impostare MsiBreak sul nome dell'azione personalizzata nella [tabella CustomAction](customaction-table.md). MsiBreak può essere una variabile di ambiente di sistema o utente. Se la variabile è impostata come variabile di sistema, potrebbe essere necessario riavviare il sistema quando il valore viene modificato per rilevare il nuovo valore.

Per usare la variabile di ambiente MsiBreak per eseguire il debug di un'interfaccia utente incorporata, impostare il valore di MsiBreak su MsiEmbeddedUI.

Windows Il programma di installazione controlla la variabile di ambiente MsiBreak solo se l'utente è un amministratore. Il programma di installazione ignora il valore di MsiBreak se l'utente non è un amministratore, anche se si tratta di [*un'applicazione gestita.*](m-gly.md)

Se si esegue il debug di un'azione personalizzata eseguita con privilegi di sistema elevati nella sequenza di esecuzione, collegare il debugger al servizio Windows Installer. Quando si esegue il debug di un'azione personalizzata eseguita con privilegi rappresentati nella sequenza di esecuzione, il sistema richiede una finestra di dialogo che indica quale processo deve essere eseguito il debug. All'utente viene visualizzata una finestra di dialogo che indica il processo di cui eseguire il debug. Per altre informazioni sulle azioni personalizzate con privilegi elevati, vedere [Sicurezza delle azioni personalizzate.](custom-action-security.md)

Dopo che il debugger è stato collegato al processo corretto, il programma di installazione attiva un punto di interruzione del debugger immediatamente prima di chiamare il punto di ingresso della DLL. In corrispondenza del punto di interruzione, la DLL è già caricata nel processo e viene determinato l'indirizzo del punto di ingresso. Se non è stato possibile caricare la DLL dell'azione personalizzata o se il punto di ingresso dell'azione personalizzata non esiste, non viene attivato alcun punto di interruzione. Poiché il punto di interruzione viene attivato prima di chiamare la funzione DLL, dopo l'attivazione del punto di interruzione è necessario usare il debugger per procedere fino a quando non viene chiamato il punto di ingresso dell'azione personalizzata. In alternativa, è possibile impostare un punto di interruzione in qualsiasi punto dell'azione personalizzata e riprendere l'esecuzione normale.

Il Windows di installazione esegue LE DLL non archiviate nella [tabella Binary](binary-table.md) direttamente dal percorso della DLL. Il programma di installazione non conosce il nome originale di una DLL archiviata nella tabella Binary ed esegue l'azione personalizzata dll con un nome di file temporaneo. Il formato del nome del file temporaneo è MSI?????. TMP. In Windows XP, questo file temporaneo viene archiviato in una posizione sicura, in genere &lt; WindowsFolder &gt; \\ Installer.

Si noti che molte DLL create per il debug contengono il nome e il percorso del file PDB corrispondente come parte della DLL stessa. Quando si esegue il debug di questo tipo di DLL in un sistema in cui il PDB si trova nel percorso archiviato nella DLL, i simboli possono essere caricati automaticamente dallo strumento del debugger. Nelle situazioni in cui non è possibile trovare il file PDB nel percorso archiviato, in cui il debugger non supporta il caricamento dei simboli dal percorso archiviato o in cui la DLL non è stata compilata con le informazioni di debug, potrebbe essere necessario inserire i file di simboli nella cartella con il file DLL temporaneo.

Il programma di installazione aggiunge le informazioni di debug per gli script delle azioni personalizzate al file di log di installazione.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



