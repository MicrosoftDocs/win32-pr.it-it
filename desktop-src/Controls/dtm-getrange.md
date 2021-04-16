---
title: Messaggio DTM_GETRANGE (COMmctrl. h)
description: Ottiene l'ora di sistema corrente minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetRange.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- Controlli di Windows Message DTM_GETRANGE
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477933"
---
# <a name="dtm_getrange-message"></a><span data-ttu-id="6381e-105">\_Messaggio GETRANGE DTM</span><span class="sxs-lookup"><span data-stu-id="6381e-105">DTM\_GETRANGE message</span></span>

<span data-ttu-id="6381e-106">Ottiene l'ora di sistema corrente minima e massima consentita per un controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="6381e-106">Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="6381e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .</span><span class="sxs-lookup"><span data-stu-id="6381e-107">You can send this message explicitly or use the [**DateTime\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6381e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6381e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6381e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6381e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6381e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6381e-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6381e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6381e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6381e-112">Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="6381e-112">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6381e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6381e-113">Return value</span></span>

<span data-ttu-id="6381e-114">Restituisce un valore **DWORD** che corrisponde a una combinazione di GDTR \_ min o GDTR \_ max.</span><span class="sxs-lookup"><span data-stu-id="6381e-114">Returns a **DWORD** value that is a combination of GDTR\_MIN or GDTR\_MAX.</span></span> <span data-ttu-id="6381e-115">Il primo elemento della matrice [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contiene il tempo minimo consentito se \_ è impostato GDTR min.</span><span class="sxs-lookup"><span data-stu-id="6381e-115">The first element of the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) array contains the minimum allowable time if GDTR\_MIN is set.</span></span> <span data-ttu-id="6381e-116">Il secondo elemento della matrice **SYSTEMTIME** contiene il tempo massimo consentito se \_ è impostato GDTR max.</span><span class="sxs-lookup"><span data-stu-id="6381e-116">The second element of the **SYSTEMTIME** array contains the maximum allowable time if GDTR\_MAX is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="6381e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6381e-117">Remarks</span></span>

<span data-ttu-id="6381e-118">Il selettore di data e ora Visualizza solo le date e le ore che rientrano nell'intervallo specificato, impedendo all'utente di selezionare una data e un'ora non comprese nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="6381e-118">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="6381e-119">Se il [**messaggio \_ SETSYSTEMTIME di DTM**](dtm-setsystemtime.md) specifica una data e un'ora che non rientrano nell'intervallo, l'operazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6381e-119">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6381e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6381e-120">Requirements</span></span>



| <span data-ttu-id="6381e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6381e-121">Requirement</span></span> | <span data-ttu-id="6381e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6381e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6381e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6381e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6381e-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6381e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6381e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6381e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6381e-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6381e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6381e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6381e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6381e-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6381e-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

