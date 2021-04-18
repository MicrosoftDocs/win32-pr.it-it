---
title: Messaggio MMIOM_CLOSE (mmsystem. h)
description: Il \_ messaggio MMIOM Close viene inviato a una routine di i/O dalla funzione mmioClose per richiedere che un file venga chiuso.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- MMIOM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519294"
---
# <a name="mmiom_close-message"></a><span data-ttu-id="b0132-104">\_Messaggio di chiusura MMIOM</span><span class="sxs-lookup"><span data-stu-id="b0132-104">MMIOM\_CLOSE message</span></span>

<span data-ttu-id="b0132-105">Il messaggio **MMIOM \_ Close** viene inviato a una routine di i/O dalla funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) per richiedere che un file venga chiuso.</span><span class="sxs-lookup"><span data-stu-id="b0132-105">The **MMIOM\_CLOSE** message is sent to an I/O procedure by the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to request that a file be closed.</span></span>


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b0132-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0132-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span><span class="sxs-lookup"><span data-stu-id="b0132-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span></span>
</dt> <dd>

<span data-ttu-id="b0132-108">Flag contenuti nel parametro **wFlags** di **mmioClose**.</span><span class="sxs-lookup"><span data-stu-id="b0132-108">Flags contained in the **wFlags** parameter of **mmioClose**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0132-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0132-109">Return Value</span></span>

<span data-ttu-id="b0132-110">Restituisce zero se il file è stato chiuso correttamente o un errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b0132-110">Returns zero if the file is successfully closed or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0132-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0132-111">Requirements</span></span>



| <span data-ttu-id="b0132-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0132-112">Requirement</span></span> | <span data-ttu-id="b0132-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b0132-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0132-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0132-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b0132-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0132-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0132-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0132-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b0132-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0132-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0132-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0132-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0132-119"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0132-119"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

