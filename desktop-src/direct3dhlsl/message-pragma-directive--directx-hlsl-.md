---
title: Message pragma (direttiva)
description: Direttiva pragma che produce messaggi della fase di compilazione.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Message pragma directive HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718925"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="28060-104">Message pragma (direttiva)</span><span class="sxs-lookup"><span data-stu-id="28060-104">message pragma Directive</span></span>

<span data-ttu-id="28060-105">Direttiva pragma che produce messaggi della fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="28060-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="28060-106">\#pragma message "*token-String*"</span><span class="sxs-lookup"><span data-stu-id="28060-106">\#pragma message "*token-string*"</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="28060-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="28060-107">Parameters</span></span>



| <span data-ttu-id="28060-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="28060-108">Item</span></span>                                                                                    | <span data-ttu-id="28060-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28060-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="28060-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*stringa di token*</span><span class="sxs-lookup"><span data-stu-id="28060-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="28060-111">Messaggio del compilatore.</span><span class="sxs-lookup"><span data-stu-id="28060-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="28060-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="28060-112">Examples</span></span>

<span data-ttu-id="28060-113">Nell'esempio seguente viene illustrata l'elaborazione dei messaggi durante la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="28060-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="28060-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28060-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28060-115">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28060-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="28060-116">\#pragma (direttiva) (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="28060-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





