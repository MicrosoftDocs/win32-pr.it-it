---
description: Indica se la stringa riconosciuta specificata proviene dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Metodo IContextNode:: IsAlternateStringSupported (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307425"
---
# <a name="icontextnodeisalternatestringsupported-method"></a><span data-ttu-id="21653-103">Metodo IContextNode:: IsAlternateStringSupported</span><span class="sxs-lookup"><span data-stu-id="21653-103">IContextNode::IsAlternateStringSupported method</span></span>

<span data-ttu-id="21653-104">Indica se la stringa riconosciuta specificata proviene dal dizionario di sistema, dal dizionario utente o dall'elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="21653-104">Indicates whether the specified recognized string came from the system dictionary, user dictionary, or word list.</span></span> <span data-ttu-id="21653-105">Tutti i dati di restrizione, ad esempio liste, guide o factoids, in qualsiasi nodo hint corrispondente verranno usati per determinare se la stringa è supportata.</span><span class="sxs-lookup"><span data-stu-id="21653-105">Any restricting data, like wordlists, guides or factoids, in any corresponding hint node will be used to determine if the string is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="21653-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21653-106">Syntax</span></span>


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="21653-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="21653-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21653-108">*bstrAlternateString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21653-108">*bstrAlternateString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21653-109">Stringa riconosciuta da verificare.</span><span class="sxs-lookup"><span data-stu-id="21653-109">Recognized string to verify.</span></span>

</dd> <dt>

<span data-ttu-id="21653-110">*pfIsSupported* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="21653-110">*pfIsSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21653-111">**Variante \_ TRUE** se la stringa specificata è supportata da [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con qualsiasi nodo hint corrispondente applicato; **Variante \_ FALSE** se non è supportato.</span><span class="sxs-lookup"><span data-stu-id="21653-111">**VARIANT\_TRUE** if the specified string is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; **VARIANT\_FALSE** if not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21653-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21653-112">Return value</span></span>

<span data-ttu-id="21653-113">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="21653-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="21653-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="21653-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="21653-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21653-115">Requirements</span></span>



| <span data-ttu-id="21653-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="21653-116">Requirement</span></span> | <span data-ttu-id="21653-117">Valore</span><span class="sxs-lookup"><span data-stu-id="21653-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21653-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21653-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21653-119">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="21653-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="21653-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21653-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21653-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="21653-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="21653-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21653-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21653-123"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="21653-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="21653-124">DLL</span><span class="sxs-lookup"><span data-stu-id="21653-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21653-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21653-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="21653-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21653-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21653-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="21653-127">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




