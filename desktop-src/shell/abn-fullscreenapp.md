---
description: Notifica a un AppBar quando un'applicazione a schermo intero è in fase di apertura o chiusura. Questa notifica viene inviata sotto forma di messaggio definito dall'applicazione impostato dal \_ nuovo messaggio ABM.
title: Messaggio ABN_FULLSCREENAPP (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128475"
---
# <a name="abn_fullscreenapp-message"></a><span data-ttu-id="b0714-104">\_Messaggio FULLSCREENAPP di ABN</span><span class="sxs-lookup"><span data-stu-id="b0714-104">ABN\_FULLSCREENAPP message</span></span>

<span data-ttu-id="b0714-105">Notifica a un AppBar quando un'applicazione a schermo intero è in fase di apertura o chiusura.</span><span class="sxs-lookup"><span data-stu-id="b0714-105">Notifies an appbar when a full-screen application is opening or closing.</span></span> <span data-ttu-id="b0714-106">Questa notifica viene inviata sotto forma di messaggio definito dall'applicazione impostato dal [**\_ nuovo messaggio ABM**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="b0714-106">This notification is sent in the form of an application-defined message that is set by the [**ABM\_NEW**](abm-new.md) message.</span></span>


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a><span data-ttu-id="b0714-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0714-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0714-108">*fOpen*</span><span class="sxs-lookup"><span data-stu-id="b0714-108">*fOpen*</span></span> 
</dt> <dd>

<span data-ttu-id="b0714-109">Flag che specifica se un'applicazione a schermo intero è in apertura o in chiusura.</span><span class="sxs-lookup"><span data-stu-id="b0714-109">A flag specifying whether a full-screen application is opening or closing.</span></span> <span data-ttu-id="b0714-110">Questo parametro è **true** se l'applicazione è in apertura o **false** se è in chiusura.</span><span class="sxs-lookup"><span data-stu-id="b0714-110">This parameter is **TRUE** if the application is opening or **FALSE** if it is closing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0714-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0714-111">Return value</span></span>

<span data-ttu-id="b0714-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b0714-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0714-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0714-113">Remarks</span></span>

<span data-ttu-id="b0714-114">Quando si apre un'applicazione a schermo intero, un AppBar deve essere rilasciato nella parte inferiore dell'ordine z.</span><span class="sxs-lookup"><span data-stu-id="b0714-114">When a full-screen application is opening, an appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="b0714-115">Quando viene chiuso, il AppBar deve ripristinare la posizione dell'ordine z.</span><span class="sxs-lookup"><span data-stu-id="b0714-115">When it is closing, the appbar should restore its z-order position.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0714-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0714-116">Requirements</span></span>



| <span data-ttu-id="b0714-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0714-117">Requirement</span></span> | <span data-ttu-id="b0714-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b0714-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0714-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0714-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0714-120">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b0714-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b0714-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0714-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0714-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b0714-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0714-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0714-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0714-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0714-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




