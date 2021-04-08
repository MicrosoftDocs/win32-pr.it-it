---
title: Struttura MCI_VCR_CUE_PARMS (VCR. h)
description: La \_ struttura di cue parametri di MCI VCR \_ \_ contiene i parametri per il \_ comando di cue MCI per i registratori di nastri video.
ms.assetid: b2ac0c43-93ea-41c9-b886-542bda57b59e
keywords:
- Struttura MCI_VCR_CUE_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_CUE_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eeae20495281640718f95066476f0f3ac89dc6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874457"
---
# <a name="mci_vcr_cue_parms-structure"></a><span data-ttu-id="f4fae-104">\_ \_ Struttura parametri cue VCR di MCI \_</span><span class="sxs-lookup"><span data-stu-id="f4fae-104">MCI\_VCR\_CUE\_PARMS structure</span></span>

<span data-ttu-id="f4fae-105">La struttura di **\_ \_ cue \_ parametri di MCI VCR** contiene i parametri per il comando di [**\_ cue MCI**](mci-cue.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="f4fae-105">The **MCI\_VCR\_CUE\_PARMS** structure contains parameters for the [**MCI\_CUE**](mci-cue.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fae-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4fae-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_CUE_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_VCR_CUE_PARMS;
```



## <a name="members"></a><span data-ttu-id="f4fae-107">Members</span><span class="sxs-lookup"><span data-stu-id="f4fae-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4fae-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="f4fae-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="f4fae-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="f4fae-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="f4fae-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="f4fae-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="f4fae-111">Posizione da cui eseguire il cue.</span><span class="sxs-lookup"><span data-stu-id="f4fae-111">Position to cue from.</span></span>

</dd> <dt>

<span data-ttu-id="f4fae-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="f4fae-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="f4fae-113">Posizione in cui inserire il segnale.</span><span class="sxs-lookup"><span data-stu-id="f4fae-113">Position to cue to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4fae-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4fae-114">Remarks</span></span>

<span data-ttu-id="f4fae-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="f4fae-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4fae-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4fae-116">Requirements</span></span>



| <span data-ttu-id="f4fae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4fae-117">Requirement</span></span> | <span data-ttu-id="f4fae-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f4fae-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f4fae-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4fae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4fae-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4fae-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f4fae-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4fae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4fae-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4fae-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4fae-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4fae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4fae-124"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4fae-124"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4fae-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4fae-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fae-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="f4fae-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f4fae-127">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="f4fae-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="f4fae-128">**\_cue MCI**</span><span class="sxs-lookup"><span data-stu-id="f4fae-128">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

<span data-ttu-id="f4fae-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f4fae-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

