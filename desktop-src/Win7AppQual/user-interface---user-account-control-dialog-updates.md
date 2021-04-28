---
description: Interfaccia utente - Aggiornamenti della finestra di dialogo Controllo account utente
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interfaccia utente - Aggiornamenti della finestra di dialogo Controllo account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cd6cc6709283c7bd9cba3e26bd2df29bb02ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094419"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="11639-103">Interfaccia utente - Aggiornamenti della finestra di dialogo Controllo account utente</span><span class="sxs-lookup"><span data-stu-id="11639-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="11639-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="11639-104">Affected Platforms</span></span>

<span data-ttu-id="11639-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="11639-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="11639-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11639-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="11639-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="11639-107">Feature Impact</span></span>

<span data-ttu-id="11639-108">**Gravità** - Bassa</span><span class="sxs-lookup"><span data-stu-id="11639-108">**Severity** - Low</span></span>  
<span data-ttu-id="11639-109">**Frequenza** - Media</span><span class="sxs-lookup"><span data-stu-id="11639-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="11639-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11639-110">Description</span></span>

<span data-ttu-id="11639-111">In Windows 7 sono state standardizzate le opzioni della finestra di dialogo Controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="11639-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="11639-112">In precedenza, gli utenti dovevano scegliere tra più opzioni, ad esempio "Continua", "Annulla" e così via.</span><span class="sxs-lookup"><span data-stu-id="11639-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="11639-113">Ora tutte le finestre di dialogo offrono agli utenti un semplice "Sì" o "No".</span><span class="sxs-lookup"><span data-stu-id="11639-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="11639-114">Il layout della finestra di dialogo ora mostra anche chiaramente il nome del programma, l'autore e l'origine.</span><span class="sxs-lookup"><span data-stu-id="11639-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="11639-115">Sfruttare le funzionalità delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="11639-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="11639-116">I requisiti di sviluppo delle applicazioni in Windows 7 per la compatibilità del controllo dell'account utente sono gli stessi di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11639-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="11639-117">Le applicazioni compatibili con Windows Vista interagiranno con il controllo dell'account utente in Windows 7 senza alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="11639-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="11639-118">Per informazioni su come far funzionare correttamente le applicazioni Windows XP in Windows 7, vedere gli argomenti controllo dell'account utente nel manuale di riferimento sulla compatibilità delle applicazioni di *Windows Vista.*</span><span class="sxs-lookup"><span data-stu-id="11639-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="11639-119">Anche se i miglioramenti del controllo dell'account utente per Windows 7 incideranno sull'esperienza dell'utente, non incideranno sull'interfaccia dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="11639-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="11639-120">Tuttavia, se è presente contenuto della Guida collegato alle finestre di dialogo di Controllo dell'account utente, potrebbe essere necessario aggiornare gli screenshot.</span><span class="sxs-lookup"><span data-stu-id="11639-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="11639-121">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="11639-121">Links to Other Resources</span></span>

-   <span data-ttu-id="11639-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="11639-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="11639-123">Application Compatibility Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="11639-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="11639-124">[Analizzatore utente standard](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="11639-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="11639-125">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="11639-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
