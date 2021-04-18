---
description: È possibile eseguire il debug di azioni personalizzate basate su librerie a collegamento dinamico mediante gli strumenti di debug per Windows. Non è possibile utilizzare il debug dinamico con azioni personalizzate basate su file eseguibili o script.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Debug di azioni personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ddfbc9952f0dd7fc1b85b5c64fa6a23381ceafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314294"
---
# <a name="debugging-custom-actions"></a>Debug di azioni personalizzate

È possibile eseguire il debug di azioni personalizzate basate su [librerie a collegamento dinamico](dynamic-link-libraries.md) mediante [gli strumenti di debug per Windows](https://www.microsoft.com/?ref=go). Non è possibile utilizzare il debug dinamico con azioni personalizzate basate su [file eseguibili](executable-files.md) o [script](scripts.md).

Le tecniche descritte in questa sezione consentono di eseguire il debug di Windows Installer azioni personalizzate. Per informazioni sugli [strumenti di debug per Windows](https://www.microsoft.com/?ref=go), vedere la sezione strumenti di sviluppo driver di Windows Driver Kit (WDK).

Windows Installer usa la variabile di ambiente MsiBreak per determinare quale azione personalizzata deve essere sottoposta a debug. Se si ha accesso al codice sorgente dell'azione personalizzata, potrebbe essere possibile usare il debug senza MsiBreak. Per avviare il debug senza MsiBreak, inserire una finestra di messaggio temporanea all'inizio del codice dell'azione. Quando viene visualizzata la finestra di messaggio durante l'installazione, alleghi il debugger al processo proprietario della finestra di messaggio. È quindi possibile impostare eventuali punti di interruzione necessari e chiudere la finestra di messaggio per riprendere l'esecuzione. Non è possibile eseguire il debug delle parti precedenti dell'azione personalizzata da questo metodo.

Per usare la variabile di ambiente MsiBreak per eseguire il debug dell'azione personalizzata, impostare MsiBreak sul nome dell'azione personalizzata nella [tabella CustomAction](customaction-table.md). MsiBreak può essere una variabile di ambiente di sistema o utente. Se la variabile è impostata come variabile di sistema, potrebbe essere necessario riavviare il sistema quando il valore viene modificato per rilevare il nuovo valore.

Per usare la variabile di ambiente MsiBreak per eseguire il debug di un'interfaccia utente incorporata, impostare il valore di MsiBreak su MsiEmbeddedUI.

Windows Installer controlla solo la variabile di ambiente MsiBreak se l'utente è un amministratore. Il programma di installazione ignora il valore di MsiBreak se l'utente non è un amministratore, anche se si tratta di un' [*applicazione gestita*](m-gly.md).

Se si esegue il debug di un'azione personalizzata che viene eseguita con privilegi elevati (di sistema) nella sequenza di esecuzione, associare il debugger al servizio Windows Installer. Quando si esegue il debug di un'azione personalizzata eseguita con privilegi rappresentati nella sequenza di esecuzione, il sistema richiede una finestra di dialogo che indica il processo di cui eseguire il debug. All'utente viene visualizzata una finestra di dialogo che indica il processo di cui eseguire il debug. Per altre informazioni sulle azioni personalizzate con privilegi elevati, vedere [sicurezza dell'azione personalizzata](custom-action-security.md).

Una volta che il debugger è stato collegato al processo corretto, il programma di installazione attiva un punto di interruzione del debugger immediatamente prima di chiamare il punto di ingresso della DLL. Nel punto di interruzione, la DLL è già caricata nel processo e l'indirizzo del punto di ingresso è stato determinato. Se non è stato possibile caricare la DLL dell'azione personalizzata oppure il punto di ingresso dell'azione personalizzata non esiste, non viene attivato alcun punto di interruzione. Poiché il punto di interruzione viene attivato prima di chiamare la funzione DLL, dopo che il punto di interruzione è stato attivato, è consigliabile utilizzare il debugger per proseguire fino a quando non viene chiamato il punto di ingresso dell'azione personalizzata. In alternativa, è possibile impostare un punto di interruzione in qualsiasi punto dell'azione personalizzata e riprendere l'esecuzione normale.

Il Windows Installer esegue le dll non memorizzate nella [tabella binaria](binary-table.md) direttamente dal percorso della dll. Il programma di installazione non conosce il nome originale di una DLL archiviata nella tabella binaria ed esegue l'azione personalizzata DLL con un nome file temporaneo. Il formato del nome file temporaneo è MSI?????. TMP. In Windows XP, questo file temporaneo viene archiviato in un percorso sicuro, in genere <WindowFolder> \\ programma di installazione.

Si noti che molte DLL create per il debug contengono il nome e il percorso del file PDB corrispondente come parte della DLL. Quando si esegue il debug di questo tipo di DLL in un sistema in cui il file PDB è disponibile nel percorso archiviato nella DLL, è possibile che i simboli vengano caricati automaticamente dallo strumento del debugger. Nelle situazioni in cui il PDB non è stato trovato nel percorso archiviato, in cui il debugger non supporta il caricamento di simboli dal percorso archiviato o in cui la DLL non è stata compilata con le informazioni di debug, potrebbe essere necessario inserire i file di simboli nella cartella con il file DLL temporaneo.

Il programma di installazione aggiunge le informazioni di debug per gli script di azione personalizzati al file di log dell'installazione.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



