---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () finestra di dialogo comune Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318889"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="1f72c-103">ChooseFont () finestra di dialogo comune Win32</span><span class="sxs-lookup"><span data-stu-id="1f72c-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="1f72c-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="1f72c-104">Affected Platforms</span></span>

<span data-ttu-id="1f72c-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="1f72c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="1f72c-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1f72c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="1f72c-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="1f72c-107">Feature Impact</span></span>

<span data-ttu-id="1f72c-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="1f72c-108">**Severity** - Low</span></span>  
<span data-ttu-id="1f72c-109">**Frequenza** -media</span><span class="sxs-lookup"><span data-stu-id="1f72c-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="1f72c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f72c-110">Description</span></span>

<span data-ttu-id="1f72c-111">Windows 7 include diversi aggiornamenti alla finestra di dialogo comune di ChooseFont () Win32.</span><span class="sxs-lookup"><span data-stu-id="1f72c-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="1f72c-112">Questi rientrano in due categorie:</span><span class="sxs-lookup"><span data-stu-id="1f72c-112">These fall into two categories:</span></span>

-   <span data-ttu-id="1f72c-113">Aggiornamento visivo della finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="1f72c-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="1f72c-114">Supporto per la nuova funzionalità Mostra/Nascondi tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="1f72c-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="1f72c-115">L' **aggiornamento della finestra di dialogo** aggiorna il modello standard per rendere la finestra di dialogo più in linea con altri layout di finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="1f72c-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="1f72c-116">Introduce gli elenchi di visualizzazione del tipo di carattere WYSIWYG per consentire agli utenti di scegliere i tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="1f72c-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="1f72c-117">Include anche un collegamento al CPL dei tipi di carattere per facilitare l'accesso agli utenti che desiderano personalizzare gli elenchi di tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="1f72c-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="1f72c-118">**Mostra/Nascondi tipi di carattere** è una nuova funzionalità della piattaforma Windows 7 in cui i tipi di carattere non appropriati per le impostazioni della lingua dell'utente corrente (metodi di input) non vengono visualizzati per impostazione predefinita negli elenchi di selezione dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="1f72c-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="1f72c-119">Gli utenti possono personalizzare i tipi di carattere che desiderano visualizzare nel CPL dei tipi di carattere o possono disabilitare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1f72c-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="1f72c-120">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="1f72c-120">Manifestation of Impact</span></span>

<span data-ttu-id="1f72c-121">**Aggiornamento visivo finestra di dialogo**</span><span class="sxs-lookup"><span data-stu-id="1f72c-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="1f72c-122">In Windows 7 sono stati introdotti due nuovi modelli (uno per le applicazioni che caricano la versione 6 o successiva di comctl32.dll e un'altra per le applicazioni che caricano versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="1f72c-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="1f72c-123">Per motivi di compatibilità delle applicazioni, questi nuovi modelli verranno caricati solo per le applicazioni che non eseguono l'hook della coda di messaggi ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="1f72c-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="1f72c-124">Le applicazioni che collegano la coda di messaggi continueranno a visualizzare il vecchio layout della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="1f72c-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="1f72c-125">Le applicazioni che forniscono modelli personalizzati continueranno a utilizzarle.</span><span class="sxs-lookup"><span data-stu-id="1f72c-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="1f72c-126">Le applicazioni che non ottengono i nuovi modelli non vedranno modifiche al layout della finestra di dialogo da vista.</span><span class="sxs-lookup"><span data-stu-id="1f72c-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="1f72c-127">Dovrebbero comunque ottenere la nuova anteprima del tipo di carattere WYSIWYG.</span><span class="sxs-lookup"><span data-stu-id="1f72c-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="1f72c-128">**Mostra/Nascondi tipi di carattere**</span><span class="sxs-lookup"><span data-stu-id="1f72c-128">**Show/hide fonts**</span></span>

<span data-ttu-id="1f72c-129">Per tutte le versioni di ChooseFont, nella finestra di dialogo vengono usate le impostazioni del tipo di carattere Mostra/Nascondi dell'utente corrente per determinare l'elenco dei tipi di carattere da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="1f72c-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="1f72c-130">Questo comporterà la visualizzazione di un numero inferiore di elenchi di tipi di carattere nella maggior parte delle istanze.</span><span class="sxs-lookup"><span data-stu-id="1f72c-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="1f72c-131">Attenuazione dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="1f72c-131">End-user Mitigation</span></span>

<span data-ttu-id="1f72c-132">**Mostra/Nascondi tipi di carattere:** Per disabilitare il nascondimento dei tipi di carattere, gli utenti devono passare alla pagina delle impostazioni del tipo di carattere nel CPL dei tipi di carattere e deselezionare l'</span><span class="sxs-lookup"><span data-stu-id="1f72c-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="1f72c-133">Casella di controllo "Nascondi tipi di carattere basati su Impostazioni lingua"</span><span class="sxs-lookup"><span data-stu-id="1f72c-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="1f72c-134">Mitigazione degli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="1f72c-134">Developer Mitigation</span></span>

-   <span data-ttu-id="1f72c-135">**Aggiornamento visivo:** Gli sviluppatori di applicazioni che forniscono i propri modelli potrebbero voler aggiornare questo oggetto in linea con il nuovo modello di Windows 7 appropriato.</span><span class="sxs-lookup"><span data-stu-id="1f72c-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="1f72c-136">I nuovi modelli sono disponibili nel file di modello font. dlg.</span><span class="sxs-lookup"><span data-stu-id="1f72c-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="1f72c-137">**Nota:** Il nuovo modello pubblicato contiene un controllo SysLink aggiuntivo che fornisce un collegamento che consente agli utenti di avviare il CPL dei tipi di carattere per visualizzare più tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="1f72c-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="1f72c-138">Il controllo collegamento richiede la versione 6 della libreria di controlli comuni di Windows (comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="1f72c-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="1f72c-139">Gli sviluppatori devono fornire un manifesto o una direttiva che specifichi l'uso della versione 6 della DLL, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="1f72c-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="1f72c-140">Se un'applicazione usa una versione precedente della libreria di controlli comuni, usare invece il tipo di controllo "pulsante".</span><span class="sxs-lookup"><span data-stu-id="1f72c-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="1f72c-141">**Mostra/Nascondi tipi di carattere:** Gli sviluppatori possono disabilitare questa funzionalità fornendo un flag aggiuntivo (CF \_ INACTIVEFONTS) nel membro Flags della struttura ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="1f72c-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="1f72c-142">L'impostazione di questo flag causa la visualizzazione di tutti i tipi di carattere installati nell'elenco dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="1f72c-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="1f72c-143">**Mostra/Nascondi tipi di carattere:** Le applicazioni che forniscono contenuto della Guida ChooseFont possono voler aggiungere contenuto per spiegare il motivo per cui l'elenco dei tipi di carattere viene ridotto e indirizzare gli utenti al CPL dei tipi di carattere per personalizzare gli elenchi di tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="1f72c-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="1f72c-144">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="1f72c-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="1f72c-145">Gli sviluppatori le cui applicazioni collegano la coda di messaggi ChooseFont per personalizzare la finestra di dialogo devono verificare che le applicazioni mantengano tutte le funzionalità esistenti.</span><span class="sxs-lookup"><span data-stu-id="1f72c-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="1f72c-146">Le applicazioni che tagliano fortemente l'elenco dei tipi di carattere usando i flag devono assicurarsi che l'elenco dei tipi di carattere rimanga accettabile.</span><span class="sxs-lookup"><span data-stu-id="1f72c-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



