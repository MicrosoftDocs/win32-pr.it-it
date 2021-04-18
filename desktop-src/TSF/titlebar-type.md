---
title: Enumerazione TITLEBAR_TYPE (Softkbdc. h)
description: Gli elementi dell'enumerazione del tipo di barra di titolo \_ vengono usati per specificare i tipi di barra disponibili per una finestra di tastiera soft.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- Framework servizi di testo enumerazione TITLEBAR_TYPE
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301685"
---
# <a name="titlebar_type-enumeration"></a><span data-ttu-id="fc02f-104">Enumerazione tipo di barra di titolo \_</span><span class="sxs-lookup"><span data-stu-id="fc02f-104">TITLEBAR\_TYPE enumeration</span></span>

<span data-ttu-id="fc02f-105">Gli elementi dell'enumerazione del **\_ tipo di barra** di titolo vengono usati per specificare i tipi di barra disponibili per una finestra di tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="fc02f-105">Elements of the **TITLEBAR\_TYPE** enumeration are used to specify types of titlebars that are available for a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc02f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc02f-106">Syntax</span></span>


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="fc02f-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="fc02f-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fc02f-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**BARRA titolo \_ None**</span><span class="sxs-lookup"><span data-stu-id="fc02f-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="fc02f-109">La finestra della tastiera soft non usa alcuna barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="fc02f-109">The soft keyboard window uses no titlebar.</span></span>

</dd> <dt>

<span data-ttu-id="fc02f-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**\_ \_ solo orizzontale di pinza della barra del titolo \_**</span><span class="sxs-lookup"><span data-stu-id="fc02f-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR\_GRIPPER\_HORIZ\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="fc02f-111">La finestra della tastiera soft usa solo una barra di pinza orizzontale.</span><span class="sxs-lookup"><span data-stu-id="fc02f-111">The soft keyboard window uses a horizontal gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="fc02f-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**BARRA del titolo \_ \_ solo verti \_**</span><span class="sxs-lookup"><span data-stu-id="fc02f-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR\_GRIPPER\_VERTI\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="fc02f-113">La finestra della tastiera soft usa solo una barra verticale di pinza.</span><span class="sxs-lookup"><span data-stu-id="fc02f-113">The soft keyboard window uses a vertical gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="fc02f-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**pulsante della barra del titolo \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fc02f-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TITLEBAR\_GRIPPER\_BUTTON**</span></span>
</dt> <dd>

<span data-ttu-id="fc02f-115">La finestra della tastiera soft usa solo un pulsante di pinza.</span><span class="sxs-lookup"><span data-stu-id="fc02f-115">The soft keyboard window uses a gripper button only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc02f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc02f-116">Requirements</span></span>



| <span data-ttu-id="fc02f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc02f-117">Requirement</span></span> | <span data-ttu-id="fc02f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fc02f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc02f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc02f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc02f-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc02f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fc02f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc02f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc02f-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fc02f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fc02f-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fc02f-123">Redistributable</span></span><br/>          | <span data-ttu-id="fc02f-124">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fc02f-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="fc02f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc02f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc02f-126"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc02f-126"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="fc02f-127">IDL</span><span class="sxs-lookup"><span data-stu-id="fc02f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc02f-128"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc02f-128"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





