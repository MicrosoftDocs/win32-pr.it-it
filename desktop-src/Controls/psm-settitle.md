---
title: Messaggio PSM_SETTITLE (Prsht. h)
description: Imposta il titolo di una finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- Controlli di Windows Message PSM_SETTITLE
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963799"
---
# <a name="psm_settitle-message"></a><span data-ttu-id="df706-105">\_Messaggio di proprietà PSM</span><span class="sxs-lookup"><span data-stu-id="df706-105">PSM\_SETTITLE message</span></span>

<span data-ttu-id="df706-106">Imposta il titolo di una finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="df706-106">Sets the title of a property sheet.</span></span> <span data-ttu-id="df706-107">È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .</span><span class="sxs-lookup"><span data-stu-id="df706-107">You can send this message explicitly or by using the [**PropSheet\_SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="df706-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df706-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df706-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df706-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df706-110">Flag che indica se includere il prefisso "Properties per" o il suffisso "Properties" (a seconda della versione) con la stringa del titolo specificata.</span><span class="sxs-lookup"><span data-stu-id="df706-110">Flag that indicates whether to include the prefix "Properties for" or the suffix "Properties" (depending on the version) with the specified title string.</span></span> <span data-ttu-id="df706-111">Se questo valore è PSH \_ PROPTITLE, viene incluso il prefisso o il suffisso.</span><span class="sxs-lookup"><span data-stu-id="df706-111">If this value is PSH\_PROPTITLE, the prefix or suffix is included.</span></span>

</dd> <dt>

<span data-ttu-id="df706-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df706-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df706-113">Puntatore a un buffer contenente la stringa del titolo.</span><span class="sxs-lookup"><span data-stu-id="df706-113">Pointer to a buffer that contains the title string.</span></span> <span data-ttu-id="df706-114">Se il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) di questo parametro è **null**, la finestra delle proprietà carica la risorsa di stringa specificata in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df706-114">If the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this parameter is **NULL**, the property sheet loads the string resource specified in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df706-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df706-115">Return value</span></span>

<span data-ttu-id="df706-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="df706-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df706-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="df706-117">Remarks</span></span>

<span data-ttu-id="df706-118">In una procedura guidata Aero questo messaggio può essere utilizzato per modificare dinamicamente il titolo di una pagina interna; ad esempio, quando si gestisce la notifica [ \_ seactive PSN](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="df706-118">In an Aero Wizard, this message can be used to change the title of an interior page dynamically; for example, when handling the [PSN\_SETACTIVE](psn-setactive.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="df706-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df706-119">Requirements</span></span>



| <span data-ttu-id="df706-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="df706-120">Requirement</span></span> | <span data-ttu-id="df706-121">Valore</span><span class="sxs-lookup"><span data-stu-id="df706-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df706-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df706-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df706-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df706-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="df706-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df706-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df706-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="df706-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df706-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df706-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="df706-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="df706-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="df706-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="df706-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="df706-129">**PSM \_ SETTITLEW** (Unicode) e **PSM \_ setitlea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="df706-129">**PSM\_SETTITLEW** (Unicode) and **PSM\_SETTITLEA** (ANSI)</span></span><br/>              |



 

