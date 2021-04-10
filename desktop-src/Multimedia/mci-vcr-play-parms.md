---
title: Struttura MCI_VCR_PLAY_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ Play contiene i \_ parametri per il \_ comando MCI Play per i registratori di nastri video.
ms.assetid: e180c203-3113-4fdb-bcf1-ea3e45e646e2
keywords:
- Struttura MCI_VCR_PLAY_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_PLAY_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae15eedc69accc88ef7a58a6d7ad435e872de7ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964328"
---
# <a name="mci_vcr_play_parms-structure"></a><span data-ttu-id="c22b5-104">\_ \_ Struttura parametri della riproduzione MCI VCR \_</span><span class="sxs-lookup"><span data-stu-id="c22b5-104">MCI\_VCR\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="c22b5-105">La struttura **parametri di MCI \_ VCR \_ Play \_** contiene i parametri per il comando [**MCI \_ Play**](mci-play.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="c22b5-105">The **MCI\_VCR\_PLAY\_PARMS** structure contains parameters for the [**MCI\_PLAY**](mci-play.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22b5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c22b5-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_PLAY_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="c22b5-107">Members</span><span class="sxs-lookup"><span data-stu-id="c22b5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c22b5-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="c22b5-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="c22b5-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="c22b5-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="c22b5-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-111">Posizione da cui riprodurre.</span><span class="sxs-lookup"><span data-stu-id="c22b5-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="c22b5-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="c22b5-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-113">Posizione in cui eseguire la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c22b5-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="c22b5-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="c22b5-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-115">Valore di ora che influiscono sul comando [**MCI \_ Play**](mci-play.md) o [**MCI \_ cue**](mci-cue.md) .</span><span class="sxs-lookup"><span data-stu-id="c22b5-115">Time value that affects the [**MCI\_PLAY**](mci-play.md) or [**MCI\_CUE**](mci-cue.md) command.</span></span> <span data-ttu-id="c22b5-116">Per la riproduzione [**MCI \_**](mci-play-parms.md), questo è il momento in cui inizia la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c22b5-116">For [**MCI\_PLAY**](mci-play-parms.md), this is the time when playback begins.</span></span> <span data-ttu-id="c22b5-117">Per **MCI \_ cue**, questo è il momento in cui il dispositivo di cui è stato caricato il carico raggiunge la posizione specificata in **dwFrom**.</span><span class="sxs-lookup"><span data-stu-id="c22b5-117">For **MCI\_CUE**, this is the time when the cued device reaches the position given in **dwFrom**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c22b5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c22b5-118">Remarks</span></span>

<span data-ttu-id="c22b5-119">Le posizioni vengono specificate nel formato ora corrente.</span><span class="sxs-lookup"><span data-stu-id="c22b5-119">Positions are specified in the current time format.</span></span>

<span data-ttu-id="c22b5-120">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="c22b5-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="c22b5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c22b5-121">Requirements</span></span>



| <span data-ttu-id="c22b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c22b5-122">Requirement</span></span> | <span data-ttu-id="c22b5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c22b5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c22b5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c22b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c22b5-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c22b5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c22b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c22b5-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c22b5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c22b5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c22b5-129"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="c22b5-129"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c22b5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c22b5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c22b5-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="c22b5-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="c22b5-132">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="c22b5-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="c22b5-133">**\_cue MCI**</span><span class="sxs-lookup"><span data-stu-id="c22b5-133">**MCI\_CUE**</span></span>](mci-cue.md)
</dt> <dt>

[<span data-ttu-id="c22b5-134">**\_riproduzione MCI**</span><span class="sxs-lookup"><span data-stu-id="c22b5-134">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="c22b5-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c22b5-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

