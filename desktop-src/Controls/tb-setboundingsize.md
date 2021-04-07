---
title: Messaggio TB_SETBOUNDINGSIZE (COMmctrl. h)
description: Imposta la dimensione di delimitazione per un controllo della barra degli strumenti a più colonne.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- Controlli di Windows Message TB_SETBOUNDINGSIZE
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873285"
---
# <a name="tb_setboundingsize-message"></a><span data-ttu-id="01a96-104">TB \_ SETBOUNDINGSIZE messaggio</span><span class="sxs-lookup"><span data-stu-id="01a96-104">TB\_SETBOUNDINGSIZE message</span></span>

<span data-ttu-id="01a96-105">\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="01a96-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="01a96-106">Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="01a96-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="01a96-107">Imposta la dimensione di delimitazione per un controllo della barra degli strumenti a più colonne.</span><span class="sxs-lookup"><span data-stu-id="01a96-107">Sets the bounding size for a multi-column toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="01a96-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01a96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01a96-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01a96-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01a96-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="01a96-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="01a96-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01a96-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01a96-112">Puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) il cui membro **CY** contiene l'altezza di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="01a96-112">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure whose **cy** member contains the bounding height.</span></span> <span data-ttu-id="01a96-113">Il membro **CX** (la larghezza) viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="01a96-113">The **cx** member (the width) is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01a96-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01a96-114">Return value</span></span>

<span data-ttu-id="01a96-115">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="01a96-115">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="01a96-116">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="01a96-116">Security Considerations</span></span>

<span data-ttu-id="01a96-117">L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="01a96-117">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="01a96-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="01a96-118">Remarks</span></span>

<span data-ttu-id="01a96-119">La dimensione di delimitazione controlla la modalità di organizzazione dei pulsanti in colonne.</span><span class="sxs-lookup"><span data-stu-id="01a96-119">The bounding size controls how buttons are organized into columns.</span></span> <span data-ttu-id="01a96-120">Se il controllo Toolbar non ha lo stile [**\_ \_ multicolonna TBSTYLE ex**](toolbar-extended-styles.md) , questo messaggio non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="01a96-120">If the toolbar control does not have the [**TBSTYLE\_EX\_MULTICOLUMN**](toolbar-extended-styles.md) style, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a96-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01a96-121">Requirements</span></span>



| <span data-ttu-id="01a96-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="01a96-122">Requirement</span></span> | <span data-ttu-id="01a96-123">Valore</span><span class="sxs-lookup"><span data-stu-id="01a96-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01a96-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a96-124">Minimum supported client</span></span><br/> | <span data-ttu-id="01a96-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01a96-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01a96-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01a96-126">Minimum supported server</span></span><br/> | <span data-ttu-id="01a96-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01a96-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01a96-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01a96-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a96-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01a96-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

