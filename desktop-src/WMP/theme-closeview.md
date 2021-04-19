---
title: THEME. closeView
description: Il metodo closeView chiude una visualizzazione aperta.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- THEME. closeView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327284"
---
# <a name="themecloseview"></a><span data-ttu-id="c5e0c-104">THEME. closeView</span><span class="sxs-lookup"><span data-stu-id="c5e0c-104">THEME.closeView</span></span>

<span data-ttu-id="c5e0c-105">Il metodo **closeView** chiude una **visualizzazione** aperta.</span><span class="sxs-lookup"><span data-stu-id="c5e0c-105">The **closeView** method closes an open **VIEW**.</span></span>

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a><span data-ttu-id="c5e0c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5e0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e0c-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span><span class="sxs-lookup"><span data-stu-id="c5e0c-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span></span>
</dt> <dd>

<span data-ttu-id="c5e0c-108">**Stringa** che specifica l' **ID** della **visualizzazione** da chiudere.</span><span class="sxs-lookup"><span data-stu-id="c5e0c-108">A **String** specifying the **id** of the **VIEW** to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e0c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5e0c-109">Return Value</span></span>

<span data-ttu-id="c5e0c-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c5e0c-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="c5e0c-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="c5e0c-111">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="c5e0c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5e0c-112">Requirements</span></span>



| <span data-ttu-id="c5e0c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e0c-113">Requirement</span></span> | <span data-ttu-id="c5e0c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c5e0c-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c5e0c-115">Versione</span><span class="sxs-lookup"><span data-stu-id="c5e0c-115">Version</span></span><br/> | <span data-ttu-id="c5e0c-116">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="c5e0c-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5e0c-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5e0c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e0c-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="c5e0c-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="c5e0c-119">**TEMA. openView**</span><span class="sxs-lookup"><span data-stu-id="c5e0c-119">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





