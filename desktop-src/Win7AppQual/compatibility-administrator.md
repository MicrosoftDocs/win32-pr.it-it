---
description: Compatibility Administrator
ms.assetid: 72a77e83-ab18-438c-af11-fa6d55bf0180
title: Compatibility Administrator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d941c9db85c8302d8d7d8808f24b95d1f3b08be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088529"
---
# <a name="compatibility-administrator"></a><span data-ttu-id="9fc6f-103">Compatibility Administrator</span><span class="sxs-lookup"><span data-stu-id="9fc6f-103">Compatibility Administrator</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="9fc6f-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="9fc6f-104">Affected Platforms</span></span>

 <span data-ttu-id="9fc6f-105">**Client:** Windows 2000, Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="9fc6f-105">**Clients:** Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="9fc6f-106">**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9fc6f-106">**Servers:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="9fc6f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fc6f-107">Description</span></span>

<span data-ttu-id="9fc6f-108">Lo strumento Di amministrazione compatibilità, fornito da Application Compatibility Toolkit (ACT) consente di risolvere molti dei potenziali problemi di compatibilità delle applicazioni, prima di distribuire una nuova versione di Windows nell'organizzazione, tramite:</span><span class="sxs-lookup"><span data-stu-id="9fc6f-108">The Compatibility Administrator tool, provided by the Application Compatibility Toolkit (ACT) enables you to resolve many of your potential application compatibility issues, before deploying a new version of Windows to your organization, by:</span></span>

-   <span data-ttu-id="9fc6f-109">Fornire singole correzioni di compatibilità, modalità di compatibilità e messaggi AppHelp che è possibile usare per risolvere problemi di compatibilità specifici</span><span class="sxs-lookup"><span data-stu-id="9fc6f-109">Providing individual compatibility fixes, compatibility modes, and AppHelp messages that you can use to resolve specific compatibility issues</span></span>
-   <span data-ttu-id="9fc6f-110">Possibilità di creare correzioni di compatibilità personalizzate, modalità di compatibilità, messaggi AppHelp e database di compatibilità</span><span class="sxs-lookup"><span data-stu-id="9fc6f-110">Enabling you to create customized compatibility fixes, compatibility modes, AppHelp messages, and compatibility databases</span></span>
-   <span data-ttu-id="9fc6f-111">Fornire uno strumento di query che consente di cercare le correzioni installate nei computer locali</span><span class="sxs-lookup"><span data-stu-id="9fc6f-111">Providing a query tool that enables you to search for installed fixes on your local computers</span></span>

## <a name="usage"></a><span data-ttu-id="9fc6f-112">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="9fc6f-112">Usage</span></span>

<span data-ttu-id="9fc6f-113">Il diagramma di flusso seguente illustra i passaggi necessari per usare Amministratore compatibilità per creare le correzioni per la compatibilità, le modalità di compatibilità e i messaggi di AppHelp.</span><span class="sxs-lookup"><span data-stu-id="9fc6f-113">The following flowchart illustrates the steps required in using the Compatibility Administrator to create your compatibility fixes, compatibility modes, and your AppHelp messages.</span></span>



|                                            |          |                                                                                            |          |                                                     |          |                                                                             |
|--------------------------------------------|----------|--------------------------------------------------------------------------------------------|----------|-----------------------------------------------------|----------|-----------------------------------------------------------------------------|
| <span data-ttu-id="9fc6f-114">Creare un nuovo database di compatibilità (con estensione sdb)</span><span class="sxs-lookup"><span data-stu-id="9fc6f-114">Create a new compatibility database (.sdb)</span></span> | **>** | <span data-ttu-id="9fc6f-115">Selezionare l'applicazione e quindi selezionare le correzioni per la compatibilità da applicare all'applicazione</span><span class="sxs-lookup"><span data-stu-id="9fc6f-115">Select the application and then select the compatibility fixes to apply to the application</span></span> | **>** | <span data-ttu-id="9fc6f-116">Testare l'applicazione con la nuova correzione per la compatibilità</span><span class="sxs-lookup"><span data-stu-id="9fc6f-116">Test the application with the new compatibility fix</span></span> | **>** | <span data-ttu-id="9fc6f-117">Salvare il database di compatibilità e quindi distribuire la correzione all'azienda</span><span class="sxs-lookup"><span data-stu-id="9fc6f-117">Save the compatibility database and then deploy the fix to your corporation</span></span> |



 

## <a name="links-to-other-resources"></a><span data-ttu-id="9fc6f-118">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="9fc6f-118">Links to Other Resources</span></span>

-   [<span data-ttu-id="9fc6f-119">Application Compatibility Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="9fc6f-119">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="9fc6f-120">[Uso di Amministrazione compatibilità](/previous-versions/windows/it-pro/windows-7/cc749034(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9fc6f-120">[Using the Compatibility Administrator](/previous-versions/windows/it-pro/windows-7/cc749034(v=ws.10))</span></span>
-   <span data-ttu-id="9fc6f-121">[Correzioni di compatibilità note, modalità di compatibilità e messaggi AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9fc6f-121">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   <span data-ttu-id="9fc6f-122">[Test e mitigazione dei problemi tramite gli strumenti di sviluppo](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9fc6f-122">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>

 

 
