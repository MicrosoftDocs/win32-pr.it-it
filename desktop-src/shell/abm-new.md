---
description: Registra un nuovo AppBar e specifica l'identificatore del messaggio che il sistema deve utilizzare per inviare i messaggi di notifica. Un AppBar deve inviare questo messaggio prima di inviare altri messaggi di AppBar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Messaggio ABM_NEW (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750311"
---
# <a name="abm_new-message"></a><span data-ttu-id="6a3ba-104">\_Nuovo messaggio di ABM</span><span class="sxs-lookup"><span data-stu-id="6a3ba-104">ABM\_NEW message</span></span>

<span data-ttu-id="6a3ba-105">Registra un nuovo AppBar e specifica l'identificatore del messaggio che il sistema deve utilizzare per inviare i messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-105">Registers a new appbar and specifies the message identifier that the system should use to send it notification messages.</span></span> <span data-ttu-id="6a3ba-106">Un AppBar deve inviare questo messaggio prima di inviare altri messaggi di AppBar.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-106">An appbar should send this message before sending any other appbar messages.</span></span>


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="6a3ba-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a3ba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a3ba-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="6a3ba-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="6a3ba-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che contiene il nuovo handle della finestra di AppBar e l'identificatore del messaggio.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the new appbar's window handle and message identifier.</span></span> <span data-ttu-id="6a3ba-110">Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND** e **uCallbackMessage** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-110">You must specify the **cbSize**, **hWnd**, and **uCallbackMessage** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a3ba-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a3ba-111">Return value</span></span>

<span data-ttu-id="6a3ba-112">Restituisce **true** se ha esito positivo o **false** se si verifica un errore o se il AppBar è già registrato.</span><span class="sxs-lookup"><span data-stu-id="6a3ba-112">Returns **TRUE** if successful, or **FALSE** if an error occurs or if the appbar is already registered.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a3ba-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a3ba-113">Requirements</span></span>



| <span data-ttu-id="6a3ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a3ba-114">Requirement</span></span> | <span data-ttu-id="6a3ba-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6a3ba-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a3ba-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a3ba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a3ba-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6a3ba-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6a3ba-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a3ba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a3ba-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a3ba-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a3ba-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a3ba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a3ba-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a3ba-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




