---
title: attribute_onchange
description: Quando un attributo Skin cambia valore, si verifica un evento che può essere gestito da un gestore eventi. Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e da \ 0034; OnChange \ 0034;, ad esempio \ 0034; value \_ OnChange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330740"
---
# <a name="attribute_onchange"></a><span data-ttu-id="a8bbe-105">attributo \_ OnChange</span><span class="sxs-lookup"><span data-stu-id="a8bbe-105">attribute\_onchange</span></span>

<span data-ttu-id="a8bbe-106">Quando un attributo Skin cambia valore, si verifica un evento che può essere gestito da un gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="a8bbe-106">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="a8bbe-107">Il nome del gestore eventi è il nome dell'attributo seguito da un carattere di sottolineatura e da "onChange", ad esempio "valore \_ OnChange".</span><span class="sxs-lookup"><span data-stu-id="a8bbe-107">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span>

``` syntax
        attribute_onchange
```

## <a name="examples"></a><span data-ttu-id="a8bbe-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8bbe-108">Examples</span></span>


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a><span data-ttu-id="a8bbe-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8bbe-109">Requirements</span></span>



| <span data-ttu-id="a8bbe-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8bbe-110">Requirement</span></span> | <span data-ttu-id="a8bbe-111">Valore</span><span class="sxs-lookup"><span data-stu-id="a8bbe-111">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="a8bbe-112">Versione</span><span class="sxs-lookup"><span data-stu-id="a8bbe-112">Version</span></span><br/> | <span data-ttu-id="a8bbe-113">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="a8bbe-113">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8bbe-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8bbe-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bbe-115">**Gestori eventi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="a8bbe-115">**Ambient Event Handlers**</span></span>](ambient-event-handlers.md)
</dt> </dl>

 

 





