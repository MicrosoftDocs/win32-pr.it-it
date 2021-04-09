---
description: L'oggetto Microsoft. Windows. ActCtx fa riferimento a manifesti e fornisce un modo per eseguire lo scripting dei motori per accedere agli assembly side-by-side. L'oggetto Microsoft. Windows. ActCtx può essere utilizzato per creare un'istanza di un assembly affiancato con componenti COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Oggetto Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880857"
---
# <a name="microsoftwindowsactctx-object"></a><span data-ttu-id="84cd7-104">Oggetto Microsoft. Windows. ActCtx</span><span class="sxs-lookup"><span data-stu-id="84cd7-104">Microsoft.Windows.ActCtx object</span></span>

<span data-ttu-id="84cd7-105">L'oggetto **Microsoft. Windows. ACTCTX** fa riferimento a manifesti e fornisce un modo per eseguire lo scripting dei motori per accedere agli assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="84cd7-105">The **Microsoft.Windows.ActCtx** object references manifests and provides a way for scripting engines to access side-by-side assemblies.</span></span> <span data-ttu-id="84cd7-106">L'oggetto **Microsoft. Windows. ACTCTX** può essere utilizzato per creare un'istanza di un assembly affiancato con componenti com.</span><span class="sxs-lookup"><span data-stu-id="84cd7-106">The **Microsoft.Windows.ActCtx** object can be used to create an instance of a side-by-side assembly with COM components.</span></span>

<span data-ttu-id="84cd7-107">L'oggetto **Microsoft. Windows. ACTCTX** viene visualizzato come assembly in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="84cd7-107">The **Microsoft.Windows.ActCtx** object comes as an assembly in Windows Server 2003.</span></span> <span data-ttu-id="84cd7-108">Può anche essere installato da applicazioni che usano la Windows Installer per il programma di installazione e lo includono come modulo merge nel pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="84cd7-108">It can also be installed by applications that use the Windows Installer for setup and include it as a merge module in their installation package.</span></span>

## <a name="members"></a><span data-ttu-id="84cd7-109">Membri</span><span class="sxs-lookup"><span data-stu-id="84cd7-109">Members</span></span>

<span data-ttu-id="84cd7-110">L'oggetto **Microsoft. Windows. ACTCTX** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="84cd7-110">The **Microsoft.Windows.ActCtx** object has these types of members:</span></span>

-   [<span data-ttu-id="84cd7-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="84cd7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="84cd7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84cd7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="84cd7-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="84cd7-113">Methods</span></span>

<span data-ttu-id="84cd7-114">L'oggetto **Microsoft. Windows. ACTCTX** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="84cd7-114">The **Microsoft.Windows.ActCtx** object has these methods.</span></span>



| <span data-ttu-id="84cd7-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="84cd7-115">Method</span></span>                               | <span data-ttu-id="84cd7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84cd7-116">Description</span></span>                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="84cd7-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="84cd7-117">**CreateObject**</span></span>](createobject.md) | <span data-ttu-id="84cd7-118">Crea un oggetto nel contesto del manifesto corrente.</span><span class="sxs-lookup"><span data-stu-id="84cd7-118">Creates an object in the context of the current manifest.</span></span><br/>            |
| [<span data-ttu-id="84cd7-119">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="84cd7-119">**GetObject**</span></span>](getobject.md)       | <span data-ttu-id="84cd7-120">Ottiene un'istanza di un oggetto **Microsoft. Windows. ACTCTX** esistente.</span><span class="sxs-lookup"><span data-stu-id="84cd7-120">Gets an instance of an existing **Microsoft.Windows.ActCtx** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="84cd7-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84cd7-121">Properties</span></span>

<span data-ttu-id="84cd7-122">L'oggetto **Microsoft. Windows. ACTCTX** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="84cd7-122">The **Microsoft.Windows.ActCtx** object has these properties.</span></span>



| <span data-ttu-id="84cd7-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="84cd7-123">Property</span></span>                                | <span data-ttu-id="84cd7-124">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="84cd7-124">Access type</span></span>          | <span data-ttu-id="84cd7-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84cd7-125">Description</span></span>                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [<span data-ttu-id="84cd7-126">**Manifesto**</span><span class="sxs-lookup"><span data-stu-id="84cd7-126">**Manifest**</span></span>](manifest.md)<br/> | <span data-ttu-id="84cd7-127">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="84cd7-127">Read-only</span></span><br/> | <span data-ttu-id="84cd7-128">Ottiene il contesto di attivazione attiva.</span><span class="sxs-lookup"><span data-stu-id="84cd7-128">Gets the active activation context.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="84cd7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84cd7-129">Requirements</span></span>



| <span data-ttu-id="84cd7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="84cd7-130">Requirement</span></span> | <span data-ttu-id="84cd7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="84cd7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84cd7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84cd7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="84cd7-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="84cd7-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="84cd7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84cd7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="84cd7-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84cd7-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




