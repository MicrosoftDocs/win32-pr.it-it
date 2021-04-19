---
description: .
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interfaccia utente-aggiornamenti della finestra di dialogo controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5711f8bbed029102bea81e0f4cfcbd4649b5a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319826"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="afda6-103">Interfaccia utente-aggiornamenti della finestra di dialogo controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="afda6-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="afda6-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="afda6-104">Affected Platforms</span></span>

<span data-ttu-id="afda6-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="afda6-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="afda6-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="afda6-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="afda6-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="afda6-107">Feature Impact</span></span>

<span data-ttu-id="afda6-108">**Gravità** -bassa</span><span class="sxs-lookup"><span data-stu-id="afda6-108">**Severity** - Low</span></span>  
<span data-ttu-id="afda6-109">**Frequenza** -media</span><span class="sxs-lookup"><span data-stu-id="afda6-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="afda6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afda6-110">Description</span></span>

<span data-ttu-id="afda6-111">In Windows 7 sono state standardizzate le opzioni della finestra di dialogo controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="afda6-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="afda6-112">In precedenza, gli utenti dovevano scegliere tra più opzioni, ad esempio "continua", "Annulla" e così via.</span><span class="sxs-lookup"><span data-stu-id="afda6-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="afda6-113">Ora tutte le finestre di dialogo forniscono agli utenti un semplice "Sì" o "No".</span><span class="sxs-lookup"><span data-stu-id="afda6-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="afda6-114">Il layout della finestra di dialogo ora Mostra anche il nome del programma, l'autore e l'origine.</span><span class="sxs-lookup"><span data-stu-id="afda6-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="afda6-115">Sfruttando le funzionalità</span><span class="sxs-lookup"><span data-stu-id="afda6-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="afda6-116">I requisiti di sviluppo delle applicazioni in Windows 7 per la compatibilità con il controllo dell'account utente sono identici a quelli di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="afda6-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="afda6-117">Le applicazioni compatibili con Windows Vista interagiranno con UAC in Windows 7 senza alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="afda6-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="afda6-118">Per informazioni su come fare in modo che le applicazioni Windows XP funzionino correttamente in Windows 7, vedere gli argomenti relativi al controllo dell'account utente in *Windows Vista Application Compatibility Cookbook* .</span><span class="sxs-lookup"><span data-stu-id="afda6-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="afda6-119">Sebbene i miglioramenti apportati all'UAC per Windows 7 avranno un effetto sull'esperienza dell'utente, non avranno alcun effetto sull'interfaccia dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="afda6-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="afda6-120">Tuttavia, se è presente un contenuto della guida collegato alle finestre di dialogo del controllo dell'account utente, potrebbe essere necessario aggiornare le schermate.</span><span class="sxs-lookup"><span data-stu-id="afda6-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="afda6-121">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="afda6-121">Links to Other Resources</span></span>

-   <span data-ttu-id="afda6-122">[Cookbook per la compatibilità delle applicazioni di Windows Vista](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="afda6-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="afda6-123">Download di Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="afda6-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="afda6-124">[Analizzatore utente standard](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="afda6-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="afda6-125">Queste risorse potrebbero non essere disponibili in alcune lingue e paesi/aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="afda6-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
