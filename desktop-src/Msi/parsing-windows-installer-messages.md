---
description: Un gestore dell'interfaccia utente esterno può elaborare l'elenco dei messaggi del programma di installazione specificati dal parametro dwMessagedFilter della funzione MsiSetExternalUI.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Analisi di messaggi di Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226854"
---
# <a name="parsing-windows-installer-messages"></a>Analisi di messaggi di Windows Installer

Un gestore dell'interfaccia utente esterno può elaborare l'elenco dei messaggi del programma di installazione specificati dal parametro *dwMessagedFilter* della funzione [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) . Alcuni di questi messaggi contengono stringhe che possono essere usate direttamente e altri messaggi possono essere analizzati ed elaborati dal gestore dell'interfaccia utente esterno per essere utili. Il gestore dell'interfaccia utente esterno può solo dover monitorare Windows Installer messaggi senza eseguire alcuna operazione che influisca sull'installazione.

I messaggi di Windows Installer seguenti contengono stringhe che possono essere visualizzate da una finestra di dialogo e che non richiedono alcuna elaborazione aggiuntiva. Questi messaggi contengono un elenco di pulsanti e icone che devono essere visualizzati da una finestra di dialogo. È possibile usare i valori di **MB \_ ICONMASK**, **MB \_ DEFMASK** e **MB \_ TYPEMASK** per specificare icone e pulsanti.

<dl> <dt>

<span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**\_FATALEXIT INSTALLMESSAGE**
</dt> <dd>

Si è verificata una chiusura prematura dell'installazione.

</dd> <dt>

<span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**\_errore INSTALLMESSAGE**
</dt> <dd>

Messaggio di errore formattato.

</dd> <dt>

<span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**avviso di INSTALLMESSAGE \_**
</dt> <dd>

Messaggio di avviso formattato.

</dd> <dt>

<span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**\_informazioni INSTALLMESSAGE**
</dt> <dd>

Messaggio del log formattato.

</dd> <dt>

<span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_utente INSTALLMESSAGE**
</dt> <dd>

Messaggio utente formattato.

</dd> <dt>

<span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**\_OUTOFDISKSPACE INSTALLMESSAGE**
</dt> <dd>

Messaggio formattato che indica una condizione di spazio su disco insufficiente

</dd> </dl>

Il gestore utenti esterno può utilizzare i messaggi di Windows Installer seguenti per monitorare una sequenza dell'interfaccia utente Windows Installer. Il programma di installazione invia questi messaggi all'inizio di una sequenza di interfaccia utente di Windows Installer, perché ogni finestra di dialogo viene visualizzata e alla fine della sequenza dell'interfaccia utente. Non è necessaria alcuna elaborazione per usare questi messaggi.

<dl> <dt>

<span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>\_terminazione INSTALLMESSAGE
</dt> <dd>

Questo messaggio indica la fine della sequenza dell'interfaccia utente. La stringa è una stringa null.

</dd> <dt>

<span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>\_inizializzazione INSTALLMESSAGE
</dt> <dd>

Questo messaggio indica che la sequenza dell'interfaccia utente è stata avviata. La stringa è una stringa null.

</dd> <dt>

<span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG
</dt> <dd>

La stringa contiene il nome della finestra di dialogo corrente.

</dd> </dl>

Per i messaggi di Windows Installer seguenti è necessaria un'ulteriore elaborazione da parte del gestore dell'interfaccia utente esterno.

<dl> <dt>

<span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**\_RESOLVESOURCE INSTALLMESSAGE**
</dt> <dd>

Il gestore dell'interfaccia utente esterno deve restituire 0 e consentire Windows Installer di gestire il messaggio. Il gestore dell'interfaccia utente esterno può monitorare questo messaggio, ma non deve eseguire alcuna azione che influisca sull'installazione.

</dd> <dt>

<span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**filesinus INSTALLMESSAGE \_**
</dt> <dd>

L'interfaccia utente esterna dovrebbe visualizzare una [finestra di dialogo filesinus](filesinuse-dialog.md) in risposta a questo messaggio.

</dd> <dt>

<span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**\_RMFILESINUSE INSTALLMESSAGE**
</dt> <dd>

L'interfaccia utente esterna dovrebbe visualizzare una [finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) in risposta a questo messaggio. Disponibile a partire dalla versione Windows Installer 4,0. Per ulteriori informazioni su questo messaggio, vedere [utilizzo di gestione riavvio con un'interfaccia utente esterna](using-restart-manager-with-an-external-ui-.md).

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**\_ACTIONSTART INSTALLMESSAGE**
</dt> <dd>

