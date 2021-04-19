---
title: THEME. currentViewID
description: L'attributo currentViewID specifica o recupera la visualizzazione attualmente visualizzata.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- THEME. currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328548"
---
# <a name="themecurrentviewid"></a><span data-ttu-id="a1283-104">THEME. currentViewID</span><span class="sxs-lookup"><span data-stu-id="a1283-104">THEME.currentViewID</span></span>

<span data-ttu-id="a1283-105">L'attributo **currentViewID** specifica o recupera la **visualizzazione** attualmente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="a1283-105">The **currentViewID** attribute specifies or retrieves the currently displayed **VIEW**.</span></span>

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a><span data-ttu-id="a1283-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a1283-106">Possible Values</span></span>

<span data-ttu-id="a1283-107">Questo attributo è una **stringa** di lettura/scrittura che specifica l' **ID** della **visualizzazione** corrente.</span><span class="sxs-lookup"><span data-stu-id="a1283-107">This attribute is a read/write **String** specifying the **id** of the current **VIEW**.</span></span> <span data-ttu-id="a1283-108">e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a1283-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1283-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1283-109">Remarks</span></span>

<span data-ttu-id="a1283-110">Se si specifica **currentViewID** , il **currentView** esistente (a cui fa riferimento l'attributo **View** Global) viene chiuso automaticamente e viene aperta la **visualizzazione** specificata.</span><span class="sxs-lookup"><span data-stu-id="a1283-110">Specifying **currentViewID** automatically closes the existing **currentView** (pointed to by the **view** global attribute) and opens the specified **VIEW**.</span></span>

## <a name="examples"></a><span data-ttu-id="a1283-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="a1283-111">Examples</span></span>


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="a1283-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1283-112">Requirements</span></span>



| <span data-ttu-id="a1283-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1283-113">Requirement</span></span> | <span data-ttu-id="a1283-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a1283-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a1283-115">Versione</span><span class="sxs-lookup"><span data-stu-id="a1283-115">Version</span></span><br/> | <span data-ttu-id="a1283-116">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a1283-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1283-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1283-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1283-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="a1283-118">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





