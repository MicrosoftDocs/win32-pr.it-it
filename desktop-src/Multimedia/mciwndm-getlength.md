---
title: Messaggio di MCIWNDM_GETLENGTH (VFW. h)
description: Il \_ messaggio MCIWNDM GetLength recupera la lunghezza del contenuto o del file attualmente utilizzato da un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- MCIWNDM_GETLENGTH messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2347647fcff0beb87be12b7f6a05790b97f36d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475527"
---
# <a name="mciwndm_getlength-message"></a><span data-ttu-id="79be8-105">\_Messaggio MCIWNDM GETlength</span><span class="sxs-lookup"><span data-stu-id="79be8-105">MCIWNDM\_GETLENGTH message</span></span>

<span data-ttu-id="79be8-106">Il messaggio **MCIWNDM \_ GetLength** recupera la lunghezza del contenuto o del file attualmente utilizzato da un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="79be8-106">The **MCIWNDM\_GETLENGTH** message retrieves the length of the content or file currently used by an MCI device.</span></span> <span data-ttu-id="79be8-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="79be8-107">You can send this message explicitly or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span>


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="79be8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79be8-108">Return Value</span></span>

<span data-ttu-id="79be8-109">Restituisce la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="79be8-109">Returns the length.</span></span> <span data-ttu-id="79be8-110">Le unità per la lunghezza dipendono dal formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="79be8-110">The units for the length depend on the current time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="79be8-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79be8-111">Requirements</span></span>



| <span data-ttu-id="79be8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="79be8-112">Requirement</span></span> | <span data-ttu-id="79be8-113">Valore</span><span class="sxs-lookup"><span data-stu-id="79be8-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="79be8-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79be8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="79be8-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79be8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="79be8-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79be8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="79be8-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79be8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="79be8-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79be8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="79be8-119"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="79be8-119"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79be8-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79be8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79be8-121">**MCIWndGetLength**</span><span class="sxs-lookup"><span data-stu-id="79be8-121">**MCIWndGetLength**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





