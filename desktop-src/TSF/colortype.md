---
title: Enumerazione COLORTYPE (Softkbdc. h)
description: Gli elementi dell'enumerazione COLORTYPE vengono utilizzati per specificare i tipi di colori disponibili per una tastiera soft.
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- Framework servizi di testo enumerazione COLORTYPE
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302184"
---
# <a name="colortype-enumeration"></a><span data-ttu-id="abc1b-104">Enumerazione COLORTYPE</span><span class="sxs-lookup"><span data-stu-id="abc1b-104">COLORTYPE enumeration</span></span>

<span data-ttu-id="abc1b-105">Gli elementi dell'enumerazione **ColorType** vengono utilizzati per specificare i tipi di colori disponibili per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="abc1b-105">Elements of the **COLORTYPE** enumeration are used to specify types of colors that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="abc1b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abc1b-106">Syntax</span></span>


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a><span data-ttu-id="abc1b-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="abc1b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="abc1b-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span><span class="sxs-lookup"><span data-stu-id="abc1b-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span></span>
</dt> <dd>

<span data-ttu-id="abc1b-109">Colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="abc1b-109">Background color.</span></span>

</dd> <dt>

<span data-ttu-id="abc1b-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span><span class="sxs-lookup"><span data-stu-id="abc1b-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="abc1b-111">Colore di primo piano non selezionato.</span><span class="sxs-lookup"><span data-stu-id="abc1b-111">Unselected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="abc1b-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span><span class="sxs-lookup"><span data-stu-id="abc1b-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="abc1b-113">Colore del testo non selezionato.</span><span class="sxs-lookup"><span data-stu-id="abc1b-113">Unselected text color.</span></span>

</dd> <dt>

<span data-ttu-id="abc1b-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span><span class="sxs-lookup"><span data-stu-id="abc1b-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="abc1b-115">Colore di primo piano selezionato.</span><span class="sxs-lookup"><span data-stu-id="abc1b-115">Selected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="abc1b-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span><span class="sxs-lookup"><span data-stu-id="abc1b-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="abc1b-117">Colore del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="abc1b-117">Selected text color.</span></span>

</dd> <dt>

<span data-ttu-id="abc1b-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**\_Tipo di colore Max \_**</span><span class="sxs-lookup"><span data-stu-id="abc1b-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max\_color\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="abc1b-119">Tipo di colore massimo.</span><span class="sxs-lookup"><span data-stu-id="abc1b-119">Maximum color type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abc1b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abc1b-120">Requirements</span></span>



| <span data-ttu-id="abc1b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="abc1b-121">Requirement</span></span> | <span data-ttu-id="abc1b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="abc1b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abc1b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abc1b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="abc1b-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="abc1b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="abc1b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abc1b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="abc1b-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="abc1b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="abc1b-127">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="abc1b-127">Redistributable</span></span><br/>          | <span data-ttu-id="abc1b-128">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="abc1b-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="abc1b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abc1b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="abc1b-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="abc1b-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="abc1b-131">IDL</span><span class="sxs-lookup"><span data-stu-id="abc1b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abc1b-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abc1b-132"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





