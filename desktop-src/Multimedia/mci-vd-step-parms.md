---
title: Struttura MCI_VD_STEP_PARMS (Mciapi. h)
description: La \_ struttura parametri di MCI VD \_ Step \_ contiene informazioni per il \_ comando del passaggio MCI per i dispositivi videodisco.
ms.assetid: 5345468c-b195-485a-8101-4a076410f26a
keywords:
- Struttura MCI_VD_STEP_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_STEP_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b368046375f87a897d002c362624fed3ea105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517812"
---
# <a name="mci_vd_step_parms-structure"></a><span data-ttu-id="d3c62-104">\_ \_ Struttura parametri del passaggio di MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="d3c62-104">MCI\_VD\_STEP\_PARMS structure</span></span>

<span data-ttu-id="d3c62-105">La struttura **parametri di MCI \_ VD \_ Step \_** contiene informazioni per il comando del [**\_ passaggio MCI**](mci-step.md) per i dispositivi videodisco.</span><span class="sxs-lookup"><span data-stu-id="d3c62-105">The **MCI\_VD\_STEP\_PARMS** structure contains information for the [**MCI\_STEP**](mci-step.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c62-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3c62-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrames;
} MCI_VD_STEP_PARMS;
```



## <a name="members"></a><span data-ttu-id="d3c62-107">Members</span><span class="sxs-lookup"><span data-stu-id="d3c62-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3c62-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="d3c62-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="d3c62-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="d3c62-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="d3c62-110">**dwFrames**</span><span class="sxs-lookup"><span data-stu-id="d3c62-110">**dwFrames**</span></span>
</dt> <dd>

<span data-ttu-id="d3c62-111">Numero di frame da scorrere.</span><span class="sxs-lookup"><span data-stu-id="d3c62-111">Number of frames to step.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3c62-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3c62-112">Remarks</span></span>

<span data-ttu-id="d3c62-113">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="d3c62-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c62-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3c62-114">Requirements</span></span>



| <span data-ttu-id="d3c62-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3c62-115">Requirement</span></span> | <span data-ttu-id="d3c62-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d3c62-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c62-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3c62-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c62-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3c62-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d3c62-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3c62-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c62-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d3c62-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d3c62-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3c62-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c62-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3c62-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c62-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3c62-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c62-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="d3c62-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d3c62-125">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="d3c62-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="d3c62-126">**\_passaggio MCI**</span><span class="sxs-lookup"><span data-stu-id="d3c62-126">**MCI\_STEP**</span></span>](mci-step.md)
</dt> <dt>

<span data-ttu-id="d3c62-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3c62-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

