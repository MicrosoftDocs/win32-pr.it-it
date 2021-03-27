---
description: Notifica a un AppBar che lo stato di Nascondi automaticamente o sempre in primo piano della barra delle applicazioni è stato modificato&\# 8212, ovvero l'utente ha selezionato o cancellato l'&\# 0034; Always on top&\# 0034; o &\# 0034; Nascondi automaticamente&\# 0034; casella di controllo nella finestra delle proprietà della barra delle applicazioni.
title: Messaggio ABN_STATECHANGE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878778"
---
# <a name="abn_statechange-message"></a><span data-ttu-id="58741-103">\_Messaggio STATECHANGE di ABN</span><span class="sxs-lookup"><span data-stu-id="58741-103">ABN\_STATECHANGE message</span></span>

<span data-ttu-id="58741-104">Notifica a un AppBar che lo stato di Nascondi automaticamente o della barra delle applicazioni è stato modificato, ovvero l'utente ha selezionato o deselezionato la casella di controllo "always on top" o "Nascondi automaticamente" nella finestra delle proprietà della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="58741-104">Notifies an appbar that the taskbar's autohide or always-on-top state has changed that is, the user has selected or cleared the "Always on top" or "Auto hide" check box on the taskbar's property sheet.</span></span>


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a><span data-ttu-id="58741-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="58741-105">Parameters</span></span>

<span data-ttu-id="58741-106">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="58741-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58741-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58741-107">Return value</span></span>

<span data-ttu-id="58741-108">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="58741-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58741-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="58741-109">Remarks</span></span>

<span data-ttu-id="58741-110">Un AppBar può utilizzare questo messaggio di notifica per impostare lo stato di conformità a quello della barra delle applicazioni, se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="58741-110">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="58741-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58741-111">Requirements</span></span>



| <span data-ttu-id="58741-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="58741-112">Requirement</span></span> | <span data-ttu-id="58741-113">Valore</span><span class="sxs-lookup"><span data-stu-id="58741-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58741-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58741-114">Minimum supported client</span></span><br/> | <span data-ttu-id="58741-115">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="58741-115">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="58741-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58741-116">Minimum supported server</span></span><br/> | <span data-ttu-id="58741-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="58741-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58741-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58741-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="58741-119"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="58741-119"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




