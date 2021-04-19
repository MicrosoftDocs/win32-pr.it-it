---
description: Indica se la stringa riconosciuta di questo IContextNode proviene dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'Metodo IContextNode:: IsStringSupported (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307423"
---
# <a name="icontextnodeisstringsupported-method"></a><span data-ttu-id="19338-103">Metodo IContextNode:: IsStringSupported</span><span class="sxs-lookup"><span data-stu-id="19338-103">IContextNode::IsStringSupported method</span></span>

<span data-ttu-id="19338-104">Indica se la stringa riconosciuta di questo [**IContextNode**](icontextnode.md) proviene dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="19338-104">Indicates whether recognized string of this [**IContextNode**](icontextnode.md) came from the system dictionary, user dictionary, or word list.</span></span>

## <a name="syntax"></a><span data-ttu-id="19338-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19338-105">Syntax</span></span>


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="19338-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19338-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19338-107">*pfIsSupported* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="19338-107">*pfIsSupported* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="19338-108">**Variante \_ TRUE** se il valore stringa riconosciuto di questo [**IContextNode**](icontextnode.md) è supportato da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con tutti i nodi hint corrispondenti applicati. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="19338-108">**VARIANT\_TRUE** if the recognized string value of this [**IContextNode**](icontextnode.md) is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19338-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19338-109">Return value</span></span>

<span data-ttu-id="19338-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="19338-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19338-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19338-111">Requirements</span></span>



| <span data-ttu-id="19338-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="19338-112">Requirement</span></span> | <span data-ttu-id="19338-113">Valore</span><span class="sxs-lookup"><span data-stu-id="19338-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19338-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19338-114">Minimum supported client</span></span><br/> | <span data-ttu-id="19338-115">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="19338-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="19338-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19338-116">Minimum supported server</span></span><br/> | <span data-ttu-id="19338-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19338-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="19338-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19338-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="19338-119"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="19338-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="19338-120">DLL</span><span class="sxs-lookup"><span data-stu-id="19338-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19338-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19338-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="19338-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19338-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19338-123">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="19338-123">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




