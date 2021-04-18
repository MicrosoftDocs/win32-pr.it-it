---
description: Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer&\# 160; 3.0 e versioni precedenti.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Non supportato in Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310514"
---
# <a name="not-supported-in-windows-installer-30"></a><span data-ttu-id="b0b0b-103">Non supportato in Windows Installer 3,0</span><span class="sxs-lookup"><span data-stu-id="b0b0b-103">Not Supported in Windows Installer 3.0</span></span>

<span data-ttu-id="b0b0b-104">Le funzioni, le tabelle e le proprietà Windows Installer elencate in questa pagina non sono supportate da Windows Installer 3,0 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b0b0b-104">The Windows Installer functions, tables, and properties listed on this page are not supported by Windows Installer 3.0 and earlier versions.</span></span> <span data-ttu-id="b0b0b-105">L'assenza di una funzionalità da questo elenco non garantisce che la funzionalità sia supportata.</span><span class="sxs-lookup"><span data-stu-id="b0b0b-105">The absence of a feature from this list does not guarantee that the feature is supported.</span></span> <span data-ttu-id="b0b0b-106">Vedere la documentazione principale per determinare quale versione di Windows Installer è necessaria per una determinata funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b0b0b-106">See the main documentation to determine which Windows Installer version is required for a particular feature.</span></span> <span data-ttu-id="b0b0b-107">Per informazioni sulle altre versioni di Windows Installer, vedere Novità [di Windows Installer](what-s-new-in-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="b0b0b-107">For information about other Windows Installer versions see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

<span data-ttu-id="b0b0b-108">Windows Installer 3,0 è disponibile per Windows Server 2003, Windows XP o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b0b0b-108">Windows Installer 3.0 is available for Windows Server 2003, Windows XP, or Windows 2000.</span></span> <span data-ttu-id="b0b0b-109">Per un elenco di tutte le versioni Windows Installer e i ridistribuibili, vedere [versioni rilasciate di Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="b0b0b-109">For a list of all Windows Installer versions and redistributables, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="b0b0b-110">Le funzionalità seguenti non sono supportate in Windows Installer 3,0 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b0b0b-110">The following features are not supported in Windows Installer 3.0 and earlier versions.</span></span>

[<span data-ttu-id="b0b0b-111">Funzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="b0b0b-111">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="b0b0b-112">**MsiSetExternalUIRecord**</span><span class="sxs-lookup"><span data-stu-id="b0b0b-112">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="b0b0b-113">**MsiNotifySidChange**</span><span class="sxs-lookup"><span data-stu-id="b0b0b-113">**MsiNotifySidChange**</span></span>](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

<span data-ttu-id="b0b0b-114">Prototipo di funzione di callback</span><span class="sxs-lookup"><span data-stu-id="b0b0b-114">Callback Function Prototype</span></span>

-   [<span data-ttu-id="b0b0b-115">**\_record gestore \_ INSTALLUI**</span><span class="sxs-lookup"><span data-stu-id="b0b0b-115">**INSTALLUI\_HANDLER\_RECORD**</span></span>](/windows/win32/api/msi/nc-msi-installui_handler_record)

[<span data-ttu-id="b0b0b-116">Tabelle di database</span><span class="sxs-lookup"><span data-stu-id="b0b0b-116">Database Tables</span></span>](database-tables.md)

-   <span data-ttu-id="b0b0b-117">La colonna valore della [tabella MsiPatchMetadata](msipatchmetadata-table.md) accetta **OptimizedInstallMode** e **MinorUpdateTargetRTM**.</span><span class="sxs-lookup"><span data-stu-id="b0b0b-117">The Value column of the [MsiPatchMetadata Table](msipatchmetadata-table.md) accepts **OptimizedInstallMode** and **MinorUpdateTargetRTM**.</span></span>

[<span data-ttu-id="b0b0b-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b0b0b-118">Properties</span></span>](properties.md)

-   [<span data-ttu-id="b0b0b-119">**Proprietà Msix64**</span><span class="sxs-lookup"><span data-stu-id="b0b0b-119">**Msix64 Property**</span></span>](msix64.md)

[<span data-ttu-id="b0b0b-120">Windows Installer su sistemi operativi a 64 bit</span><span class="sxs-lookup"><span data-stu-id="b0b0b-120">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)

-   <span data-ttu-id="b0b0b-121">La [**proprietà di riepilogo del modello**](template-summary.md) accetta il valore x64.</span><span class="sxs-lookup"><span data-stu-id="b0b0b-121">The [**Template Summary Property**](template-summary.md) accepts the value x64.</span></span>

[<span data-ttu-id="b0b0b-122">Analizzatori di coerenza interni-CIEM</span><span class="sxs-lookup"><span data-stu-id="b0b0b-122">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="b0b0b-123">ICE99</span><span class="sxs-lookup"><span data-stu-id="b0b0b-123">ICE99</span></span>](ice99.md)

 

 
