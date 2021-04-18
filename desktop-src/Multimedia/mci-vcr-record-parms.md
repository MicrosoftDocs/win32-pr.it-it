---
title: Struttura MCI_VCR_RECORD_PARMS (VCR. h)
description: La \_ \_ struttura parametri del record MCI VCR \_ contiene i parametri per il \_ comando MCI record per i registratori di nastri video.
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- Struttura MCI_VCR_RECORD_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4089b6b7977959b5eb0d0ac60dd4e612b17b823d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301374"
---
# <a name="mci_vcr_record_parms-structure"></a><span data-ttu-id="d3052-104">\_ \_ Struttura parametri del record VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="d3052-104">MCI\_VCR\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="d3052-105">La **struttura \_ \_ \_ parametri del record MCI VCR** contiene i parametri per il comando [**MCI \_ record**](mci-record.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="d3052-105">The **MCI\_VCR\_RECORD\_PARMS** structure contains parameters for the [**MCI\_RECORD**](mci-record.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3052-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3052-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="d3052-107">Members</span><span class="sxs-lookup"><span data-stu-id="d3052-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3052-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="d3052-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d3052-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="d3052-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d3052-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="d3052-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="d3052-111">Posizione da cui riprodurre.</span><span class="sxs-lookup"><span data-stu-id="d3052-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="d3052-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="d3052-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="d3052-113">Posizione in cui eseguire la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="d3052-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="d3052-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="d3052-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="d3052-115">Valore di ora che influiscono sul comando [**MCI \_ record**](mci-record.md) o [**MCI \_ cue**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="d3052-115">Time value that affects the [**MCI\_RECORD**](mci-record.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="d3052-116">Per **il \_ record MCI**, questo è il momento in cui inizia la registrazione.</span><span class="sxs-lookup"><span data-stu-id="d3052-116">For **MCI\_RECORD**, this is the time when recording begins.</span></span> <span data-ttu-id="d3052-117">Per **MCI \_ cue**, questo è il momento in cui il dispositivo di cui è stato caricato il carico raggiunge la posizione specificata in **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="d3052-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3052-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3052-118">Remarks</span></span>

<span data-ttu-id="d3052-119">Le posizioni vengono specificate nel formato ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d3052-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="d3052-120">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="d3052-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3052-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3052-121">Requirements</span></span>



| <span data-ttu-id="d3052-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3052-122">Requirement</span></span> | <span data-ttu-id="d3052-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d3052-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d3052-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3052-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d3052-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3052-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d3052-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3052-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d3052-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3052-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3052-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3052-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3052-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3052-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3052-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3052-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3052-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d3052-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d3052-132">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="d3052-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d3052-133">**\_cue MCI**</span><span class="sxs-lookup"><span data-stu-id="d3052-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="d3052-134">**\_record MCI**</span><span class="sxs-lookup"><span data-stu-id="d3052-134">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="d3052-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3052-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

