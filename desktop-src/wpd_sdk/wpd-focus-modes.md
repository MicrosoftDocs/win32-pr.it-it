---
description: Il \_ tipo di enumerazione WPD Focus Modes \_ descrive la modalità messa a fuoco usata da un dispositivo di acquisizione di immagini ancora.
ms.assetid: 3b092391-e4c1-4586-8df4-b58a1dcccc81
title: Enumerazione WPD_FOCUS_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_FOCUS_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e7e1dc50f115fbd2ace84a3b631d37a42e1c4ba7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328964"
---
# <a name="wpd_focus_modes-enumeration"></a><span data-ttu-id="c1b06-103">\_Enumerazione WPD Focus \_ modes</span><span class="sxs-lookup"><span data-stu-id="c1b06-103">WPD\_FOCUS\_MODES enumeration</span></span>

<span data-ttu-id="c1b06-104">Il tipo di enumerazione **WPD \_ Focus \_** Modes descrive la modalità messa a fuoco usata da un dispositivo di acquisizione di immagini ancora.</span><span class="sxs-lookup"><span data-stu-id="c1b06-104">The **WPD\_FOCUS\_MODES** enumeration type describes the focus mode used by a still image capture device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1b06-105">Syntax</span></span>


```C++
typedef enum WPD_FOCUS_MODES { 
  WPD_FOCUS_UNDEFINED        = 0,
  WPD_FOCUS_MANUAL           = 1,
  WPD_FOCUS_AUTOMATIC        = 2,
  WPD_FOCUS_AUTOMATIC_MACRO  = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="c1b06-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c1b06-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c1b06-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**lo \_ stato attivo WPD non è \_ definito**</span><span class="sxs-lookup"><span data-stu-id="c1b06-107"><span id="WPD_FOCUS_UNDEFINED"></span><span id="wpd_focus_undefined"></span>**WPD\_FOCUS\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-108">La modalità messa a fuoco non è stata specificata.</span><span class="sxs-lookup"><span data-stu-id="c1b06-108">The focus mode has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**Manuale di WPD \_ Focus \_**</span><span class="sxs-lookup"><span data-stu-id="c1b06-109"><span id="WPD_FOCUS_MANUAL"></span><span id="wpd_focus_manual"></span>**WPD\_FOCUS\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-110">Specifica lo stato attivo manuale.</span><span class="sxs-lookup"><span data-stu-id="c1b06-110">Specifies manual focus.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD \_ messa a fuoco \_ automatica**</span><span class="sxs-lookup"><span data-stu-id="c1b06-111"><span id="WPD_FOCUS_AUTOMATIC"></span><span id="wpd_focus_automatic"></span>**WPD\_FOCUS\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-112">Specifica lo stato attivo automatico, controllato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c1b06-112">Specifies automatic focus, controlled by the device.</span></span>

</dd> <dt>

<span data-ttu-id="c1b06-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**\_macro messa a fuoco \_ automatica WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c1b06-113"><span id="WPD_FOCUS_AUTOMATIC_MACRO"></span><span id="wpd_focus_automatic_macro"></span>**WPD\_FOCUS\_AUTOMATIC\_MACRO**</span></span>
</dt> <dd>

<span data-ttu-id="c1b06-114">Specifica che il dispositivo deve passare automaticamente tra la macro e lo stato attivo normale, a seconda delle esigenze.</span><span class="sxs-lookup"><span data-stu-id="c1b06-114">Specifies that the device should automatically switch between macro and normal focus, as required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1b06-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1b06-115">Remarks</span></span>

<span data-ttu-id="c1b06-116">Questa enumerazione viene utilizzata dalla proprietà [WPD \_ still \_ Image \_ Focus \_ mode](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b06-116">This enumeration is used by the [WPD\_STILL\_IMAGE\_FOCUS\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b06-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1b06-117">Requirements</span></span>



| <span data-ttu-id="c1b06-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1b06-118">Requirement</span></span> | <span data-ttu-id="c1b06-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c1b06-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b06-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1b06-120">Header</span></span><br/> | <dl> <span data-ttu-id="c1b06-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b06-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b06-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1b06-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b06-123">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="c1b06-123">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




