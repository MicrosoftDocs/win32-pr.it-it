---
description: L'azione ResolveSource determina il percorso dell'origine e imposta la proprietà SourceDir se l'origine non è stata ancora risolta.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Azione ResolveSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316742"
---
# <a name="resolvesource-action"></a><span data-ttu-id="4355c-103">Azione ResolveSource</span><span class="sxs-lookup"><span data-stu-id="4355c-103">ResolveSource Action</span></span>

<span data-ttu-id="4355c-104">L'azione ResolveSource determina il percorso dell'origine e imposta la proprietà [**SourceDir**](sourcedir.md) se l'origine non è stata ancora risolta.</span><span class="sxs-lookup"><span data-stu-id="4355c-104">The ResolveSource action determines the location of the source and sets the [**SourceDir**](sourcedir.md) property if the source has not been resolved yet.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4355c-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="4355c-105">Sequence Restrictions</span></span>

<span data-ttu-id="4355c-106">L'azione ResolveSource deve essere successiva all' [azione CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="4355c-106">The ResolveSource action must come after the [CostInitialize action](costinitialize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4355c-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="4355c-107">ActionData Messages</span></span>

<span data-ttu-id="4355c-108">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="4355c-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="4355c-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="4355c-109">Remarks</span></span>

<span data-ttu-id="4355c-110">Prima di usare la proprietà [**SourceDir**](sourcedir.md) in qualsiasi espressione, è necessario chiamare l'azione ResolveSource.</span><span class="sxs-lookup"><span data-stu-id="4355c-110">The ResolveSource action must be called before using the [**SourceDir**](sourcedir.md) property in any expression.</span></span> <span data-ttu-id="4355c-111">Deve anche essere chiamato prima di tentare di recuperare il valore della proprietà **SourceDir** usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="4355c-111">It must also be called before attempting to retrieve the value of the **SourceDir** property using [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="4355c-112">L'azione ResolveSource non deve essere eseguita se l'origine non è disponibile, come potrebbe essere quando si disinstalla l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4355c-112">The ResolveSource action should not be executed when the source is unavailable, as it may be when uninstalling the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4355c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4355c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4355c-114">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="4355c-114">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



