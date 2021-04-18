---
title: TEMA. openView
description: Il metodo openView apre una visualizzazione in una nuova finestra.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- TEMA. openView Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328391"
---
# <a name="themeopenview"></a><span data-ttu-id="8c657-104">TEMA. openView</span><span class="sxs-lookup"><span data-stu-id="8c657-104">THEME.openView</span></span>

<span data-ttu-id="8c657-105">Il metodo **openView** apre una **visualizzazione** in una nuova finestra.</span><span class="sxs-lookup"><span data-stu-id="8c657-105">The **openView** method opens a **VIEW** in a new window.</span></span>

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a><span data-ttu-id="8c657-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c657-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c657-107"><span id="view"></span><span id="VIEW"></span>*visualizzare*</span><span class="sxs-lookup"><span data-stu-id="8c657-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="8c657-108">**Stringa** che specifica l' **ID** della **visualizzazione** da aprire.</span><span class="sxs-lookup"><span data-stu-id="8c657-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c657-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c657-109">Return Value</span></span>

<span data-ttu-id="8c657-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8c657-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="8c657-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c657-111">Examples</span></span>


```JScript
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



## <a name="requirements"></a><span data-ttu-id="8c657-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c657-112">Requirements</span></span>



| <span data-ttu-id="8c657-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c657-113">Requirement</span></span> | <span data-ttu-id="8c657-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8c657-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8c657-115">Versione</span><span class="sxs-lookup"><span data-stu-id="8c657-115">Version</span></span><br/> | <span data-ttu-id="8c657-116">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="8c657-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c657-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c657-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c657-118">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="8c657-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="8c657-119">**THEME. closeView**</span><span class="sxs-lookup"><span data-stu-id="8c657-119">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="8c657-120">**THEME. openViewRelative**</span><span class="sxs-lookup"><span data-stu-id="8c657-120">**THEME.openViewRelative**</span></span>](theme-openviewrelative.md)
</dt> </dl>

 

 





