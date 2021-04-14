---
description: Richiede una dimensione e una posizione dello schermo per un AppBar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Messaggio ABM_QUERYPOS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342866"
---
# <a name="abm_querypos-message"></a><span data-ttu-id="6ab9b-103">\_Messaggio QUERYPOS ABM</span><span class="sxs-lookup"><span data-stu-id="6ab9b-103">ABM\_QUERYPOS message</span></span>

<span data-ttu-id="6ab9b-104">Richiede una dimensione e una posizione dello schermo per un AppBar.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-104">Requests a size and screen position for an appbar.</span></span> <span data-ttu-id="6ab9b-105">Quando viene effettuata la richiesta, il messaggio propone un bordo dello schermo e un rettangolo di delimitazione per AppBar.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-105">When the request is made, the message proposes a screen edge and a bounding rectangle for the appbar.</span></span> <span data-ttu-id="6ab9b-106">Il sistema regola il rettangolo di delimitazione in modo che AppBar non interferisca con la barra delle applicazioni di Windows o con altre AppBar.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-106">The system adjusts the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="6ab9b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ab9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab9b-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="6ab9b-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab9b-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="6ab9b-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="6ab9b-110">Il membro **uEdge** specifica un bordo dello schermo e il membro **RC** contiene il rettangolo di delimitazione proposto.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the proposed bounding rectangle.</span></span> <span data-ttu-id="6ab9b-111">Quando la funzione [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) restituisce, **RC** contiene il rettangolo di delimitazione approvato.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="6ab9b-112">Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge** e **RC** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab9b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ab9b-113">Return value</span></span>

<span data-ttu-id="6ab9b-114">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="6ab9b-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab9b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ab9b-115">Remarks</span></span>

<span data-ttu-id="6ab9b-116">Un AppBar deve inviare questo messaggio prima di inviare il messaggio di [**\_ SETPOS ABM**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="6ab9b-116">An appbar should send this message before sending the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab9b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ab9b-117">Requirements</span></span>



| <span data-ttu-id="6ab9b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab9b-118">Requirement</span></span> | <span data-ttu-id="6ab9b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6ab9b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab9b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ab9b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab9b-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6ab9b-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6ab9b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ab9b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab9b-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ab9b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ab9b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ab9b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab9b-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab9b-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




