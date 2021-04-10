---
description: Funzioni di Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: Funzioni AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225517"
---
# <a name="avx-functions"></a><span data-ttu-id="14329-103">Funzioni AVX</span><span class="sxs-lookup"><span data-stu-id="14329-103">AVX Functions</span></span>

<span data-ttu-id="14329-104">Di seguito sono riportate le funzioni di Intel AVX.</span><span class="sxs-lookup"><span data-stu-id="14329-104">The following are the Intel AVX functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="14329-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="14329-105">In this section</span></span>



| <span data-ttu-id="14329-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="14329-106">Topic</span></span>                                                                   | <span data-ttu-id="14329-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14329-107">Description</span></span>                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="14329-108">**CopyContext**</span><span class="sxs-lookup"><span data-stu-id="14329-108">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | <span data-ttu-id="14329-109">Copia una struttura del contesto di origine (incluso qualsiasi XState) in una struttura del contesto di destinazione inizializzata.</span><span class="sxs-lookup"><span data-stu-id="14329-109">Copies a source context structure (including any XState) onto an initialized destination context structure.</span></span><br/>         |
| [<span data-ttu-id="14329-110">**GetEnabledXStateFeatures**</span><span class="sxs-lookup"><span data-stu-id="14329-110">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | <span data-ttu-id="14329-111">Ottiene una maschera delle funzionalità XState abilitate nei processori x86 o x64.</span><span class="sxs-lookup"><span data-stu-id="14329-111">Gets a mask of enabled XState features on x86 or x64 processors.</span></span><br/>                                                    |
| [<span data-ttu-id="14329-112">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="14329-112">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | <span data-ttu-id="14329-113">Restituisce la maschera delle funzionalità XState impostate all'interno di una struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .</span><span class="sxs-lookup"><span data-stu-id="14329-113">Returns the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) structure.</span></span><br/>                        |
| [<span data-ttu-id="14329-114">**InitializeContext**</span><span class="sxs-lookup"><span data-stu-id="14329-114">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | <span data-ttu-id="14329-115">Inizializza una struttura di [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) all'interno di un buffer con le dimensioni e l'allineamento necessari.</span><span class="sxs-lookup"><span data-stu-id="14329-115">Initializes a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure inside a buffer with the necessary size and alignment.</span></span><br/>       |
| [<span data-ttu-id="14329-116">**LocateXStateFeature**</span><span class="sxs-lookup"><span data-stu-id="14329-116">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | <span data-ttu-id="14329-117">Recupera un puntatore allo stato del processore per una funzionalità XState all'interno di una struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="14329-117">Retrieves a pointer to the processor state for an XState feature within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/> |
| [<span data-ttu-id="14329-118">**SetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="14329-118">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | <span data-ttu-id="14329-119">Imposta la maschera delle funzionalità XState impostate all'interno di una struttura del [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="14329-119">Sets the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/>                             |



 

 

 




