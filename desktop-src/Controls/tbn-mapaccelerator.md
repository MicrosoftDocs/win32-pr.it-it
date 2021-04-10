---
title: Codice di notifica TBN_MAPACCELERATOR (COMmctrl. h)
description: Richiede l'indice del pulsante sulla barra degli strumenti corrispondente al carattere dell'acceleratore specificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- Controlli di Windows per il codice di notifica TBN_MAPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963751"
---
# <a name="tbn_mapaccelerator-notification-code"></a><span data-ttu-id="5321c-105">\_Codice di notifica MAPACCELERATOR di TBN</span><span class="sxs-lookup"><span data-stu-id="5321c-105">TBN\_MAPACCELERATOR notification code</span></span>

<span data-ttu-id="5321c-106">Richiede l'indice del pulsante sulla barra degli strumenti corrispondente al carattere dell'acceleratore specificato.</span><span class="sxs-lookup"><span data-stu-id="5321c-106">Requests the index of the button in the toolbar corresponding to the specified accelerator character.</span></span> <span data-ttu-id="5321c-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5321c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5321c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5321c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5321c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5321c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5321c-110">Puntatore a una struttura [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) che contiene il carattere del tasto di scelta rapida e che riceve l'indice del pulsante corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5321c-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains the accelerator key character and that receives the index of the corresponding button.</span></span> <span data-ttu-id="5321c-111">Il campo **dwItemNext** è-1 se il tasto di scelta rapida non corrisponde a un comando.</span><span class="sxs-lookup"><span data-stu-id="5321c-111">The **dwItemNext** field is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5321c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5321c-112">Return value</span></span>

<span data-ttu-id="5321c-113">TRUE se **NMCHAR. dwItemNext** è impostato su un valore.</span><span class="sxs-lookup"><span data-stu-id="5321c-113">TRUE if **NMCHAR.dwItemNext** is set to a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5321c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5321c-114">Requirements</span></span>



| <span data-ttu-id="5321c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5321c-115">Requirement</span></span> | <span data-ttu-id="5321c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5321c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5321c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5321c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5321c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5321c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5321c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5321c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5321c-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5321c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5321c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5321c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5321c-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5321c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





