---
description: La proprietà ModuleFiles dell'oggetto GetFiles restituisce tutte le chiavi primarie della tabella file per il modulo attualmente aperto.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Proprietà GetFiles. ModuleFiles (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332853"
---
# <a name="getfilesmodulefiles-property"></a><span data-ttu-id="bc3df-103">Proprietà GetFiles. ModuleFiles</span><span class="sxs-lookup"><span data-stu-id="bc3df-103">GetFiles.ModuleFiles property</span></span>

<span data-ttu-id="bc3df-104">La proprietà **ModuleFiles** dell'oggetto [**GetFiles**](getfiles-object.md) restituisce tutte le chiavi primarie della [tabella file](file-table.md) per il modulo attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="bc3df-104">**ModuleFiles** property of the [**GetFiles**](getfiles-object.md) object returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span> <span data-ttu-id="bc3df-105">Le chiavi primarie vengono restituite come raccolta di stringhe.</span><span class="sxs-lookup"><span data-stu-id="bc3df-105">The primary keys are returned as a collection of strings.</span></span> <span data-ttu-id="bc3df-106">Il modulo deve essere aperto da una chiamata al metodo [**ApriModulo**](merge-openmodule.md) dell' [oggetto merge](merge-object.md) prima di chiamare **ModuleFiles**.</span><span class="sxs-lookup"><span data-stu-id="bc3df-106">The module must be opened by a call to the [**OpenModule**](merge-openmodule.md) method of the [Merge object](merge-object.md) before calling **ModuleFiles**.</span></span>

<span data-ttu-id="bc3df-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bc3df-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3df-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc3df-108">Syntax</span></span>


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a><span data-ttu-id="bc3df-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bc3df-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="bc3df-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc3df-110">Remarks</span></span>

<span data-ttu-id="bc3df-111">Si noti che l'ordine dei file elencati nella raccolta potrebbe non trovarsi nella stessa sequenza indicata nella tabella file.</span><span class="sxs-lookup"><span data-stu-id="bc3df-111">Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.</span></span>

<span data-ttu-id="bc3df-112">Se il modulo non dispone di una tabella di file o non contiene file nel linguaggio specifico, ModuleFiles restituisce una raccolta di stringhe vuota.</span><span class="sxs-lookup"><span data-stu-id="bc3df-112">If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.</span></span>

### <a name="c"></a><span data-ttu-id="bc3df-113">C++</span><span class="sxs-lookup"><span data-stu-id="bc3df-113">C++</span></span>

<span data-ttu-id="bc3df-114">Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) la funzione ModuleFiles.</span><span class="sxs-lookup"><span data-stu-id="bc3df-114">See [**get\_ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc3df-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc3df-115">Requirements</span></span>



| <span data-ttu-id="bc3df-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc3df-116">Requirement</span></span> | <span data-ttu-id="bc3df-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bc3df-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3df-118">Versione</span><span class="sxs-lookup"><span data-stu-id="bc3df-118">Version</span></span><br/> | <span data-ttu-id="bc3df-119">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bc3df-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="bc3df-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc3df-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bc3df-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc3df-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc3df-122">DLL</span><span class="sxs-lookup"><span data-stu-id="bc3df-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="bc3df-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc3df-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
