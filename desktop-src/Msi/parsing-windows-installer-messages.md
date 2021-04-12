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
# <a name="parsing-windows-installer-messages"></a><span data-ttu-id="de2bc-103">Analisi di messaggi di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="de2bc-103">Parsing Windows Installer Messages</span></span>

<span data-ttu-id="de2bc-104">Un gestore dell'interfaccia utente esterno può elaborare l'elenco dei messaggi del programma di installazione specificati dal parametro *dwMessagedFilter* della funzione [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="de2bc-104">An external UI handler can process the list of installer messages specified by the *dwMessagedFilter* parameter of the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span> <span data-ttu-id="de2bc-105">Alcuni di questi messaggi contengono stringhe che possono essere usate direttamente e altri messaggi possono essere analizzati ed elaborati dal gestore dell'interfaccia utente esterno per essere utili.</span><span class="sxs-lookup"><span data-stu-id="de2bc-105">Some of these messages contain strings that can be used directly, and other messages may need to be parsed and processed by the external UI handler to be useful.</span></span> <span data-ttu-id="de2bc-106">Il gestore dell'interfaccia utente esterno può solo dover monitorare Windows Installer messaggi senza eseguire alcuna operazione che influisca sull'installazione.</span><span class="sxs-lookup"><span data-stu-id="de2bc-106">Your external UI handler may only need to monitor Windows Installer messages without performing any operation that affects the installation.</span></span>

<span data-ttu-id="de2bc-107">I messaggi di Windows Installer seguenti contengono stringhe che possono essere visualizzate da una finestra di dialogo e che non richiedono alcuna elaborazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="de2bc-107">The following Windows Installer messages contain strings that can be displayed by a dialog box and need no additional processing.</span></span> <span data-ttu-id="de2bc-108">Questi messaggi contengono un elenco di pulsanti e icone che devono essere visualizzati da una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="de2bc-108">These messages contain a list of buttons and icons that are to be displayed by a dialog box.</span></span> <span data-ttu-id="de2bc-109">È possibile usare i valori di **MB \_ ICONMASK**, **MB \_ DEFMASK** e **MB \_ TYPEMASK** per specificare icone e pulsanti.</span><span class="sxs-lookup"><span data-stu-id="de2bc-109">You can use the **MB\_ICONMASK**, **MB\_DEFMASK**, and **MB\_TYPEMASK** values to specify icons and buttons.</span></span>

<dl> <dt>

<span data-ttu-id="de2bc-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**\_FATALEXIT INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE\_FATALEXIT**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-111">Si è verificata una chiusura prematura dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="de2bc-111">Premature termination of installation has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**\_errore INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-113">Messaggio di errore formattato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-113">Formatted error message.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**avviso di INSTALLMESSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="de2bc-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE\_WARNING**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-115">Messaggio di avviso formattato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-115">Formatted warning message.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**\_informazioni INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-117">Messaggio del log formattato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-117">Formatted log message.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_utente INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-119">Messaggio utente formattato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-119">Formatted user message.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**\_OUTOFDISKSPACE INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE\_OUTOFDISKSPACE**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-121">Messaggio formattato che indica una condizione di spazio su disco insufficiente</span><span class="sxs-lookup"><span data-stu-id="de2bc-121">Formatted message indicating an out of disk space condition</span></span>

</dd> </dl>

<span data-ttu-id="de2bc-122">Il gestore utenti esterno può utilizzare i messaggi di Windows Installer seguenti per monitorare una sequenza dell'interfaccia utente Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="de2bc-122">The external user handler can use the following Windows Installer messages to monitor a sequence of the Windows Installer UI.</span></span> <span data-ttu-id="de2bc-123">Il programma di installazione invia questi messaggi all'inizio di una sequenza di interfaccia utente di Windows Installer, perché ogni finestra di dialogo viene visualizzata e alla fine della sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-123">The installer sends these messages at the start of a Windows Installer UI sequence, as each dialog box is displayed, and at the end of the UI sequence.</span></span> <span data-ttu-id="de2bc-124">Non è necessaria alcuna elaborazione per usare questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="de2bc-124">No processing is required to use these messages.</span></span>

<dl> <dt>

<span data-ttu-id="de2bc-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>\_terminazione INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="de2bc-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE\_TERMINATE</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-126">Questo messaggio indica la fine della sequenza dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-126">This message indicates the end of the UI sequence.</span></span> <span data-ttu-id="de2bc-127">La stringa è una stringa null.</span><span class="sxs-lookup"><span data-stu-id="de2bc-127">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>\_inizializzazione INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="de2bc-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-129">Questo messaggio indica che la sequenza dell'interfaccia utente è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="de2bc-129">This message indicates that the UI sequence has started.</span></span> <span data-ttu-id="de2bc-130">La stringa è una stringa null.</span><span class="sxs-lookup"><span data-stu-id="de2bc-130">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE \_ SHOWDIALOG</span><span class="sxs-lookup"><span data-stu-id="de2bc-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE\_SHOWDIALOG</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-132">La stringa contiene il nome della finestra di dialogo corrente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-132">The string contains the name of the current dialog box.</span></span>

</dd> </dl>

<span data-ttu-id="de2bc-133">Per i messaggi di Windows Installer seguenti è necessaria un'ulteriore elaborazione da parte del gestore dell'interfaccia utente esterno.</span><span class="sxs-lookup"><span data-stu-id="de2bc-133">The following Windows Installer messages require additional processing by the external UI handler.</span></span>

<dl> <dt>

<span data-ttu-id="de2bc-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**\_RESOLVESOURCE INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE\_RESOLVESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-135">Il gestore dell'interfaccia utente esterno deve restituire 0 e consentire Windows Installer di gestire il messaggio.</span><span class="sxs-lookup"><span data-stu-id="de2bc-135">The external user interface handler must return 0 and allow Windows Installer to handle the message.</span></span> <span data-ttu-id="de2bc-136">Il gestore dell'interfaccia utente esterno può monitorare questo messaggio, ma non deve eseguire alcuna azione che influisca sull'installazione.</span><span class="sxs-lookup"><span data-stu-id="de2bc-136">The external user interface handler can monitor for this message, but it should not perform any action that affects the installation .</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**filesinus INSTALLMESSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="de2bc-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE\_FILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-138">L'interfaccia utente esterna dovrebbe visualizzare una [finestra di dialogo filesinus](filesinuse-dialog.md) in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="de2bc-138">The external UI should display a [FilesInUse dialog](filesinuse-dialog.md) in response to this message.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**\_RMFILESINUSE INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE\_RMFILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-140">L'interfaccia utente esterna dovrebbe visualizzare una [finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="de2bc-140">The external UI should display a [MsiRMFilesInUse dialog](msirmfilesinuse-dialog.md) in response to this message.</span></span> <span data-ttu-id="de2bc-141">Disponibile a partire dalla versione Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="de2bc-141">Available beginning with Windows Installer version 4.0.</span></span> <span data-ttu-id="de2bc-142">Per ulteriori informazioni su questo messaggio, vedere [utilizzo di gestione riavvio con un'interfaccia utente esterna](using-restart-manager-with-an-external-ui-.md).</span><span class="sxs-lookup"><span data-stu-id="de2bc-142">For more information about this message see [Using Restart Manager with an External UI](using-restart-manager-with-an-external-ui-.md).</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**\_ACTIONSTART INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE\_ACTIONSTART**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-144">Questo messaggio fornisce informazioni sull'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-144">This message gives information about the current action.</span></span> <span data-ttu-id="de2bc-145">Il formato è Action \[ 1 \] : \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="de2bc-145">The format is Action \[1\]: \[2\].</span></span> <span data-ttu-id="de2bc-146">\[3 \] , dove vengono usati i due punti per separare il campo 1 e il campo 2 e viene usato un punto per separare il campo 2 e il campo 3.</span><span class="sxs-lookup"><span data-stu-id="de2bc-146">\[3\], where a colon is used to separate Field 1 and Field 2 and a period is used to separate Field 2 and Field 3.</span></span> <span data-ttu-id="de2bc-147">Il campo \[ 1 \] contiene l'ora in cui l'azione è stata avviata utilizzando il formato della proprietà [**ora**](time.md) .</span><span class="sxs-lookup"><span data-stu-id="de2bc-147">Field \[1\] contains the time the action was started using the [**Time**](time.md) property format.</span></span> <span data-ttu-id="de2bc-148">Il campo \[ 2 \] contiene il nome dell'azione dalla tabella di sequenza.</span><span class="sxs-lookup"><span data-stu-id="de2bc-148">Field \[2\] contains the action's name from the sequence table.</span></span> <span data-ttu-id="de2bc-149">Il campo \[ 3 \] restituisce la descrizione dell'azione dalla [tabella ActionText](actiontext-table.md) o dalla funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="de2bc-149">Field \[3\] gives the action's description from the [ActionText table](actiontext-table.md) or from the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**\_ACTIONDATA INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE\_ACTIONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-151">Il formato di questa stringa viene specificato dal valore del [modello](template.md) fornito nella [tabella ActionText](actiontext-table.md) o dalla funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="de2bc-151">The format of this string is specified by the [Template](template.md) value provided in the [ActionText table](actiontext-table.md) or by the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="de2bc-152">Dopo il messaggio **\_ ACTIONSTART di INSTALLMESSAGE** può essere presente un numero illimitato di messaggi **\_ ACTIONDATA di INSTALLMESSAGE** .</span><span class="sxs-lookup"><span data-stu-id="de2bc-152">There can be an unlimited number of **INSTALLMESSAGE\_ACTIONDATA** messages after the **INSTALLMESSAGE\_ACTIONSTART** message.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**\_COMMONDATA INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="de2bc-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE\_COMMONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-154">Questo messaggio ha tre sottotipi: Language, Caption e CancelShow.</span><span class="sxs-lookup"><span data-stu-id="de2bc-154">This message has three subtypes: Language, Caption, and CancelShow.</span></span> <span data-ttu-id="de2bc-155">La stringa può contenere tre campi delimitati da un numero seguito da due punti.</span><span class="sxs-lookup"><span data-stu-id="de2bc-155">The string can have three fields delimited by a number followed by a colon.</span></span> <span data-ttu-id="de2bc-156">Non tutti i campi sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="de2bc-156">Not all fields are required.</span></span> <span data-ttu-id="de2bc-157">Il messaggio può essere una stringa NULL o vuota ("").</span><span class="sxs-lookup"><span data-stu-id="de2bc-157">The message can be a NULL or empty ("") string.</span></span>

<dl> <dt>

<span data-ttu-id="de2bc-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio</span><span class="sxs-lookup"><span data-stu-id="de2bc-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-159">Il campo 1 contiene il valore 0 per indicare che questa stringa contiene informazioni sulla lingua.</span><span class="sxs-lookup"><span data-stu-id="de2bc-159">Field 1 contains the value 0 to indicate this string contains language information.</span></span> <span data-ttu-id="de2bc-160">Il campo 2 contiene un valore di [lingua](language.md) che corrisponde a un identificatore di lingua numerico (LangID). Il campo 3 è un valore che rappresenta una tabella codici ANSI.</span><span class="sxs-lookup"><span data-stu-id="de2bc-160">Field 2 contains a [Language](language.md) value that is a numeric language identifier (LANGID.) Field 3 is a value that represents an ANSI code page.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Didascalia</span><span class="sxs-lookup"><span data-stu-id="de2bc-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Caption</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-162">Il campo 1 contiene il valore 1 per indicare che questa stringa contiene il testo di una didascalia o di un titolo.</span><span class="sxs-lookup"><span data-stu-id="de2bc-162">Field 1 contains the value 1 to indicate this string contains the text of a caption or title.</span></span> <span data-ttu-id="de2bc-163">Il campo 2 contiene il testo che un gestore dell'interfaccia utente esterno può utilizzare come didascalia di titolo per una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="de2bc-163">Field 2 contains text that an external UI handler can use as a caption of title for a dialog box.</span></span> <span data-ttu-id="de2bc-164">Il campo 3 è NULL o una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="de2bc-164">Field 3 is NULL or an empty ("") string.</span></span> <span data-ttu-id="de2bc-165">Il campo 3 può essere assente da un messaggio didascalia.</span><span class="sxs-lookup"><span data-stu-id="de2bc-165">Field 3 can be absent from a the Caption message.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span><span class="sxs-lookup"><span data-stu-id="de2bc-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-167">Il campo 1 contiene il valore 2 per indicare che questa stringa contiene informazioni sull'eventuale visualizzazione del pulsante Annulla.</span><span class="sxs-lookup"><span data-stu-id="de2bc-167">Field 1 contains the value 2 to indicate this string contains information about whether to display the cancel button.</span></span> <span data-ttu-id="de2bc-168">Se il pulsante Annulla deve essere nascosto, il campo 2 contiene il valore 0.</span><span class="sxs-lookup"><span data-stu-id="de2bc-168">If the cancel button should be hidden, Field 2 contains the value 0.</span></span> <span data-ttu-id="de2bc-169">Se il pulsante Annulla deve essere visibile, il campo 2 contiene il valore 1.</span><span class="sxs-lookup"><span data-stu-id="de2bc-169">If the cancel button should be visible, Field 2 contains the value 1.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="de2bc-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>\_stato INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="de2bc-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE\_PROGRESS</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-171">Questo messaggio ha quattro sottotipi: Reset, ActionInfo, ProgressReport e ProgressAddition.</span><span class="sxs-lookup"><span data-stu-id="de2bc-171">This message has four subtypes: Reset, ActionInfo, ProgressReport, and ProgressAddition.</span></span> <span data-ttu-id="de2bc-172">Il gestore esterno non deve agire su uno di questi messaggi fino a quando non viene ricevuto il primo messaggio di stato di reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="de2bc-172">The external handler should not act upon any of these messages until the first a Reset progress message is received.</span></span> <span data-ttu-id="de2bc-173">Viene fornita una stima del numero totale di cicli per l'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-173">This provides an estimate of the total number of ticks for the progress bar.</span></span>

<dl> <dt>

<span data-ttu-id="de2bc-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reimpostazione</span><span class="sxs-lookup"><span data-stu-id="de2bc-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reset</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-175">Il campo 1 contiene il valore 0 per indicare la reimpostazione dell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-175">Field 1 contains the value 0 to indicate a reset of the progress bar.</span></span> <span data-ttu-id="de2bc-176">Il campo 2 contiene il numero totale di cicli nell'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-176">Field 2 contains the total number of ticks in the progress bar.</span></span> <span data-ttu-id="de2bc-177">Il campo 3 contiene il valore 0 per il movimento dell'indicatore di stato in avanti.</span><span class="sxs-lookup"><span data-stu-id="de2bc-177">Field 3 contains the value 0 for forward progress bar motion.</span></span> <span data-ttu-id="de2bc-178">Il campo 3 contiene il valore 1 per il movimento dell'indicatore di stato precedente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-178">Field 3 contains the value 1 for backward progress bar motion.</span></span> <span data-ttu-id="de2bc-179">Il valore 0 nel campo 4 indica che l'installazione è in corso e che è possibile calcolare il tempo rimanente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-179">The value 0 in Field 4 means the installation is in progress and the time remaining may be calculated.</span></span> <span data-ttu-id="de2bc-180">Il valore 1 nel campo 4 indica che lo script è in esecuzione e un "attendere..." il messaggio può essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-180">The value 1 in Field 4 means script is being run and a "Please wait ..." message can be displayed.</span></span> <span data-ttu-id="de2bc-181">La stima del numero totale di cicli è un'approssimazione e potrebbe non essere corretta.</span><span class="sxs-lookup"><span data-stu-id="de2bc-181">The estimate of the total number of ticks is an approximation and may be inaccurate.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span><span class="sxs-lookup"><span data-stu-id="de2bc-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-183">Il campo 1 contiene il valore 1 per indicare che questa stringa contiene informazioni sull'azione.</span><span class="sxs-lookup"><span data-stu-id="de2bc-183">Field 1 contains the value 1 to indicate this string contains action information.</span></span> <span data-ttu-id="de2bc-184">Il campo 2 contiene il numero di cicli che l'indicatore di stato sposta per ogni messaggio ActionData inviato dall'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-184">Field 2 contains the number of ticks the progress bar moves for each ActionData message sent by the current action.</span></span> <span data-ttu-id="de2bc-185">Se il campo 3 contiene il valore 0, ignorare il campo 2.</span><span class="sxs-lookup"><span data-stu-id="de2bc-185">If Field 3 contains the value 0, ignore Field 2.</span></span> <span data-ttu-id="de2bc-186">Se il campo 3 contiene il valore 1, incrementare l'indicatore di stato in base al numero di cicli nel campo 2 per ogni messaggio ActionData inviato dall'azione corrente.</span><span class="sxs-lookup"><span data-stu-id="de2bc-186">If Field 3 contains the value 1, increment the progress bar by the number of ticks in Field 2 for each ActionData message sent by the current action.</span></span> <span data-ttu-id="de2bc-187">Il campo 4 non è usato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-187">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span><span class="sxs-lookup"><span data-stu-id="de2bc-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-189">Il campo 1 contiene il valore 2 per indicare che questa stringa contiene informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="de2bc-189">Field 1 contains the value 2 to indicate this string contains progress information.</span></span> <span data-ttu-id="de2bc-190">Il campo 2 contiene il numero di cicli spostati che l'indicatore di stato è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-190">Field 2 contains the number of ticks the progress bar has moved.</span></span> <span data-ttu-id="de2bc-191">Il campo 3 non è usato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-191">Field 3 is unused.</span></span> <span data-ttu-id="de2bc-192">Il campo 4 non è usato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-192">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="de2bc-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="de2bc-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span></span>
</dt> <dd>

<span data-ttu-id="de2bc-194">Il campo 1 contiene il valore 3 per indicare che un'azione può aggiungere un segno di avanzamento all'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-194">Field 1 contains the value 3 to indicate that an action can add ticks the progress bar.</span></span> <span data-ttu-id="de2bc-195">Il campo 2 contiene il numero di cicli da aggiungere al conteggio totale previsto dei cicli di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="de2bc-195">Field 2 contains the number of ticks to add to total expected count of progress ticks.</span></span> <span data-ttu-id="de2bc-196">Il campo 3 non è usato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-196">Field 3 is unused.</span></span> <span data-ttu-id="de2bc-197">Il campo 4 non è usato.</span><span class="sxs-lookup"><span data-stu-id="de2bc-197">Field 4 is unused.</span></span>

</dd> </dl> </dd> </dl>

 

 



