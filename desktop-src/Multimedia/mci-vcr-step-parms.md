---
title: Struttura MCI_VCR_STEP_PARMS (VCR. h)
description: La \_ struttura parametri del passaggio del VCR MCI \_ \_ contiene i parametri per il \_ comando del passaggio MCI per i registratori di nastri video.
ms.assetid: 57751de6-d174-418f-8167-402d3ead4e24
keywords:
- Struttura MCI_VCR_STEP_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STEP_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a616b31500a2c814edb3dd443586131ed0ffae7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047975"
---
# <a name="mci_vcr_step_parms-structure"></a><span data-ttu-id="4d243-104">\_ \_ Struttura parametri del passaggio VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="4d243-104">MCI\_VCR\_STEP\_PARMS structure</span></span>

<span data-ttu-id="4d243-105">La **struttura \_ \_ \_ parametri del passaggio del VCR MCI** contiene i parametri per il comando del [**\_ passaggio MCI**](mci-step.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="4d243-105">The **MCI\_VCR\_STEP\_PARMS** structure contains parameters for the [**MCI\_STEP**](mci-step.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d243-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d243-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_STEP_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VCR_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="4d243-107">Members</span><span class="sxs-lookup"><span data-stu-id="4d243-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4d243-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="4d243-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4d243-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="4d243-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="4d243-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="4d243-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="4d243-111">Il numero di fotogrammi da saltare (la lunghezza di un singolo passaggio) [**come \_ passaggio**](mci-step.md) del comando MCI, avanti o indietro nel contenuto.</span><span class="sxs-lookup"><span data-stu-id="4d243-111">Number of frames to jump (the length of a single step) as the [**MCI\_STEP**](mci-step.md) command steps forward or backward through the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d243-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d243-112">Remarks</span></span>

<span data-ttu-id="4d243-113">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* di [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="4d243-113">When assigning data to the members in this structure, set the corresponding flags in the *fdwCommand* parameter of [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d243-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d243-114">Requirements</span></span>



| <span data-ttu-id="4d243-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d243-115">Requirement</span></span> | <span data-ttu-id="4d243-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4d243-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4d243-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d243-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d243-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4d243-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4d243-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d243-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d243-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4d243-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4d243-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d243-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d243-122"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d243-122"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d243-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d243-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d243-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="4d243-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4d243-125">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="4d243-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="4d243-126">**\_passaggio MCI**</span><span class="sxs-lookup"><span data-stu-id="4d243-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="4d243-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4d243-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

