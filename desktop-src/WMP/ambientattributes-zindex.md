---
title: AmbientAttributes. zIndex
description: L'attributo zIndex specifica o recupera l'ordine in cui viene eseguito il rendering del controllo.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Media Player Windows AmbientAttributes. zIndex
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331494"
---
# <a name="ambientattributeszindex"></a><span data-ttu-id="689a1-104">AmbientAttributes. zIndex</span><span class="sxs-lookup"><span data-stu-id="689a1-104">AmbientAttributes.zIndex</span></span>

<span data-ttu-id="689a1-105">L'attributo **ZIndex** specifica o recupera l'ordine in cui viene eseguito il rendering del controllo.</span><span class="sxs-lookup"><span data-stu-id="689a1-105">The **zIndex** attribute specifies or retrieves the order in which the control is rendered.</span></span>

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a><span data-ttu-id="689a1-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="689a1-106">Possible Values</span></span>

<span data-ttu-id="689a1-107">Questo attributo è un **numero** di lettura/scrittura (**Long**) con un valore predefinito pari a zero.</span><span class="sxs-lookup"><span data-stu-id="689a1-107">This attribute is a read/write **Number** (**long**) with a default value of zero.</span></span> <span data-ttu-id="689a1-108">L'intervallo è quello di un valore long integer con segno.</span><span class="sxs-lookup"><span data-stu-id="689a1-108">The range is that of a signed long integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="689a1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="689a1-109">Remarks</span></span>

<span data-ttu-id="689a1-110">La bitmap di sfondo di  una vista **o di una visualizzazione è** con un indice z fisso pari a zero.</span><span class="sxs-lookup"><span data-stu-id="689a1-110">The background bitmap of a **VIEW** or **SUBVIEW** has a fixed z index of zero.</span></span> <span data-ttu-id="689a1-111">Se si vuole che un controllo sia dietro lo sfondo, è necessario impostare **ZIndex** su un numero negativo.</span><span class="sxs-lookup"><span data-stu-id="689a1-111">If you want a control to be behind the background, the **zIndex** must be set to a negative number.</span></span>

<span data-ttu-id="689a1-112">L'indice z di una **vista** o **di una vista è** un indice assoluto, mentre l'indice z di un controllo è relativo all'indice z della **vista** o della **Sottovisualizzazione** che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="689a1-112">The z index of a **VIEW** or **SUBVIEW** is an absolute index, while the z index of a control is relative to the z index of the **VIEW** or **SUBVIEW** that contains it.</span></span>

<span data-ttu-id="689a1-113">L'attributo **ZIndex** non è supportato dagli elementi **browser** e **playlist** .</span><span class="sxs-lookup"><span data-stu-id="689a1-113">The **zIndex** attribute is not supported by the **BROWSER** and **PLAYLIST** elements.</span></span> <span data-ttu-id="689a1-114">Non funzionerà con l'elemento **video** se *video*. senza **finestra** è impostato su false, né con l'elemento **Effects** se **Effects**. **windowed** è impostato su true.</span><span class="sxs-lookup"><span data-stu-id="689a1-114">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if **EFFECTS**.**windowed** is set to true.</span></span>

<span data-ttu-id="689a1-115">Gli elementi **ButtonElement** utilizzano il **ZIndex** del **ButtonGroup**.</span><span class="sxs-lookup"><span data-stu-id="689a1-115">**BUTTONELEMENT** elements use the **zIndex** of their **BUTTONGROUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="689a1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="689a1-116">Requirements</span></span>



| <span data-ttu-id="689a1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="689a1-117">Requirement</span></span> | <span data-ttu-id="689a1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="689a1-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="689a1-119">Versione</span><span class="sxs-lookup"><span data-stu-id="689a1-119">Version</span></span><br/> | <span data-ttu-id="689a1-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="689a1-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="689a1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="689a1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="689a1-122">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="689a1-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





