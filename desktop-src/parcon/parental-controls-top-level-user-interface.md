---
description: Controlli padre Top-Level interfaccia utente
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: Controlli padre Top-Level interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321475097e25b812aca8d1e65f8b88843ebb1055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313029"
---
# <a name="parental-controls-top-level-user-interface"></a><span data-ttu-id="85354-103">Controlli padre Top-Level interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="85354-103">Parental Controls Top-Level User Interface</span></span>

<span data-ttu-id="85354-104">Il collegamento forte tra la sicurezza della famiglia e gli account utente di Windows ha guidato una categoria combinata che appare come **account utente e Family Safety** nel pannello di controllo per gli SKU orientati agli utenti di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="85354-104">The strong link between Family Safety and Windows user accounts has driven a combined category appearing as **User Accounts and Family Safety** in Control Panel for consumer-oriented SKUs of Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="85354-105">La categoria verrà visualizzata come **account utente** quando viene aggiunto un computer con funzionalità di aggiunta al dominio.</span><span class="sxs-lookup"><span data-stu-id="85354-105">The category will appear as **User Accounts** when a computer with domain-join capability is joined.</span></span>

 

<span data-ttu-id="85354-106">Se un account utente standard non è stato ancora configurato per l'utente controllato, un collegamento nel pannello di controllo fornisce un semplice flusso di lavoro per l'aggiunta di un nuovo account controllato dal padre.</span><span class="sxs-lookup"><span data-stu-id="85354-106">If a standard user account has not yet been set up for the controlled user, a link in Control Panel provides a simple workflow for adding a new parentally controlled account.</span></span>

<span data-ttu-id="85354-107">Dopo la creazione di un account, il pannello di controllo Parental Controls espone la funzionalità di primo livello per l'utente controllato.</span><span class="sxs-lookup"><span data-stu-id="85354-107">After an account is created, the Parental Controls Control Panel exposes the top-level user-facing functionality for the controlled user.</span></span> <span data-ttu-id="85354-108">Elementi</span><span class="sxs-lookup"><span data-stu-id="85354-108">Elements:</span></span>

-   <span data-ttu-id="85354-109">Le restrizioni generali dei controlli padre sono i pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="85354-109">Overall Parental Controls restrictions on or off radio buttons.</span></span>
-   <span data-ttu-id="85354-110">Pulsante di opzione per la segnalazione di attività indipendenti.</span><span class="sxs-lookup"><span data-stu-id="85354-110">Independent Activity Reporting on or off control radio buttons.</span></span>
-   <span data-ttu-id="85354-111">Una sezione delle impostazioni con le restrizioni Web implementate da Microsoft viene collegata in modo condizionale e vengono visualizzati i tipi di restrizioni implementate da Microsoft non in linea di base disponibili.</span><span class="sxs-lookup"><span data-stu-id="85354-111">A Settings section with the Microsoft-implemented Web Restrictions link conditionally shown, and available core offline Microsoft-implemented restrictions types shown.</span></span>
-   <span data-ttu-id="85354-112">Una maggiore area Impostazioni visualizzata se le estensioni dell'interfaccia utente sono registrate da Microsoft o da terze parti.</span><span class="sxs-lookup"><span data-stu-id="85354-112">A More Settings area that appears if User Interface extensions are registered by Microsoft or third parties.</span></span>
-   <span data-ttu-id="85354-113">Area di riepilogo dello stato che mostra il nome utente e il riquadro, il collegamento Visualizza report attività e lo stato delle impostazioni dei controlli padre.</span><span class="sxs-lookup"><span data-stu-id="85354-113">A summary status area showing the user name and tile, the View activity reports link, and the state of Parental Controls settings.</span></span> <span data-ttu-id="85354-114">Se attivata, la visualizzazione include il livello di impostazione del filtro contenuto Web (se il filtro Microsoft è attivo) o il nome del filtro se sottoposto a override da un'estensione di terze parti e lo stato delle impostazioni offline per l'utente.</span><span class="sxs-lookup"><span data-stu-id="85354-114">If on, the display includes the Web Content Filter setting level (if the Microsoft filter is active) or filter name if overridden by a third-party extension, and state of offline settings for the user.</span></span>

<span data-ttu-id="85354-115">I controlli padre generali abilitano il pulsante di opzione inizialmente impostato sullo stato disattivato.</span><span class="sxs-lookup"><span data-stu-id="85354-115">The overall Parental Controls enable radio button is initially set to the off state.</span></span> <span data-ttu-id="85354-116">Una volta attivato da un amministratore, il servizio di report delle attività sarà attivato per impostazione predefinita, ma può essere disattivato in modo indipendente.</span><span class="sxs-lookup"><span data-stu-id="85354-116">When turned on by an administrator, Activity Reporting will also be on by default, but may be turned off independently.</span></span> <span data-ttu-id="85354-117">Come per quasi tutte le impostazioni dei controlli padre, la configurazione può essere eseguita a livello di codice tramite le API disponibili.</span><span class="sxs-lookup"><span data-stu-id="85354-117">As with nearly all settings in Parental Controls, configuration may be performed programmatically through the available APIs.</span></span>

 

 



