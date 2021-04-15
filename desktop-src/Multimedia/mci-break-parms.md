---
title: Struttura MCI_BREAK_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri di MCI break contiene il codice della chiave virtuale e le informazioni della finestra per il \_ comando MCI break.
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- Struttura MCI_BREAK_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517631"
---
# <a name="mci_break_parms-structure"></a><span data-ttu-id="19acf-104">\_ \_ Struttura parametri break MCI</span><span class="sxs-lookup"><span data-stu-id="19acf-104">MCI\_BREAK\_PARMS structure</span></span>

<span data-ttu-id="19acf-105">La **struttura \_ \_ parametri di MCI break** contiene il codice della chiave virtuale e le informazioni della finestra per il comando [**MCI \_ break**](mci-break.md) .</span><span class="sxs-lookup"><span data-stu-id="19acf-105">The **MCI\_BREAK\_PARMS** structure contains virtual-key code and window information for the [**MCI\_BREAK**](mci-break.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="19acf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19acf-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a><span data-ttu-id="19acf-107">Members</span><span class="sxs-lookup"><span data-stu-id="19acf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="19acf-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="19acf-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="19acf-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="19acf-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="19acf-110">**nVirtKey**</span><span class="sxs-lookup"><span data-stu-id="19acf-110">**nVirtKey**</span></span>
</dt> <dd>

<span data-ttu-id="19acf-111">Codice di chiave virtuale per la chiave di break.</span><span class="sxs-lookup"><span data-stu-id="19acf-111">Virtual-key code for break key.</span></span>

</dd> <dt>

<span data-ttu-id="19acf-112">**hwndBreak**</span><span class="sxs-lookup"><span data-stu-id="19acf-112">**hwndBreak**</span></span>
</dt> <dd>

<span data-ttu-id="19acf-113">Handle per la finestra che deve essere la finestra corrente per il rilevamento delle interruzioni.</span><span class="sxs-lookup"><span data-stu-id="19acf-113">Handle to the window that must be the current window for break detection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19acf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="19acf-114">Remarks</span></span>

<span data-ttu-id="19acf-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="19acf-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span> <span data-ttu-id="19acf-116">Vengono definiti i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="19acf-116">The following flags are defined:</span></span>

<span data-ttu-id="19acf-117">\_HWND Interrompi MCI \_</span><span class="sxs-lookup"><span data-stu-id="19acf-117">MCI\_BREAK\_HWND</span></span>

<span data-ttu-id="19acf-118">Convalida il membro **hwndBreak** specificando la finestra che deve avere lo stato attivo per abilitare il rilevamento delle interruzioni.</span><span class="sxs-lookup"><span data-stu-id="19acf-118">Validates the **hwndBreak** member specifying the window that must have focus to enable break detection.</span></span>

<span data-ttu-id="19acf-119">\_chiave di pausa MCI \_</span><span class="sxs-lookup"><span data-stu-id="19acf-119">MCI\_BREAK\_KEY</span></span>

<span data-ttu-id="19acf-120">Convalida il membro **nVirtKey** specificando il codice della chiave virtuale da usare per la chiave di break.</span><span class="sxs-lookup"><span data-stu-id="19acf-120">Validates the **nVirtKey** member specifying the virtual-key code to be used for the break key.</span></span>

<span data-ttu-id="19acf-121">interruzione di MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="19acf-121">MCI\_BREAK\_OFF</span></span>

<span data-ttu-id="19acf-122">Disabilita qualsiasi chiave di break esistente.</span><span class="sxs-lookup"><span data-stu-id="19acf-122">Disables any existing break key.</span></span>

## <a name="requirements"></a><span data-ttu-id="19acf-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19acf-123">Requirements</span></span>



| <span data-ttu-id="19acf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="19acf-124">Requirement</span></span> | <span data-ttu-id="19acf-125">Valore</span><span class="sxs-lookup"><span data-stu-id="19acf-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="19acf-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19acf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="19acf-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19acf-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="19acf-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19acf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="19acf-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="19acf-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="19acf-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19acf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="19acf-131"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19acf-131"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19acf-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19acf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19acf-133">**MCI**</span><span class="sxs-lookup"><span data-stu-id="19acf-133">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="19acf-134">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="19acf-134">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="19acf-135">**\_interruzioni MCI**</span><span class="sxs-lookup"><span data-stu-id="19acf-135">**MCI\_BREAK**</span></span>](mci-break.md)
</dt> <dt>

<span data-ttu-id="19acf-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19acf-136">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

