---
title: Messaggio di EM_SETTARGETDEVICE (RichEdit. h)
description: Imposta il dispositivo di destinazione e lo spessore della riga usati per \ 0034; ciò che viene visualizzato è quello che si ottiene \ 0034; (WYSIWYG) formattazione in un controllo Rich Edit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- Controlli di Windows Message EM_SETTARGETDEVICE
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120127"
---
# <a name="em_settargetdevice-message"></a><span data-ttu-id="849af-104">\_Messaggio SETTARGETDEVICE em</span><span class="sxs-lookup"><span data-stu-id="849af-104">EM\_SETTARGETDEVICE message</span></span>

<span data-ttu-id="849af-105">Imposta il dispositivo di destinazione e la lunghezza di riga usati per la formattazione "What You See is what you get" (WYSIWYG) in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="849af-105">Sets the target device and line width used for "what you see is what you get" (WYSIWYG) formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="849af-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="849af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="849af-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="849af-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="849af-108">HDC per il dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="849af-108">HDC for the target device.</span></span>

</dd> <dt>

<span data-ttu-id="849af-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="849af-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="849af-110">Spessore riga da usare per la formattazione.</span><span class="sxs-lookup"><span data-stu-id="849af-110">Line width to use for formatting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="849af-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="849af-111">Return value</span></span>

<span data-ttu-id="849af-112">Il valore restituito è zero se l'operazione ha esito negativo o è diverso da zero se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="849af-112">The return value is zero if the operation fails, or nonzero if it succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="849af-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="849af-113">Remarks</span></span>

<span data-ttu-id="849af-114">HDC per la stampante predefinita può essere ottenuto come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="849af-114">The HDC for the default printer can be obtained as follows.</span></span>


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



<span data-ttu-id="849af-115">Se *lParam* è zero, non vengono create interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="849af-115">If *lParam* is zero, no line breaks are created.</span></span>

## <a name="requirements"></a><span data-ttu-id="849af-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="849af-116">Requirements</span></span>



| <span data-ttu-id="849af-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="849af-117">Requirement</span></span> | <span data-ttu-id="849af-118">Valore</span><span class="sxs-lookup"><span data-stu-id="849af-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="849af-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="849af-119">Minimum supported client</span></span><br/> | <span data-ttu-id="849af-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="849af-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="849af-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="849af-121">Minimum supported server</span></span><br/> | <span data-ttu-id="849af-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="849af-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="849af-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="849af-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="849af-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="849af-124"><dt>Richedit.h</dt></span></span> </dl> |



 

 





