---
description: Imposta la dimensione e la posizione dello schermo di un AppBar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Messaggio ABM_SETPOS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525428"
---
# <a name="abm_setpos-message"></a><span data-ttu-id="930b6-103">\_Messaggio SETPOS ABM</span><span class="sxs-lookup"><span data-stu-id="930b6-103">ABM\_SETPOS message</span></span>

<span data-ttu-id="930b6-104">Imposta la dimensione e la posizione dello schermo di un AppBar.</span><span class="sxs-lookup"><span data-stu-id="930b6-104">Sets the size and screen position of an appbar.</span></span> <span data-ttu-id="930b6-105">Il messaggio specifica un bordo dello schermo e il rettangolo di delimitazione per AppBar.</span><span class="sxs-lookup"><span data-stu-id="930b6-105">The message specifies a screen edge and the bounding rectangle for the appbar.</span></span> <span data-ttu-id="930b6-106">Il sistema può regolare il rettangolo di delimitazione in modo che AppBar non interferisca con la barra delle applicazioni di Windows o con altre AppBar.</span><span class="sxs-lookup"><span data-stu-id="930b6-106">The system may adjust the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="930b6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="930b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930b6-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="930b6-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="930b6-109">Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="930b6-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="930b6-110">Il membro **uEdge** specifica un bordo dello schermo e il membro **RC** contiene il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="930b6-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the bounding rectangle.</span></span> <span data-ttu-id="930b6-111">Quando la funzione [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) restituisce, **RC** contiene il rettangolo di delimitazione approvato.</span><span class="sxs-lookup"><span data-stu-id="930b6-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="930b6-112">Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND**, **uEdge** e **RC** . tutti gli altri membri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="930b6-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930b6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="930b6-113">Return value</span></span>

<span data-ttu-id="930b6-114">Restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="930b6-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="930b6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="930b6-115">Remarks</span></span>

<span data-ttu-id="930b6-116">Questo messaggio consente al sistema di inviare il messaggio di notifica [**\_ POSCHANGED di ABN**](abn-poschanged.md) a tutti i AppBar.</span><span class="sxs-lookup"><span data-stu-id="930b6-116">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="930b6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="930b6-117">Requirements</span></span>



| <span data-ttu-id="930b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="930b6-118">Requirement</span></span> | <span data-ttu-id="930b6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="930b6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="930b6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="930b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="930b6-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="930b6-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="930b6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="930b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="930b6-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="930b6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="930b6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="930b6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="930b6-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="930b6-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




