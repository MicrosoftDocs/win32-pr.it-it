---
description: È possibile fornire tutte le informazioni necessarie per configurare installazione applicazioni nel pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto di Windows Installer dell'applicazione.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configurazione di installazione applicazioni con Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/30/2021
ms.locfileid: "106334296"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a><span data-ttu-id="d3ef2-103">Configurazione di installazione applicazioni con Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d3ef2-103">Configuring Add/Remove Programs with Windows Installer</span></span>

<span data-ttu-id="d3ef2-104">È possibile fornire tutte le informazioni necessarie per configurare installazione applicazioni nel pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto di Windows Installer dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-104">You can supply all of the information needed to configure Add/Remove Programs in Control Panel by setting the values of certain installer properties in your application's Windows Installer package.</span></span> <span data-ttu-id="d3ef2-105">L'impostazione di queste proprietà scrive automaticamente i valori corrispondenti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-105">Setting these properties automatically writes the corresponding values into the registry.</span></span> <span data-ttu-id="d3ef2-106">Se il programma di installazione rileva che il prodotto è contrassegnato per la rimozione completa, le operazioni vengono aggiunte automaticamente allo script per rimuovere la cartella Aggiungi/Rimuovi programmi nel pannello di controllo informazioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-106">If the installer detects that the product is marked for complete removal, operations are automatically added to the script to remove the Add/Remove Programs folder in Control Panel information for the product.</span></span>

<span data-ttu-id="d3ef2-107">Se un'applicazione non è registrata, non è elencata in Installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-107">If an application is not registered, it is not listed in Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="d3ef2-108">Per ulteriori informazioni, vedere [aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="d3ef2-108">For more information, see [Adding and Removing an Application and Leaving No Trace in the Registry](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span></span>

<span data-ttu-id="d3ef2-109">Le applicazioni installate nel [contesto di installazione](installation-context.md) per utente vengono visualizzate in Installazione applicazioni dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-109">Applications that have been installed in the per-user [installation context](installation-context.md) are displayed in the Add/Remove Programs of the current user.</span></span> <span data-ttu-id="d3ef2-110">Le applicazioni che sono state installate nel contesto di installazione per computer vengono visualizzate in Installazione applicazioni di tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-110">Applications that have been installed in the per-machine installation context are displayed in the Add/Remove Programs of all users.</span></span> <span data-ttu-id="d3ef2-111">Le applicazioni che non sono state installate per computer e sono state installate solo come applicazioni per utente per utenti diversi dall'utente corrente, non vengono visualizzate nell'installazione applicazioni dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-111">Applications that have not been installed per-machine, and have only been installed as per-user applications for users other than the current user, do not appear in the Add/Remove Programs of the current user.</span></span>

<span data-ttu-id="d3ef2-112">Si noti che i pacchetti di installazione che usano la proprietà [**LIMITUI**](limitui.md) devono anche contenere [**ARPNOMODIFY**](arpnomodify.md).</span><span class="sxs-lookup"><span data-stu-id="d3ef2-112">Note that installation packages that use the [**LIMITUI**](limitui.md) property must also contain the [**ARPNOMODIFY**](arpnomodify.md).</span></span> <span data-ttu-id="d3ef2-113">Questa operazione è necessaria affinché un utente ottenga il comportamento corretto da installazione applicazioni nell'utilità pannello di controllo durante il tentativo di configurazione di un prodotto.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-113">This is required for a user to obtain the correct behavior from Add/Remove Programs in Control Panel utility when attempting to configure a product.</span></span>

<span data-ttu-id="d3ef2-114">Il programma di installazione usa le seguenti [proprietà pubbliche](public-properties.md) per gestire installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-114">The installer uses the following [public properties](public-properties.md) to manage Add/Remove Programs in Control Panel.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3ef2-115">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="d3ef2-115">Property name</span></span></th>
<th><span data-ttu-id="d3ef2-116">Breve descrizione della proprietà</span><span class="sxs-lookup"><span data-stu-id="d3ef2-116">Brief description of property</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3ef2-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-118">URL del canale di aggiornamento per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-118">URL of the update channel for the application.</span></span> <span data-ttu-id="d3ef2-119">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-119">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ef2-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-121">Fornisce commenti per installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-121">Provides Comments for the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="d3ef2-122">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-122">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ef2-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-124">Fornisce il contatto per installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-124">Provides the Contact for Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="d3ef2-125">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-125">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ef2-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-127">Percorso completo della cartella principale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-127">Fully qualified path to the application's primary folder.</span></span> <span data-ttu-id="d3ef2-128">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-128">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ef2-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-130">Indirizzo Internet, o URL, per il supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-130">Internet address, or URL, for technical support.</span></span> <span data-ttu-id="d3ef2-131">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-131">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ef2-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-133">Numeri di telefono del supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-133">Technical support phone numbers.</span></span> <span data-ttu-id="d3ef2-134">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-134">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ef2-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-136">Impedisce la visualizzazione di un pulsante modifica per il prodotto in Installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-136">Prevents display of a Change button for the product in Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="d3ef2-137">
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-137">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="d3ef2-138">Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-138">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ef2-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-140">Impedisce la visualizzazione di un pulsante Rimuovi per il prodotto in Installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-140">Prevents display of a Remove button for the product in the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="d3ef2-141">Il prodotto può comunque essere rimosso selezionando il pulsante modifica se il pacchetto di installazione è stato creato con un'interfaccia utente che fornisce la rimozione del prodotto come opzione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-141">The product can still be removed by selecting the Change button if the installation package has been authored with a user interface that provides product removal as an option.</span></span>
<blockquote><span data-ttu-id="d3ef2-142">
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-142">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="d3ef2-143">Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-143">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ef2-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-145">Disabilita il pulsante Ripristina di installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-145">Disables the Repair button in the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="d3ef2-146">
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-146">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="d3ef2-147">Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-147">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ef2-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-149">Identifica l'icona visualizzata in Installazione applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-149">Identifies the icon displayed in Add/Remove Programs.</span></span> <span data-ttu-id="d3ef2-150">Se questa proprietà non è definita, Aggiungi/Rimuovi programmi specifica l'icona di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-150">If this property is not defined, Add/Remove Programs specifies the display icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ef2-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-152">Include il file Leggimi per installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-152">Provides the ReadMe for Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="d3ef2-153">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-153">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ef2-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-155">Dimensioni stimate dell'applicazione in KB.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-155">Estimated size of the application in KB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ef2-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-157">Impedisce la visualizzazione dell'applicazione nell'elenco programmi di installazione applicazioni nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-157">Prevents display of the application in the Programs List of the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="d3ef2-158">
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-158">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="d3ef2-159">Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-159">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ef2-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-161">URL per la home page dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-161">URL for application's home page.</span></span> <span data-ttu-id="d3ef2-162">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-162">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d3ef2-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="d3ef2-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span></span></td>
<td><span data-ttu-id="d3ef2-164">URL per le informazioni di aggiornamento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-164">URL for application update information.</span></span> <span data-ttu-id="d3ef2-165">Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="d3ef2-165">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="d3ef2-166">Per informazioni sullo strumento set Program and Defaults, vedere la sezione Utilizzo di [set Program Access e computer defaults](/previous-versions//bb776877(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3ef2-166">For information regarding the Set Program and Defaults tool, refer to the section [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3ef2-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3ef2-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3ef2-168">Disinstalla chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d3ef2-168">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
</dt> </dl>