Questo messaggio fornisce informazioni sull'azione corrente. Il formato è Action \[ 1 \] : \[ 2 \] . \[3 \] , dove vengono usati i due punti per separare il campo 1 e il campo 2 e viene usato un punto per separare il campo 2 e il campo 3. Il campo \[ 1 \] contiene l'ora in cui l'azione è stata avviata utilizzando il formato della proprietà [**ora**](time.md) . Il campo \[ 2 \] contiene il nome dell'azione dalla tabella di sequenza. Il campo \[ 3 \] restituisce la descrizione dell'azione dalla [tabella ActionText](actiontext-table.md) o dalla funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**\_ACTIONDATA INSTALLMESSAGE**
</dt> <dd>

Il formato di questa stringa viene specificato dal valore del [modello](template.md) fornito nella [tabella ActionText](actiontext-table.md) o dalla funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . Dopo il messaggio **\_ ACTIONSTART di INSTALLMESSAGE** può essere presente un numero illimitato di messaggi **\_ ACTIONDATA di INSTALLMESSAGE** .

</dd> <dt>

<span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**\_COMMONDATA INSTALLMESSAGE**
</dt> <dd>

Questo messaggio ha tre sottotipi: Language, Caption e CancelShow. La stringa può contenere tre campi delimitati da un numero seguito da due punti. Non tutti i campi sono obbligatori. Il messaggio può essere una stringa NULL o vuota ("").

<dl> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio
</dt> <dd>

Il campo 1 contiene il valore 0 per indicare che questa stringa contiene informazioni sulla lingua. Il campo 2 contiene un valore di [lingua](language.md) che corrisponde a un identificatore di lingua numerico (LangID). Il campo 3 è un valore che rappresenta una tabella codici ANSI.

</dd> <dt>

<span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Didascalia
</dt> <dd>

Il campo 1 contiene il valore 1 per indicare che questa stringa contiene il testo di una didascalia o di un titolo. Il campo 2 contiene il testo che un gestore dell'interfaccia utente esterno può utilizzare come didascalia di titolo per una finestra di dialogo. Il campo 3 è NULL o una stringa vuota (""). Il campo 3 può essere assente da un messaggio didascalia.

</dd> <dt>

<span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow
</dt> <dd>

Il campo 1 contiene il valore 2 per indicare che questa stringa contiene informazioni sull'eventuale visualizzazione del pulsante Annulla. Se il pulsante Annulla deve essere nascosto, il campo 2 contiene il valore 0. Se il pulsante Annulla deve essere visibile, il campo 2 contiene il valore 1.

</dd> </dl> </dd> <dt>

<span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>\_stato INSTALLMESSAGE
</dt> <dd>

Questo messaggio ha quattro sottotipi: Reset, ActionInfo, ProgressReport e ProgressAddition. Il gestore esterno non deve agire su uno di questi messaggi fino a quando non viene ricevuto il primo messaggio di stato di reimpostazione. Viene fornita una stima del numero totale di cicli per l'indicatore di stato.

<dl> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reimpostazione
</dt> <dd>

Il campo 1 contiene il valore 0 per indicare la reimpostazione dell'indicatore di stato. Il campo 2 contiene il numero totale di cicli nell'indicatore di stato. Il campo 3 contiene il valore 0 per il movimento dell'indicatore di stato in avanti. Il campo 3 contiene il valore 1 per il movimento dell'indicatore di stato precedente. Il valore 0 nel campo 4 indica che l'installazione è in corso e che è possibile calcolare il tempo rimanente. Il valore 1 nel campo 4 indica che lo script è in esecuzione e un "attendere..." il messaggio può essere visualizzato. La stima del numero totale di cicli è un'approssimazione e potrebbe non essere corretta.

</dd> <dt>

<span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo
</dt> <dd>

Il campo 1 contiene il valore 1 per indicare che questa stringa contiene informazioni sull'azione. Il campo 2 contiene il numero di cicli che l'indicatore di stato sposta per ogni messaggio ActionData inviato dall'azione corrente. Se il campo 3 contiene il valore 0, ignorare il campo 2. Se il campo 3 contiene il valore 1, incrementare l'indicatore di stato in base al numero di cicli nel campo 2 per ogni messaggio ActionData inviato dall'azione corrente. Il campo 4 non è usato.

</dd> <dt>

<span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport
</dt> <dd>

Il campo 1 contiene il valore 2 per indicare che questa stringa contiene informazioni sullo stato di avanzamento. Il campo 2 contiene il numero di cicli spostati che l'indicatore di stato è stato spostato. Il campo 3 non è usato. Il campo 4 non è usato.

</dd> <dt>

<span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition
</dt> <dd>

Il campo 1 contiene il valore 3 per indicare che un'azione può aggiungere un segno di avanzamento all'indicatore di stato. Il campo 2 contiene il numero di cicli da aggiungere al conteggio totale previsto dei cicli di avanzamento. Il campo 3 non è usato. Il campo 4 non è usato.

</dd> </dl> </dd> </dl>

 

 



