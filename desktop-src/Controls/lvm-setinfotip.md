---
title: Messaggio LVM_SETINFOTIP (COMmctrl. h)
description: Imposta il testo della descrizione comando in risposta ritardata alla \_ notifica GETINFOTIP LVN.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- Controlli di Windows Message LVM_SETINFOTIP
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300976"
---
# <a name="lvm_setinfotip-message"></a><span data-ttu-id="1250d-104">\_Messaggio SETINFOTIP LVM</span><span class="sxs-lookup"><span data-stu-id="1250d-104">LVM\_SETINFOTIP message</span></span>

<span data-ttu-id="1250d-105">Imposta il testo della descrizione comando in risposta ritardata alla notifica [ \_ GETINFOTIP LVN](lvn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="1250d-105">Sets tooltip text in delayed response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification.</span></span>

## <a name="parameters"></a><span data-ttu-id="1250d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1250d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1250d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1250d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1250d-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1250d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1250d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1250d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1250d-110">Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> che contiene le informazioni da impostare.</span><span class="sxs-lookup"><span data-stu-id="1250d-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1250d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1250d-111">Return value</span></span>

<span data-ttu-id="1250d-112">Restituisce **true** se il testo della descrizione comando è impostato come riuscito; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="1250d-112">Returns **TRUE** if the tooltip text is set successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1250d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1250d-113">Remarks</span></span>

<span data-ttu-id="1250d-114">Il messaggio **LVM \_ SETINFOTIP** consente a un'applicazione di calcolare infotip in background attenendosi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="1250d-114">The **LVM\_SETINFOTIP** message lets an application calculate infotips in the background by performing the following steps:</span></span>

1.  <span data-ttu-id="1250d-115">In risposta alla notifica [ \_ GETINFOTIP di LVN](lvn-getinfotip.md) , impostare il membro **pszText** della struttura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) su una stringa vuota e restituire 0.</span><span class="sxs-lookup"><span data-stu-id="1250d-115">In response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification, set the **pszText** member of the [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure to an empty string and return 0.</span></span>
2.  <span data-ttu-id="1250d-116">In background, calcolare l'infotip.</span><span class="sxs-lookup"><span data-stu-id="1250d-116">In the background, compute the infotip.</span></span>
3.  <span data-ttu-id="1250d-117">Dopo aver calcolato il infotip, inviare il messaggio **LVM \_ SETINFOTIP** , impostando il membro **pszText** della struttura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sui membri infotip e iItem e **iSubItem** sull'elemento **e sull'elemento** secondario a cui si applica infotip.</span><span class="sxs-lookup"><span data-stu-id="1250d-117">After computing the infotip, send the **LVM\_SETINFOTIP** message, setting the **pszText** member of the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure to the infotip and the **iItem** and **iSubItem** members to the item and sub-item to which the infotip applies.</span></span>

<span data-ttu-id="1250d-118">Il testo passato al messaggio **LVM \_ SETINFOTIP** viene visualizzato solo se l'elemento e l'elemento secondario descritti dalla struttura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) sono ancora in uno stato che richiede un infotip</span><span class="sxs-lookup"><span data-stu-id="1250d-118">The text passed to the **LVM\_SETINFOTIP** message appears only if the item and sub-item described by the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure are still in a state that requires an infotip</span></span>

> [!Note]  
> <span data-ttu-id="1250d-119">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="1250d-119">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1250d-120">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1250d-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1250d-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1250d-121">Requirements</span></span>



| <span data-ttu-id="1250d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1250d-122">Requirement</span></span> | <span data-ttu-id="1250d-123">Valore</span><span class="sxs-lookup"><span data-stu-id="1250d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1250d-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1250d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1250d-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1250d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1250d-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1250d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1250d-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1250d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1250d-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1250d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1250d-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1250d-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





