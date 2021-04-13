---
title: Messaggio MM_MCISIGNAL (mmsystem. h)
description: Il \_ messaggio mm MCISIGNAL viene inviato a una finestra per notificare a un'applicazione che un dispositivo MCI ha raggiunto una posizione definita in un comando precedente ( \_ segnale MCI).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400805"
---
# <a name="mm_mcisignal-message"></a><span data-ttu-id="eca2c-104">\_Messaggio MCISIGNAL mm</span><span class="sxs-lookup"><span data-stu-id="eca2c-104">MM\_MCISIGNAL message</span></span>

<span data-ttu-id="eca2c-105">Il messaggio **mm \_ MCISIGNAL** viene inviato a una finestra per notificare a un'applicazione che un dispositivo MCI ha raggiunto una posizione definita in un [**comando precedente (**](signal.md) [**\_ segnale MCI**](mci-signal.md)).</span><span class="sxs-lookup"><span data-stu-id="eca2c-105">The **MM\_MCISIGNAL** message is sent to a window to notify an application that an MCI device has reached a position defined in a previous [**signal**](signal.md) ( [**MCI\_SIGNAL**](mci-signal.md)) command.</span></span>


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a><span data-ttu-id="eca2c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eca2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eca2c-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span><span class="sxs-lookup"><span data-stu-id="eca2c-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span></span>
</dt> <dd>

<span data-ttu-id="eca2c-108">Identificatore del dispositivo che avvia il messaggio del segnale.</span><span class="sxs-lookup"><span data-stu-id="eca2c-108">Identifier of the device initiating the signal message.</span></span>

</dd> <dt>

<span data-ttu-id="eca2c-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span><span class="sxs-lookup"><span data-stu-id="eca2c-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span></span>
</dt> <dd>

<span data-ttu-id="eca2c-110">Valore passato nel membro **dwUserParm** della struttura del **\_ \_ \_ parametro Signal DGV di MCI** quando il comando **Signal** ha definito questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="eca2c-110">Value passed in the **dwUserParm** member of the **MCI\_DGV\_SIGNAL\_PARAMS** structure when the **signal** command has defined this callback function.</span></span> <span data-ttu-id="eca2c-111">In alternativa, può contenere il valore Position.</span><span class="sxs-lookup"><span data-stu-id="eca2c-111">Alternatively, it might contain the position value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eca2c-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eca2c-112">Requirements</span></span>



| <span data-ttu-id="eca2c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="eca2c-113">Requirement</span></span> | <span data-ttu-id="eca2c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="eca2c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca2c-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eca2c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="eca2c-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eca2c-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eca2c-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eca2c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="eca2c-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="eca2c-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eca2c-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eca2c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="eca2c-120"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eca2c-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca2c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eca2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca2c-122">MCI</span><span class="sxs-lookup"><span data-stu-id="eca2c-122">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="eca2c-123">Messaggi MCI</span><span class="sxs-lookup"><span data-stu-id="eca2c-123">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="eca2c-124">**signal**</span><span class="sxs-lookup"><span data-stu-id="eca2c-124">**signal**</span></span>](signal.md)
</dt> </dl>

 

 





