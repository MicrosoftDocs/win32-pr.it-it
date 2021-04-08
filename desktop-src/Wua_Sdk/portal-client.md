---
description: L'API dell'agente di Windows Update (WUA) è un set di interfacce COM che consentono agli amministratori di sistema e ai programmatori di accedere Windows Update e Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API dell'agente Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749999"
---
# <a name="windows-update-agent-api"></a><span data-ttu-id="cff10-103">API dell'agente Windows Update</span><span class="sxs-lookup"><span data-stu-id="cff10-103">Windows Update Agent API</span></span>

## <a name="purpose"></a><span data-ttu-id="cff10-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="cff10-104">Purpose</span></span>

<span data-ttu-id="cff10-105">L'API dell'agente di Windows Update (WUA) è un set di interfacce COM che consentono agli amministratori di sistema e ai programmatori di accedere Windows Update e [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cff10-105">The Windows Update Agent (WUA) API is a set of COM interfaces that enable system administrators and programmers to access Windows Update and [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span></span> <span data-ttu-id="cff10-106">È possibile scrivere script e programmi per esaminare gli aggiornamenti attualmente disponibili per un computer, quindi è possibile installare o disinstallare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="cff10-106">Scripts and programs can be written to examine which updates are currently available for a computer, and then you can install or uninstall updates.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="cff10-107">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="cff10-107">Where applicable</span></span>

<span data-ttu-id="cff10-108">Gli amministratori di sistema possono utilizzare WUA per determinare a livello di codice gli aggiornamenti da applicare a un computer, scaricare tali aggiornamenti e quindi installarli senza interventi da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cff10-108">System administrators can use WUA to programmatically determine which updates should be applied to a computer, download those updates, and then install them with little or no user intervention.</span></span>

<span data-ttu-id="cff10-109">I fornitori di software indipendenti (ISV) e gli sviluppatori di utenti finali possono integrare le funzionalità di WUA nel software di gestione dei computer o degli aggiornamenti per offrire un ambiente operativo semplice.</span><span class="sxs-lookup"><span data-stu-id="cff10-109">Independent software vendors (ISV) and end-user developers can integrate WUA features into computer management or update management software to provide a seamless operating environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="cff10-110">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="cff10-110">Developer audience</span></span>

<span data-ttu-id="cff10-111">È possibile scrivere applicazioni WUA in diversi linguaggi di programmazione.</span><span class="sxs-lookup"><span data-stu-id="cff10-111">You can write WUA applications in several programming languages.</span></span> <span data-ttu-id="cff10-112">WUA definisce le interfacce e gli oggetti accessibili da Visual Basic, Visual Basic Scripting Edition (VBScript), JScript e da C e C++.</span><span class="sxs-lookup"><span data-stu-id="cff10-112">WUA defines interfaces and objects that are accessible from Visual Basic, Visual Basic Scripting Edition (VBScript), JScript, and from C and C++.</span></span> <span data-ttu-id="cff10-113">Una certa familiarità con la programmazione COM è utile per il programmatore WUA.</span><span class="sxs-lookup"><span data-stu-id="cff10-113">A familiarity with COM programming is useful to the WUA programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="cff10-114">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="cff10-114">Run-time requirements</span></span>

<span data-ttu-id="cff10-115">WUA è supportato a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cff10-115">WUA is supported starting with Windows XP.</span></span> <span data-ttu-id="cff10-116">WUA è supportato nel server che inizia con Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cff10-116">WUA is supported on the server starting with Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cff10-117">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="cff10-117">In this section</span></span>

-   [<span data-ttu-id="cff10-118">Uso dell'API Windows Update Agent</span><span class="sxs-lookup"><span data-stu-id="cff10-118">Using the Windows Update Agent API</span></span>](using-the-windows-update-agent-api.md)
-   [<span data-ttu-id="cff10-119">Informazioni di riferimento sull'API WUA</span><span class="sxs-lookup"><span data-stu-id="cff10-119">WUA API Reference</span></span>](windows-update-agent--wua--api-reference.md)

 

 
