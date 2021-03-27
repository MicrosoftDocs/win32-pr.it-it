---
title: " Error (direttiva)"
description: Direttiva per il preprocessore che produce messaggi di errore in fase di compilazione.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- Direttiva di errore HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397670"
---
# <a name="error-directive"></a><span data-ttu-id="87133-104">\#Error (direttiva)</span><span class="sxs-lookup"><span data-stu-id="87133-104">\#error Directive</span></span>

<span data-ttu-id="87133-105">Direttiva per il preprocessore che produce messaggi di errore in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="87133-105">Preprocessor directive that produces compiler-time error messages.</span></span>



| <span data-ttu-id="87133-106">\#*stringa di token di* errore</span><span class="sxs-lookup"><span data-stu-id="87133-106">\#error *token-string*</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="87133-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="87133-107">Parameters</span></span>



| <span data-ttu-id="87133-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="87133-108">Item</span></span>                                                                                    | <span data-ttu-id="87133-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87133-109">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87133-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*stringa di token*</span><span class="sxs-lookup"><span data-stu-id="87133-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="87133-111">Messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="87133-111">Error message.</span></span> <span data-ttu-id="87133-112">Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete.</span><span class="sxs-lookup"><span data-stu-id="87133-112">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="87133-113">La stringa del token è soggetta all'espansione della macro.</span><span class="sxs-lookup"><span data-stu-id="87133-113">The token string is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="87133-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="87133-114">Remarks</span></span>

<span data-ttu-id="87133-115">\#le direttive Error sono particolarmente utili per rilevare le incoerenze del programmatore e la violazione dei vincoli durante la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="87133-115">\#error directives are most useful for detecting programmer inconsistencies and violation of constraints during preprocessing.</span></span> <span data-ttu-id="87133-116">Quando \# viene rilevata una direttiva di errore, la compilazione viene terminata.</span><span class="sxs-lookup"><span data-stu-id="87133-116">When an \#error directive is encountered, compilation terminates.</span></span>

## <a name="examples"></a><span data-ttu-id="87133-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="87133-117">Examples</span></span>

<span data-ttu-id="87133-118">Nell'esempio seguente viene illustrata l'elaborazione degli errori durante la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="87133-118">The following example demonstrates error processing during preprocessing.</span></span>


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a><span data-ttu-id="87133-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87133-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87133-120">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87133-120">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





