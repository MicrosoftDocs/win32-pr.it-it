---
title: Messaggio di MCIWNDM_NEW (VFW. h)
description: Il \_ nuovo messaggio MCIWNDM crea un nuovo file per il dispositivo MCI corrente. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndNew.
ms.assetid: 18b2340d-8303-415a-867f-bd346034db2a
keywords:
- MCIWNDM_NEW messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_NEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293323cd0404da45e648024b35b7f96ef60fea61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741162"
---
# <a name="mciwndm_new-message"></a><span data-ttu-id="6858c-105">MCIWNDM \_ nuovo messaggio</span><span class="sxs-lookup"><span data-stu-id="6858c-105">MCIWNDM\_NEW message</span></span>

<span data-ttu-id="6858c-106">Il **\_ nuovo messaggio MCIWNDM** crea un nuovo file per il dispositivo MCI corrente.</span><span class="sxs-lookup"><span data-stu-id="6858c-106">The **MCIWNDM\_NEW** message creates a new file for the current MCI device.</span></span> <span data-ttu-id="6858c-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) .</span><span class="sxs-lookup"><span data-stu-id="6858c-107">You can send this message explicitly or by using the [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro.</span></span>


```C++
MCIWNDM_NEW 
wParam = 0; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a><span data-ttu-id="6858c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6858c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6858c-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="6858c-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="6858c-110">Puntatore a un buffer contenente il nome del dispositivo MCI che utilizzerà il file.</span><span class="sxs-lookup"><span data-stu-id="6858c-110">Pointer to a buffer containing the name of the MCI device that will use the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6858c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6858c-111">Return Value</span></span>

<span data-ttu-id="6858c-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="6858c-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6858c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6858c-113">Requirements</span></span>



| <span data-ttu-id="6858c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6858c-114">Requirement</span></span> | <span data-ttu-id="6858c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6858c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6858c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6858c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6858c-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6858c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6858c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6858c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6858c-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6858c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6858c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6858c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6858c-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6858c-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6858c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6858c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6858c-123">**MCIWndNew**</span><span class="sxs-lookup"><span data-stu-id="6858c-123">**MCIWndNew**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)
</dt> </dl>

 

 





