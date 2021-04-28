---
description: Finestra di dialogo comune ChooseFont() Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Finestra di dialogo comune ChooseFont() Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dd8eb6ec226f8dbf5220f5a90dac802cf149dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088609"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="4f448-103">Finestra di dialogo comune ChooseFont() Win32</span><span class="sxs-lookup"><span data-stu-id="4f448-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4f448-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="4f448-104">Affected Platforms</span></span>

<span data-ttu-id="4f448-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f448-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="4f448-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f448-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="4f448-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="4f448-107">Feature Impact</span></span>

<span data-ttu-id="4f448-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="4f448-108">**Severity** - Low</span></span>  
<span data-ttu-id="4f448-109">**Frequenza** - Media</span><span class="sxs-lookup"><span data-stu-id="4f448-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="4f448-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f448-110">Description</span></span>

<span data-ttu-id="4f448-111">Windows 7 include diversi aggiornamenti alla finestra di dialogo comune Win32 ChooseFont().</span><span class="sxs-lookup"><span data-stu-id="4f448-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="4f448-112">Queste sono suddivise in due categorie:</span><span class="sxs-lookup"><span data-stu-id="4f448-112">These fall into two categories:</span></span>

-   <span data-ttu-id="4f448-113">Aggiornamento visivo della finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="4f448-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="4f448-114">Supporto per la nuova funzionalità mostra/nascondi tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="4f448-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="4f448-115">**L'aggiornamento della** finestra di dialogo aggiorna il modello standard per allineare la finestra di dialogo con altri layout di finestra di dialogo in Windows.</span><span class="sxs-lookup"><span data-stu-id="4f448-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="4f448-116">Introduce WYSIWYG agli elenchi di visualizzazione dei tipi di carattere per aiutare gli utenti a scegliere i tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f448-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="4f448-117">Include anche un collegamento alla libreria CPL Dei tipi di carattere per consentire agli utenti di personalizzare gli elenchi di tipi di carattere in modo semplice.</span><span class="sxs-lookup"><span data-stu-id="4f448-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="4f448-118">**Mostra/Nascondi** tipi di carattere è una nuova funzionalità della piattaforma Windows 7 in base alla quale i tipi di carattere non appropriati per le impostazioni della lingua dell'utente corrente (metodi di input) non vengono presentati per impostazione predefinita negli elenchi di selezione dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f448-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="4f448-119">Gli utenti possono personalizzare i tipi di carattere che desiderano visualizzare nella libreria CPL dei tipi di carattere o disabilitare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4f448-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4f448-120">Impatto significativo</span><span class="sxs-lookup"><span data-stu-id="4f448-120">Manifestation of Impact</span></span>

<span data-ttu-id="4f448-121">**Aggiornamento dell'oggetto visivo finestra di dialogo**</span><span class="sxs-lookup"><span data-stu-id="4f448-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="4f448-122">Sono stati introdotti due nuovi modelli in Windows 7 (uno per le applicazioni che caricano la versione 6 o successiva di comctl32.dll e l'altro per le applicazioni che caricano versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="4f448-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="4f448-123">Per motivi di compatibilità delle applicazioni, questi nuovi modelli verranno caricati solo per le applicazioni che non esegano la coda di messaggi ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="4f448-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="4f448-124">Le applicazioni che eseguono l'hook della coda di messaggi continueranno a visualizzare il layout della finestra di dialogo precedente.</span><span class="sxs-lookup"><span data-stu-id="4f448-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="4f448-125">Le applicazioni che forniscono i propri modelli continueranno a essere in grado di usarli.</span><span class="sxs-lookup"><span data-stu-id="4f448-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="4f448-126">Le applicazioni che non ottengono i nuovi modelli non noteranno modifiche al layout della finestra di dialogo da Vista.</span><span class="sxs-lookup"><span data-stu-id="4f448-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="4f448-127">Dovrebbero comunque ottenere la nuova anteprima del tipo di carattere WYSIWYG.</span><span class="sxs-lookup"><span data-stu-id="4f448-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="4f448-128">**Mostra/Nascondi tipi di carattere**</span><span class="sxs-lookup"><span data-stu-id="4f448-128">**Show/hide fonts**</span></span>

