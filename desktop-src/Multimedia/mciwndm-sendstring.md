---
title: Messaggio di MCIWNDM_SENDSTRING (VFW. h)
description: Il \_ messaggio MCIWNDM SENDSTRING Invia un comando MCI in formato stringa al dispositivo associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSendString.
ms.assetid: 0e999a0e-588d-4f06-a1bc-fd3f245d8980
keywords:
- MCIWNDM_SENDSTRING messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SENDSTRING
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36a034a3459803b1652bafed4eb389866add211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742487"
---
# <a name="mciwndm_sendstring-message"></a><span data-ttu-id="dd901-105">\_Messaggio MCIWNDM SENDSTRING</span><span class="sxs-lookup"><span data-stu-id="dd901-105">MCIWNDM\_SENDSTRING message</span></span>

<span data-ttu-id="dd901-106">Il messaggio **MCIWNDM \_ SENDSTRING** Invia un comando MCI in formato stringa al dispositivo associato alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="dd901-106">The **MCIWNDM\_SENDSTRING** message sends an MCI command in string form to the device associated with the MCIWnd window.</span></span> <span data-ttu-id="dd901-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) .</span><span class="sxs-lookup"><span data-stu-id="dd901-107">You can send this message explicitly or by using the [**MCIWndSendString**](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring) macro.</span></span>


```C++
MCIWNDM_SENDSTRING 
wParam = 0; 
lParam = (LPARAM) (LPSTR) sz; 
```



## <a name="parameters"></a><span data-ttu-id="dd901-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd901-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd901-109"><span id="sz"></span><span id="SZ"></span>*SZ*</span><span class="sxs-lookup"><span data-stu-id="dd901-109"><span id="sz"></span><span id="SZ"></span>*sz*</span></span>
</dt> <dd>

<span data-ttu-id="dd901-110">Comando stringa da inviare al dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="dd901-110">String command to send to the MCI device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd901-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd901-111">Return Value</span></span>

<span data-ttu-id="dd901-112">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="dd901-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd901-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd901-113">Remarks</span></span>

<span data-ttu-id="dd901-114">Il gestore di messaggi per **MCIWNDM \_ SENDSTRING** Accoda un alias del dispositivo al comando MCI inviato al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd901-114">The message handler for **MCIWNDM\_SENDSTRING** appends a device alias to the MCI command you send to the device.</span></span> <span data-ttu-id="dd901-115">Pertanto, non usare alcun alias in un comando MCI emesso con **MCIWNDM \_ SENDSTRING**.</span><span class="sxs-lookup"><span data-stu-id="dd901-115">Therefore, you should not use any alias in an MCI command that you issue with **MCIWNDM\_SENDSTRING**.</span></span>

<span data-ttu-id="dd901-116">Per ottenere la stringa restituita, che contiene il risultato del comando, inviare il messaggio [**MCIWNDM \_ RETURNSTRING**](mciwndm-returnstring.md) .</span><span class="sxs-lookup"><span data-stu-id="dd901-116">To get the return string, which contains the result of the command, send the [**MCIWNDM\_RETURNSTRING**](mciwndm-returnstring.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd901-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd901-117">Requirements</span></span>



| <span data-ttu-id="dd901-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd901-118">Requirement</span></span> | <span data-ttu-id="dd901-119">Valore</span><span class="sxs-lookup"><span data-stu-id="dd901-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dd901-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd901-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dd901-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd901-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dd901-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd901-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dd901-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd901-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dd901-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd901-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd901-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd901-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd901-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd901-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd901-127">**MCIWndSendString**</span><span class="sxs-lookup"><span data-stu-id="dd901-127">**MCIWndSendString**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsendstring)
</dt> <dt>

[<span data-ttu-id="dd901-128">Stringhe di comando multimediali</span><span class="sxs-lookup"><span data-stu-id="dd901-128">Multimedia Command Strings</span></span>](multimedia-command-strings.md)
</dt> </dl>

 

 





