---
description: I messaggi inviati tramite MsiProcessMessage sono gli stessi messaggi ricevuti dalla funzione di callback del \_ gestore INSTALLUI se è stato chiamato MsiSetExternalUI.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Inviare messaggi a Windows Installer tramite MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968577"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a><span data-ttu-id="e11b9-103">Invio di messaggi a Windows Installer tramite MsiProcessMessage</span><span class="sxs-lookup"><span data-stu-id="e11b9-103">Sending Messages to Windows Installer Using MsiProcessMessage</span></span>

<span data-ttu-id="e11b9-104">I messaggi inviati tramite [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) sono gli stessi messaggi ricevuti dalla funzione di callback [**del \_ gestore INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) se è stato chiamato [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="e11b9-104">The messages sent using [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are the same messages that are received by the [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) callback function if [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) was called.</span></span> <span data-ttu-id="e11b9-105">In caso contrario, Windows Installer gestisce i messaggi.</span><span class="sxs-lookup"><span data-stu-id="e11b9-105">Otherwise, Windows Installer handles the messages.</span></span> <span data-ttu-id="e11b9-106">Per informazioni dettagliate, vedere [analisi dei messaggi di Windows Installer](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e11b9-106">For details, see [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="e11b9-107">Ad esempio, per inviare un \_ messaggio di errore INSTALLMESSAGE con l' \_ icona MB ICONWARNING e i \_ pulsanti MB ABORTRETRYCANCEL:</span><span class="sxs-lookup"><span data-stu-id="e11b9-107">For example, to send an INSTALLMESSAGE\_ERROR message with the MB\_ICONWARNING icon and the MB\_ABORTRETRYCANCEL buttons:</span></span>


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



<span data-ttu-id="e11b9-108">Dove *hinstall* è l'handle per l'installazione, fornito a un'azione personalizzata o all'handle *hProduct* da [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) o [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)e *hRec* è il record contenente le informazioni sull'errore da formattare.</span><span class="sxs-lookup"><span data-stu-id="e11b9-108">Where *hInstall* is the handle to the installation, provided to a custom action or the *hProduct* handle from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), and *hRec* is the record containing the error information to format.</span></span> <span data-ttu-id="e11b9-109">Per informazioni sul modo in cui viene eseguita la formattazione, vedere [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span><span class="sxs-lookup"><span data-stu-id="e11b9-109">For information on how formatting is performed, see [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span></span>

<span data-ttu-id="e11b9-110">Per impostazione predefinita, se \_ viene inviato un messaggio di errore INSTALLMESSAGE o INSTALLMESSAGE \_ FATALEXIT senza specificare tipi di pulsante o icone, MB \_ OK, nessuna icona e MB \_ DEFBUTTON1 vengono usati.</span><span class="sxs-lookup"><span data-stu-id="e11b9-110">By default, if an INSTALLMESSAGE\_ERROR or INSTALLMESSAGE\_FATALEXIT message is sent without specifying button type or icon types, MB\_OK, no icon, and MB\_DEFBUTTON1 are used.</span></span>

<span data-ttu-id="e11b9-111">Windows Installer non assegna un'etichetta al pulsante **Interrompi** con la stringa "Abort" durante la visualizzazione di un MessageBox con la \_ specifica del pulsante MB AbortRetryIgnore (, invece contrassegna il pulsante con la stringa "Cancel".</span><span class="sxs-lookup"><span data-stu-id="e11b9-111">Windows Installer does not label the **ABORT** button with the "Abort" string when displaying a MessageBox with the MB\_ABORTRETRYIGNORE button specification, instead it labels the button with the "Cancel" string.</span></span> <span data-ttu-id="e11b9-112">Tutti i messaggi di errore evitano di utilizzare la parola "Abort" e utilizzano invece la parola "Cancel".</span><span class="sxs-lookup"><span data-stu-id="e11b9-112">All error messages refrain from using the word "Abort" and instead use the word "Cancel".</span></span>

<span data-ttu-id="e11b9-113">Il parametro *hRecord* della funzione [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) dipende dal tipo di messaggio inviato a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="e11b9-113">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type sent to the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="e11b9-114">Nell'elenco seguente vengono illustrati in dettaglio i requisiti del record in relazione al tipo di messaggio:</span><span class="sxs-lookup"><span data-stu-id="e11b9-114">The following list details the requirements of the record in relation to the message type:</span></span>

<span data-ttu-id="e11b9-115">\_FATALEXIT INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-115">INSTALLMESSAGE\_FATALEXIT</span></span>

 

<span data-ttu-id="e11b9-116">\_informazioni INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-116">INSTALLMESSAGE\_INFO</span></span>

 

<span data-ttu-id="e11b9-117">\_OUTOFDISKSPACE INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-117">INSTALLMESSAGE\_OUTOFDISKSPACE</span></span>



| <span data-ttu-id="e11b9-118">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-118">Field</span></span>         | <span data-ttu-id="e11b9-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-119">Description</span></span>                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b9-120">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-120">0</span></span>             | <span data-ttu-id="e11b9-121">Modello per la formattazione della stringa risultante.</span><span class="sxs-lookup"><span data-stu-id="e11b9-121">Template for the formatting of the resultant string.</span></span> <span data-ttu-id="e11b9-122">Per ulteriori informazioni, vedere [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) .</span><span class="sxs-lookup"><span data-stu-id="e11b9-122">See [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) for more information.</span></span> <span data-ttu-id="e11b9-123">Si fa riferimento ai campi del record usando \[ 1 \] per il campo 1, \[ 2 \] per il campo 2 e così via.</span><span class="sxs-lookup"><span data-stu-id="e11b9-123">The fields of the record are referenced using \[1\] for field 1, \[2\] for field 2, etc.</span></span> |
| <span data-ttu-id="e11b9-124">da 1 a *n*</span><span class="sxs-lookup"><span data-stu-id="e11b9-124">1 through *n*</span></span> | <span data-ttu-id="e11b9-125">Tutti i campi successivi sono direttamente correlati ai campi a cui fa riferimento il modello nel campo 0.</span><span class="sxs-lookup"><span data-stu-id="e11b9-125">All subsequent fields are directly related to the fields referenced by the template in field 0.</span></span>                                                                                                                    |



 

<span data-ttu-id="e11b9-126">Se il campo 0 è null, la stringa ricevuta dal gestore dell'interfaccia utente viene formattata come: 1: \[ dati dal campo 1 \] 2: \[ dati dal campo 2 \] , ovvero per ogni campo del record, la stringa contiene il numero di campo seguito dai dati archiviati nel campo.</span><span class="sxs-lookup"><span data-stu-id="e11b9-126">If field 0 is null, the string received by the UI handler is formatted as: 1: \[data from field 1\] 2: \[data from field 2\] meaning that for each field of the record, the string contains the field number followed by the data stored in the field.</span></span>

<span data-ttu-id="e11b9-127">I messaggi informativi da [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) vengono registrati quando [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), l' [opzione della riga di comando](command-line-options.md)'/l ' o i [criteri di registrazione](logging.md) specificano le informazioni ' I ' o INSTALLLOGMODE \_ .</span><span class="sxs-lookup"><span data-stu-id="e11b9-127">Information messages from [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are logged when [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), the '/l' [command line option](command-line-options.md), or the [logging policy](logging.md) specify 'I' or INSTALLLOGMODE\_INFO.</span></span>

<span data-ttu-id="e11b9-128">\_errore INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-128">INSTALLMESSAGE\_ERROR</span></span>

 

<span data-ttu-id="e11b9-129">avviso di INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="e11b9-129">INSTALLMESSAGE\_WARNING</span></span>

 

<span data-ttu-id="e11b9-130">\_utente INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-130">INSTALLMESSAGE\_USER</span></span>

<span data-ttu-id="e11b9-131">Per utilizzare un messaggio della tabella degli errori.</span><span class="sxs-lookup"><span data-stu-id="e11b9-131">To use a message from the Error table.</span></span>



| <span data-ttu-id="e11b9-132">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-132">Field</span></span>         | <span data-ttu-id="e11b9-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-133">Description</span></span>                                           |
|---------------|-------------------------------------------------------|
| <span data-ttu-id="e11b9-134">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-134">0</span></span>             | <span data-ttu-id="e11b9-135">Deve essere null.</span><span class="sxs-lookup"><span data-stu-id="e11b9-135">Must be null.</span></span>                                         |
| <span data-ttu-id="e11b9-136">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-136">1</span></span>             | <span data-ttu-id="e11b9-137">Numero del messaggio nella [tabella degli errori](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="e11b9-137">Message number in the [Error table](error-table.md).</span></span> |
| <span data-ttu-id="e11b9-138">da 2 a *n*</span><span class="sxs-lookup"><span data-stu-id="e11b9-138">2 through *n*</span></span> | <span data-ttu-id="e11b9-139">Correlato al messaggio specificato nella tabella degli errori.</span><span class="sxs-lookup"><span data-stu-id="e11b9-139">Related to the specified message in the Error table.</span></span>  |



 

<span data-ttu-id="e11b9-140">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="e11b9-140">For example.</span></span>



| <span data-ttu-id="e11b9-141">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-141">Field</span></span> | <span data-ttu-id="e11b9-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="e11b9-142">Type</span></span>   | <span data-ttu-id="e11b9-143">Data</span><span class="sxs-lookup"><span data-stu-id="e11b9-143">Data</span></span>       |
|-------|--------|------------|
| <span data-ttu-id="e11b9-144">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-144">0</span></span>     | <span data-ttu-id="e11b9-145">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-145">string</span></span> | <span data-ttu-id="e11b9-146">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-146">null</span></span>       |
| <span data-ttu-id="e11b9-147">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-147">1</span></span>     | <span data-ttu-id="e11b9-148">INT</span><span class="sxs-lookup"><span data-stu-id="e11b9-148">int</span></span>    | <span data-ttu-id="e11b9-149">1304</span><span class="sxs-lookup"><span data-stu-id="e11b9-149">1304</span></span>       |
| <span data-ttu-id="e11b9-150">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-150">2</span></span>     | <span data-ttu-id="e11b9-151">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-151">string</span></span> | <span data-ttu-id="e11b9-152">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="e11b9-152">Myfile.txt</span></span> |



 

<span data-ttu-id="e11b9-153">Il messaggio risultante ricevuto dal gestore dell'interfaccia utente è:</span><span class="sxs-lookup"><span data-stu-id="e11b9-153">The resulting message received from the UI handler is:</span></span>

<span data-ttu-id="e11b9-154">Errore 1304.</span><span class="sxs-lookup"><span data-stu-id="e11b9-154">Error 1304.</span></span> <span data-ttu-id="e11b9-155">Errore durante la scrittura nel file: Myfile.txt.</span><span class="sxs-lookup"><span data-stu-id="e11b9-155">Error writing to file: Myfile.txt.</span></span> <span data-ttu-id="e11b9-156">Verificare di disporre dell'accesso a tale directory.</span><span class="sxs-lookup"><span data-stu-id="e11b9-156">Verify that you have access to that directory.</span></span>

<span data-ttu-id="e11b9-157">Se il campo 0 non è null, viene eseguito l'override del messaggio della tabella degli errori.</span><span class="sxs-lookup"><span data-stu-id="e11b9-157">If field 0 is not null, the message from the error table is overridden.</span></span> <span data-ttu-id="e11b9-158">Al contrario, il modello Field 0 determina il formato del messaggio.</span><span class="sxs-lookup"><span data-stu-id="e11b9-158">Instead, the field 0 template determines the format of the message.</span></span>

<span data-ttu-id="e11b9-159">Il messaggio può inoltre specificare i pulsanti, incluso il pulsante predefinito, e l'icona da usare con il messaggio come indicato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e11b9-159">The message may also specify the buttons, including the default button, and the icon for use with the message as mentioned above.</span></span> <span data-ttu-id="e11b9-160">I tipi di pulsante e icona sono elencati [**nel \_ gestore INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span><span class="sxs-lookup"><span data-stu-id="e11b9-160">The button and icon types are listed in [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span></span>

<span data-ttu-id="e11b9-161">\_COMMONDATA INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-161">INSTALLMESSAGE\_COMMONDATA</span></span>

<span data-ttu-id="e11b9-162">Questo messaggio viene inviato per abilitare o disabilitare il pulsante **Annulla** in una finestra di dialogo di stato.</span><span class="sxs-lookup"><span data-stu-id="e11b9-162">This message is sent to enable or disable the **Cancel** button in a progress dialog box.</span></span>



| <span data-ttu-id="e11b9-163">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-163">Field</span></span> | <span data-ttu-id="e11b9-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-164">Description</span></span>                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b9-165">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-165">0</span></span>     | <span data-ttu-id="e11b9-166">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e11b9-166">Unused.</span></span>                                                                                                                                      |
| <span data-ttu-id="e11b9-167">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-167">1</span></span>     | <span data-ttu-id="e11b9-168">2 si riferisce al pulsante **Annulla** .</span><span class="sxs-lookup"><span data-stu-id="e11b9-168">2 refers to the **Cancel** button.</span></span>                                                                                                           |
| <span data-ttu-id="e11b9-169">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-169">2</span></span>     | <span data-ttu-id="e11b9-170">Il valore 1 indica che il pulsante **Annulla** deve essere visibile.</span><span class="sxs-lookup"><span data-stu-id="e11b9-170">A value of 1 indicates the **Cancel** button should be visible.</span></span> <span data-ttu-id="e11b9-171">Il valore 0 indica che il pulsante **Annulla** deve essere invisibile.</span><span class="sxs-lookup"><span data-stu-id="e11b9-171">A value of 0 indicates the **Cancel** button should be invisible.</span></span><br/> |



 

<span data-ttu-id="e11b9-172">Ad esempio, per disabilitare o nascondere il pulsante **Annulla** , il record verrebbe visualizzato come segue.</span><span class="sxs-lookup"><span data-stu-id="e11b9-172">For example, to disable or hide the **Cancel** button, the record would appear as follows.</span></span>



| <span data-ttu-id="e11b9-173">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-173">Field</span></span> | <span data-ttu-id="e11b9-174">Tipo</span><span class="sxs-lookup"><span data-stu-id="e11b9-174">Type</span></span>   | <span data-ttu-id="e11b9-175">Data</span><span class="sxs-lookup"><span data-stu-id="e11b9-175">Data</span></span> |
|-------|--------|------|
| <span data-ttu-id="e11b9-176">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-176">0</span></span>     | <span data-ttu-id="e11b9-177">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-177">string</span></span> | <span data-ttu-id="e11b9-178">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-178">null</span></span> |
| <span data-ttu-id="e11b9-179">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-179">1</span></span>     | <span data-ttu-id="e11b9-180">INT</span><span class="sxs-lookup"><span data-stu-id="e11b9-180">int</span></span>    | <span data-ttu-id="e11b9-181">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-181">2</span></span>    |
| <span data-ttu-id="e11b9-182">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-182">2</span></span>     | <span data-ttu-id="e11b9-183">INT</span><span class="sxs-lookup"><span data-stu-id="e11b9-183">int</span></span>    | <span data-ttu-id="e11b9-184">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-184">0</span></span>    |



 

<span data-ttu-id="e11b9-185">\_ACTIONSTART INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-185">INSTALLMESSAGE\_ACTIONSTART</span></span>

 

<span data-ttu-id="e11b9-186">\_ACTIONDATA INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-186">INSTALLMESSAGE\_ACTIONDATA</span></span>

<span data-ttu-id="e11b9-187">Il \_ record ACTIONSTART di INSTALLMESSAGE determina il formato del record ActionData.</span><span class="sxs-lookup"><span data-stu-id="e11b9-187">The INSTALLMESSAGE\_ACTIONSTART record determines the format of the ActionData record.</span></span>



| <span data-ttu-id="e11b9-188">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-188">Field</span></span> | <span data-ttu-id="e11b9-189">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-189">Description</span></span>                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b9-190">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-190">0</span></span>     | <span data-ttu-id="e11b9-191">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-191">null</span></span>                                                                                                          |
| <span data-ttu-id="e11b9-192">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-192">1</span></span>     | <span data-ttu-id="e11b9-193">Nome dell'azione.</span><span class="sxs-lookup"><span data-stu-id="e11b9-193">Action name.</span></span> <span data-ttu-id="e11b9-194">Il nome in questo campo deve essere diverso da null.</span><span class="sxs-lookup"><span data-stu-id="e11b9-194">The name in this field must be non-null.</span></span>                                                         |
| <span data-ttu-id="e11b9-195">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-195">2</span></span>     | <span data-ttu-id="e11b9-196">Descrizione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="e11b9-196">Action description.</span></span>                                                                                           |
| <span data-ttu-id="e11b9-197">3</span><span class="sxs-lookup"><span data-stu-id="e11b9-197">3</span></span>     | <span data-ttu-id="e11b9-198">Modello di azione.</span><span class="sxs-lookup"><span data-stu-id="e11b9-198">Action template.</span></span> <span data-ttu-id="e11b9-199">Viene usato per ActionData il cui messaggio viene formattato in base a questo modello.</span><span class="sxs-lookup"><span data-stu-id="e11b9-199">This is used for the ActionData whose message is being formatted according to this template.</span></span> |



 

<span data-ttu-id="e11b9-200">Non fare riferimento al campo 0 nel messaggio del modello di azione.</span><span class="sxs-lookup"><span data-stu-id="e11b9-200">Do not reference field 0 in the Action template message.</span></span>

<span data-ttu-id="e11b9-201">Il \_ record INSTALLMESSAGE ACTIONDATA è formattato come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="e11b9-201">The INSTALLMESSAGE\_ACTIONDATA record is formatted as follows.</span></span>



| <span data-ttu-id="e11b9-202">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-202">Field</span></span>         | <span data-ttu-id="e11b9-203">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-203">Description</span></span>                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b9-204">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-204">0</span></span>             | <span data-ttu-id="e11b9-205">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-205">null</span></span>                                                                                                                                               |
| <span data-ttu-id="e11b9-206">da 1 a *n*</span><span class="sxs-lookup"><span data-stu-id="e11b9-206">1 through *n*</span></span> | <span data-ttu-id="e11b9-207">Dipendente dal campo 3 del \_ messaggio o del modello INSTALLMESSAGE ACTIONSTART corrispondente specificato nella [tabella ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="e11b9-207">Dependent upon field 3 of the corresponding INSTALLMESSAGE\_ACTIONSTART message or template specified in [ActionText table](actiontext-table.md).</span></span> |



 

<span data-ttu-id="e11b9-208">Ad esempio, il \_ record ACTIONSTART di INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="e11b9-208">For example, the INSTALLMESSAGE\_ACTIONSTART record.</span></span>



| <span data-ttu-id="e11b9-209">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-209">Field</span></span> | <span data-ttu-id="e11b9-210">Tipo</span><span class="sxs-lookup"><span data-stu-id="e11b9-210">Type</span></span>   | <span data-ttu-id="e11b9-211">Data</span><span class="sxs-lookup"><span data-stu-id="e11b9-211">Data</span></span>                                                            |
|-------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="e11b9-212">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-212">0</span></span>     | <span data-ttu-id="e11b9-213">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-213">string</span></span> | <span data-ttu-id="e11b9-214">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-214">null</span></span>                                                            |
| <span data-ttu-id="e11b9-215">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-215">1</span></span>     | <span data-ttu-id="e11b9-216">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-216">string</span></span> | <span data-ttu-id="e11b9-217">Azione</span><span class="sxs-lookup"><span data-stu-id="e11b9-217">MyAction</span></span>                                                        |
| <span data-ttu-id="e11b9-218">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-218">2</span></span>     | <span data-ttu-id="e11b9-219">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-219">string</span></span> | <span data-ttu-id="e11b9-220">Questa è la descrizione di "azione"</span><span class="sxs-lookup"><span data-stu-id="e11b9-220">This is the description of "MyAction"</span></span>                           |
| <span data-ttu-id="e11b9-221">3</span><span class="sxs-lookup"><span data-stu-id="e11b9-221">3</span></span>     | <span data-ttu-id="e11b9-222">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-222">string</span></span> | <span data-ttu-id="e11b9-223">Modello di azione: i dati di Field1 sono \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e11b9-223">MyAction template: field1 data is \[1\].</span></span> <span data-ttu-id="e11b9-224">i dati del campo 2 sono \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="e11b9-224">field 2 data is \[2\].</span></span> |



 

<span data-ttu-id="e11b9-225">Il modello per INSTALLMESSAGE \_ ACTIONSTART (Field 3) fa riferimento ai campi 1 e 2 \_ . il record INSTALLMESSAGE ACTIONDATA deve avere 2 campi contenenti i dati garantiti.</span><span class="sxs-lookup"><span data-stu-id="e11b9-225">The template for INSTALLMESSAGE\_ACTIONSTART (field 3) references fields 1 and 2, the INSTALLMESSAGE\_ACTIONDATA record should have 2 fields containing the warranted data.</span></span> <span data-ttu-id="e11b9-226">I campi possono essere di tipo String o Integer.</span><span class="sxs-lookup"><span data-stu-id="e11b9-226">The fields could be either string or integer fields.</span></span>

<span data-ttu-id="e11b9-227">\_Record ACTIONDATA INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="e11b9-227">INSTALLMESSAGE\_ACTIONDATA record.</span></span>



| <span data-ttu-id="e11b9-228">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-228">Field</span></span> | <span data-ttu-id="e11b9-229">Tipo</span><span class="sxs-lookup"><span data-stu-id="e11b9-229">Type</span></span>   | <span data-ttu-id="e11b9-230">Data</span><span class="sxs-lookup"><span data-stu-id="e11b9-230">Data</span></span>                    |
|-------|--------|-------------------------|
| <span data-ttu-id="e11b9-231">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-231">0</span></span>     | <span data-ttu-id="e11b9-232">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-232">string</span></span> | <span data-ttu-id="e11b9-233">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-233">null</span></span>                    |
| <span data-ttu-id="e11b9-234">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-234">1</span></span>     | <span data-ttu-id="e11b9-235">INT</span><span class="sxs-lookup"><span data-stu-id="e11b9-235">int</span></span>    | <span data-ttu-id="e11b9-236">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-236">2</span></span>                       |
| <span data-ttu-id="e11b9-237">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-237">2</span></span>     | <span data-ttu-id="e11b9-238">string</span><span class="sxs-lookup"><span data-stu-id="e11b9-238">string</span></span> | <span data-ttu-id="e11b9-239">ActionData per l'azione</span><span class="sxs-lookup"><span data-stu-id="e11b9-239">ActionData for MyAction</span></span> |



 

<span data-ttu-id="e11b9-240">filesinus INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="e11b9-240">INSTALLMESSAGE\_FILESINUSE</span></span>

<span data-ttu-id="e11b9-241">Il record filesinus è un record di lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="e11b9-241">The FILESINUSE record is a variable length record.</span></span>



| <span data-ttu-id="e11b9-242">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-242">Field</span></span> | <span data-ttu-id="e11b9-243">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-243">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b9-244">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-244">0</span></span>     | <span data-ttu-id="e11b9-245">Questo campo può essere null.</span><span class="sxs-lookup"><span data-stu-id="e11b9-245">This field can be null.</span></span> <span data-ttu-id="e11b9-246">Per un'installazione mediante un'interfaccia utente di base, questo campo può specificare testo statico da visualizzare nel [controllo ListBox](listbox-control.md) della [finestra di dialogo filesinus](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="e11b9-246">For an installation using a basic UI, this field may specify static text for display in the [ListBox control](listbox-control.md) of the [FilesInUse dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="e11b9-247">Per un'installazione che usa un'interfaccia utente completa, questo campo non ha alcun effetto perché il testo viene specificato dalla creazione della finestra di dialogo filesinusa personalizzata.</span><span class="sxs-lookup"><span data-stu-id="e11b9-247">For an installation using a full UI, this field has no effect because the text is specified by the authoring of the custom FilesInUse dialog box.</span></span> |
| <span data-ttu-id="e11b9-248">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-248">1</span></span>     | <span data-ttu-id="e11b9-249">Nome del file in uso.</span><span class="sxs-lookup"><span data-stu-id="e11b9-249">Name of the file in use.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e11b9-250">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-250">2</span></span>     | <span data-ttu-id="e11b9-251">Questo campo identifica il processo che contiene il file in uso. **Windows Installer versione 4,0:** ID processo (PID) del processo o titolo della finestra per il processo.</span><span class="sxs-lookup"><span data-stu-id="e11b9-251">This field identifies the process holding the file in use.**Windows Installer version 4.0:** The process id (PID) of the process, or the title of the window for the process.</span></span><br/> <span data-ttu-id="e11b9-252">**Windows Installer versione 3,1 e versioni precedenti:** Questo campo deve essere l'ID processo (PID) del processo.</span><span class="sxs-lookup"><span data-stu-id="e11b9-252">**Windows Installer version 3.1 and earlier:** This field must be the process id (PID) of the process.</span></span><br/>                                                      |



 

<span data-ttu-id="e11b9-253">Ad esempio, per inviare un messaggio filesinus che mostra due file in uso, red.exe e blue.exe, il record ha quattro campi e il campo 0.</span><span class="sxs-lookup"><span data-stu-id="e11b9-253">For example, to send a FilesInUse message showing two files in use, red.exe and blue.exe, the record has four fields plus the 0 field.</span></span> <span data-ttu-id="e11b9-254">Il formato del record sarà come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e11b9-254">The format of the record would be as shown in the following table.</span></span> <span data-ttu-id="e11b9-255">Questo esempio richiede Windows Installer versione 4,0.</span><span class="sxs-lookup"><span data-stu-id="e11b9-255">This example requires Windows Installer version 4.0.</span></span>

<span data-ttu-id="e11b9-256">**Windows Installer versione 3,1 e versioni precedenti:** I campi 2 e 4 nell'esempio seguente devono contenere i PID dei processi che mantengono red.exe e blue.exe in uso.</span><span class="sxs-lookup"><span data-stu-id="e11b9-256">**Windows Installer version 3.1 and earlier:** Fields 2 and 4 in the following example must contain the PIDs of the processes holding red.exe and blue.exe in use.</span></span>



| <span data-ttu-id="e11b9-257">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-257">Field</span></span> | <span data-ttu-id="e11b9-258">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-258">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="e11b9-259">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-259">0</span></span>     | <span data-ttu-id="e11b9-260">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-260">null</span></span>              |
| <span data-ttu-id="e11b9-261">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-261">1</span></span>     | <span data-ttu-id="e11b9-262">Red.exe</span><span class="sxs-lookup"><span data-stu-id="e11b9-262">Red.exe</span></span>           |
| <span data-ttu-id="e11b9-263">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-263">2</span></span>     | <span data-ttu-id="e11b9-264">Titolo della finestra rossa</span><span class="sxs-lookup"><span data-stu-id="e11b9-264">Red Window Title</span></span>  |
| <span data-ttu-id="e11b9-265">3</span><span class="sxs-lookup"><span data-stu-id="e11b9-265">3</span></span>     | <span data-ttu-id="e11b9-266">Blue.exe</span><span class="sxs-lookup"><span data-stu-id="e11b9-266">Blue.exe</span></span>          |
| <span data-ttu-id="e11b9-267">4</span><span class="sxs-lookup"><span data-stu-id="e11b9-267">4</span></span>     | <span data-ttu-id="e11b9-268">Titolo della finestra blu</span><span class="sxs-lookup"><span data-stu-id="e11b9-268">Blue Window Title</span></span> |



 

> [!Note]  
> <span data-ttu-id="e11b9-269">In Windows Installer versione 4,0, se il PID passato dal servizio non ha un titolo della finestra, ad esempio un'applicazione della barra di sistema, il file non viene visualizzato e il log dettagliato contiene i messaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="e11b9-269">On Windows Installer version 4.0, if the PID passed from the service does not have a window title, such as a system tray application, the file is not be displayed and the verbose log contains the following messages.</span></span>

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

<span data-ttu-id="e11b9-270">\_RESOLVESOURCE INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="e11b9-270">INSTALLMESSAGE\_RESOLVESOURCE</span></span>

<span data-ttu-id="e11b9-271">Il \_ record RESOLVESOURCE di INSTALLMESSAGE include sette campi.</span><span class="sxs-lookup"><span data-stu-id="e11b9-271">The INSTALLMESSAGE\_RESOLVESOURCE record has seven fields.</span></span> <span data-ttu-id="e11b9-272">Per \_ il corretto funzionamento di INSTALLMESSAGE RESOLVESOURCE, un gestore dell'interfaccia utente esterno potrebbe non gestire il \_ messaggio RESOLVESOURCE di INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="e11b9-272">For INSTALLMESSAGE\_RESOLVESOURCE to work correctly, an external UI handler may not handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="e11b9-273">Windows Installer necessario gestire il \_ messaggio INSTALLMESSAGE RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="e11b9-273">Windows Installer must handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="e11b9-274">Ovvero, il gestore dell'interfaccia utente esterno restituisce 0 per indicare che non viene eseguita alcuna azione quando si filtra il \_ messaggio INSTALLMESSAGE RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="e11b9-274">That is, the external UI handler returns 0 to indicate "no action taken" when filtering the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="e11b9-275">La procedura consigliata consiste nell'evitare di inviare un messaggio RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="e11b9-275">The best practice is to avoid sending a RESOLVESOURCE message.</span></span>



| <span data-ttu-id="e11b9-276">Campo</span><span class="sxs-lookup"><span data-stu-id="e11b9-276">Field</span></span> | <span data-ttu-id="e11b9-277">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e11b9-277">Description</span></span>                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b9-278">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-278">0</span></span>     | <span data-ttu-id="e11b9-279">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-279">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="e11b9-280">1</span><span class="sxs-lookup"><span data-stu-id="e11b9-280">1</span></span>     | <span data-ttu-id="e11b9-281">Null</span><span class="sxs-lookup"><span data-stu-id="e11b9-281">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="e11b9-282">2</span><span class="sxs-lookup"><span data-stu-id="e11b9-282">2</span></span>     | <span data-ttu-id="e11b9-283">Il nome del package.</span><span class="sxs-lookup"><span data-stu-id="e11b9-283">Package name.</span></span>                                                                                                                                                      |
| <span data-ttu-id="e11b9-284">3</span><span class="sxs-lookup"><span data-stu-id="e11b9-284">3</span></span>     | <span data-ttu-id="e11b9-285">Codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="e11b9-285">Product code.</span></span>                                                                                                                                                      |
| <span data-ttu-id="e11b9-286">4</span><span class="sxs-lookup"><span data-stu-id="e11b9-286">4</span></span>     | <span data-ttu-id="e11b9-287">Percorso relativo, se noto, può essere null.</span><span class="sxs-lookup"><span data-stu-id="e11b9-287">Relative path if known, can be null.</span></span>                                                                                                                               |
| <span data-ttu-id="e11b9-288">5</span><span class="sxs-lookup"><span data-stu-id="e11b9-288">5</span></span>     | <span data-ttu-id="e11b9-289">0</span><span class="sxs-lookup"><span data-stu-id="e11b9-289">0</span></span>                                                                                                                                                                  |
| <span data-ttu-id="e11b9-290">6</span><span class="sxs-lookup"><span data-stu-id="e11b9-290">6</span></span>     | <span data-ttu-id="e11b9-291">Indica se convalidare il codice del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="e11b9-291">Whether to validate the package code.</span></span> <span data-ttu-id="e11b9-292">Il valore ' 1' indica che il codice del pacchetto deve essere convalidato.</span><span class="sxs-lookup"><span data-stu-id="e11b9-292">A value of '1' indicates the package code should be validated.</span></span> <span data-ttu-id="e11b9-293">Il valore ' 0' indica che il pacchetto non deve essere convalidato.</span><span class="sxs-lookup"><span data-stu-id="e11b9-293">A value of '0' indicates the package should not be validated.</span></span> |
| <span data-ttu-id="e11b9-294">7</span><span class="sxs-lookup"><span data-stu-id="e11b9-294">7</span></span>     | <span data-ttu-id="e11b9-295">Disco richiesto dalla tabella dei supporti.</span><span class="sxs-lookup"><span data-stu-id="e11b9-295">Required disk from media table.</span></span> <span data-ttu-id="e11b9-296">Il valore ' 0' indica che qualsiasi disco è accettabile.</span><span class="sxs-lookup"><span data-stu-id="e11b9-296">A value of '0' indicates that any disk is acceptable.</span></span>                                                                              |



 

 

 




