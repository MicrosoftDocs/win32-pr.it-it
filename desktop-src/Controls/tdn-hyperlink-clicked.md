---
title: Codice di notifica TDN_HYPERLINK_CLICKED (COMmctrl. h)
description: Inviato da una finestra di dialogo attività quando l'utente fa clic su un collegamento ipertestuale nel contenuto della finestra di dialogo attività. Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo TaskDialogIndirect.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- Controlli di Windows per il codice di notifica TDN_HYPERLINK_CLICKED
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121474"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a><span data-ttu-id="e4411-105">\_Codice di \_ notifica fatto clic sul collegamento IPERtestuale TDN</span><span class="sxs-lookup"><span data-stu-id="e4411-105">TDN\_HYPERLINK\_CLICKED notification code</span></span>

<span data-ttu-id="e4411-106">Inviato da una finestra di dialogo attività quando l'utente fa clic su un collegamento ipertestuale nel contenuto della finestra di dialogo attività.</span><span class="sxs-lookup"><span data-stu-id="e4411-106">Sent by a task dialog when the user clicks a hyperlink in the task dialog content.</span></span> <span data-ttu-id="e4411-107">Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="e4411-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="e4411-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4411-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4411-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e4411-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4411-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e4411-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e4411-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e4411-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e4411-112">Puntatore a una stringa di caratteri wide contenente l'URL del collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="e4411-112">Pointer to a wide-character string containing the URL of the hyperlink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4411-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4411-113">Return value</span></span>

<span data-ttu-id="e4411-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="e4411-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4411-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4411-115">Requirements</span></span>



| <span data-ttu-id="e4411-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4411-116">Requirement</span></span> | <span data-ttu-id="e4411-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e4411-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4411-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4411-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e4411-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e4411-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4411-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4411-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e4411-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e4411-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4411-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4411-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4411-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4411-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





