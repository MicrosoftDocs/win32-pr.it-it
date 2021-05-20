---
title: Direttiva pragma message
description: Direttiva pragma che genera messaggi in fase di compilazione.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Direttiva pragma message HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153484"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="6420e-104">Direttiva pragma message</span><span class="sxs-lookup"><span data-stu-id="6420e-104">message pragma Directive</span></span>

<span data-ttu-id="6420e-105">Direttiva pragma che genera messaggi in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="6420e-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="6420e-106">\#pragma message("*token-string*")</span><span class="sxs-lookup"><span data-stu-id="6420e-106">\#pragma message("*token-string*")</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="6420e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6420e-107">Parameters</span></span>



| <span data-ttu-id="6420e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="6420e-108">Item</span></span>                                                                                    | <span data-ttu-id="6420e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6420e-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="6420e-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span><span class="sxs-lookup"><span data-stu-id="6420e-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="6420e-111">Messaggio del compilatore.</span><span class="sxs-lookup"><span data-stu-id="6420e-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="6420e-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="6420e-112">Examples</span></span>

<span data-ttu-id="6420e-113">Nell'esempio seguente viene illustrata l'elaborazione dei messaggi durante la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="6420e-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="6420e-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6420e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6420e-115">Direttive per il preprocessore (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6420e-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="6420e-116">\#Direttiva pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6420e-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





