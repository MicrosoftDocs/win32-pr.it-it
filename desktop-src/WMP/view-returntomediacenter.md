---
title: Visualizza returnToMediaCenter
description: Il metodo returnToMediaCenter restituisce l'utente alla modalità completa di Windows Media Player.
ms.assetid: eebf0679-5704-498c-8eb3-f7710e0cb1fe
keywords:
- Visualizza Media Player Windows returnToMediaCenter
topic_type:
- apiref
api_name:
- VIEW.returnToMediaCenter
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c5f0c86bdd15140ba92261d1f5e8c510d77afc7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329065"
---
# <a name="viewreturntomediacenter"></a><span data-ttu-id="83d96-104">Visualizza returnToMediaCenter</span><span class="sxs-lookup"><span data-stu-id="83d96-104">VIEW.returnToMediaCenter</span></span>

<span data-ttu-id="83d96-105">Il metodo **returnToMediaCenter** restituisce l'utente alla modalità completa di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="83d96-105">The **returnToMediaCenter** method returns the user to the full mode of Windows Media Player.</span></span>

``` syntax
        elementID.returnToMediaCenter()
```

## <a name="parameters"></a><span data-ttu-id="83d96-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83d96-106">Parameters</span></span>

<span data-ttu-id="83d96-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="83d96-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83d96-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83d96-108">Return Value</span></span>

<span data-ttu-id="83d96-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="83d96-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="83d96-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="83d96-110">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.returnToMediaCenter()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="83d96-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83d96-111">Requirements</span></span>



| <span data-ttu-id="83d96-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="83d96-112">Requirement</span></span> | <span data-ttu-id="83d96-113">Valore</span><span class="sxs-lookup"><span data-stu-id="83d96-113">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="83d96-114">Versione</span><span class="sxs-lookup"><span data-stu-id="83d96-114">Version</span></span><br/> | <span data-ttu-id="83d96-115">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="83d96-115">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83d96-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83d96-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d96-117">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="83d96-117">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