<span data-ttu-id="4f448-129">Per tutte le versioni di ChooseFont, la finestra di dialogo userà le impostazioni del carattere show/hide dell'utente corrente per determinare l'elenco dei tipi di carattere da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="4f448-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="4f448-130">Ciò comporta la visualizzazione di un numero inferiore di elenchi di tipi di carattere nella maggior parte dei casi.</span><span class="sxs-lookup"><span data-stu-id="4f448-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="4f448-131">Mitigazione dell'utente finale</span><span class="sxs-lookup"><span data-stu-id="4f448-131">End-user Mitigation</span></span>

<span data-ttu-id="4f448-132">**Mostra/Nascondi tipi di carattere:** Per disabilitare l'nascondiglio dei caratteri, gli utenti devono passare alla pagina Impostazioni carattere nel CPL Tipi di carattere e deselezionare l'opzione '</span><span class="sxs-lookup"><span data-stu-id="4f448-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="4f448-133">Casella di controllo "Nascondi tipi di carattere in base alle impostazioni della lingua"</span><span class="sxs-lookup"><span data-stu-id="4f448-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="4f448-134">Mitigazione degli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="4f448-134">Developer Mitigation</span></span>

-   <span data-ttu-id="4f448-135">**Aggiornamento visivo:** Gli sviluppatori di applicazioni che forniscono i propri modelli potrebbero voler aggiornare questo modello in modo che sia in linea con il nuovo modello di Windows 7 appropriato.</span><span class="sxs-lookup"><span data-stu-id="4f448-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="4f448-136">I nuovi modelli sono disponibili nel file di modello Font.dlg.</span><span class="sxs-lookup"><span data-stu-id="4f448-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="4f448-137">**Nota:** Il nuovo modello pubblicato contiene un controllo SysLink aggiuntivo che fornisce un collegamento che consente agli utenti di avviare la libreria di tipi di carattere CPL per visualizzare altri tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f448-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="4f448-138">Il controllo collegamento richiede la versione 6 della libreria di controlli comuni di Windows (comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="4f448-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="4f448-139">Gli sviluppatori devono fornire un manifesto o una direttiva che specifica l'uso della versione 6 della DLL, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="4f448-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="4f448-140">Quando un'applicazione usa una versione precedente della libreria di controlli comuni, usare invece il tipo di controllo "PUSHBUTTON".</span><span class="sxs-lookup"><span data-stu-id="4f448-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="4f448-141">**Mostra/Nascondi tipi di carattere:** Gli sviluppatori possono disabilitare questa funzionalità fornendo un flag aggiuntivo (CF \_ INACTIVEFONTS) nel membro flags della struttura CHOOSEFONT.</span><span class="sxs-lookup"><span data-stu-id="4f448-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="4f448-142">L'impostazione di questo flag determina la visualizzazione di tutti i tipi di carattere installati nell'elenco dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f448-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="4f448-143">**Mostra/Nascondi tipi di carattere:** Le applicazioni che forniscono contenuto della Guida ChooseFont possono voler aggiungere contenuto per spiegare perché l'elenco dei tipi di carattere è ridotto e indirizzare gli utenti alla libreria CPL Tipi di carattere per personalizzare gli elenchi di tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="4f448-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="4f448-144">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="4f448-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="4f448-145">Gli sviluppatori le cui applicazioni collegano la coda di messaggi ChooseFont per personalizzare la finestra di dialogo devono verificare che le applicazioni mantegano tutte le funzionalità esistenti.</span><span class="sxs-lookup"><span data-stu-id="4f448-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="4f448-146">Le applicazioni che tagliano notevolmente l'elenco dei tipi di carattere usando i flag devono garantire che l'elenco dei tipi di carattere presentato rimanga accettabile.</span><span class="sxs-lookup"><span data-stu-id="4f448-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



