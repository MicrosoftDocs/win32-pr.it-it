---
title: Struttura MCI_VCR_SETVIDEO_PARMS (VCR. h)
description: La \_ \_ struttura parametri MCI VCR sevideo \_ contiene i parametri per il \_ comando MCI sevideo per i registratori di nastri video.
ms.assetid: d14b2c9f-6068-4902-8db6-fc081bcd01c0
keywords:
- Struttura MCI_VCR_SETVIDEO_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETVIDEO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050e6452b3952a9d15515de01c2ca94a87af2f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874389"
---
# <a name="mci_vcr_setvideo_parms-structure"></a><span data-ttu-id="8e15b-104">\_ \_ Struttura parametri VCR VCR video \_</span><span class="sxs-lookup"><span data-stu-id="8e15b-104">MCI\_VCR\_SETVIDEO\_PARMS structure</span></span>

<span data-ttu-id="8e15b-105">La **struttura \_ parametri MCI VCR \_ sevideo \_** contiene i parametri per il comando [**MCI \_ sevideo**](mci-setvideo.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="8e15b-105">The **MCI\_VCR\_SETVIDEO\_PARMS** structure contains parameters for the [**MCI\_SETVIDEO**](mci-setvideo.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e15b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e15b-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETVIDEO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETVIDEO_PARMS;
```



## <a name="members"></a><span data-ttu-id="8e15b-107">Members</span><span class="sxs-lookup"><span data-stu-id="8e15b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8e15b-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="8e15b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="8e15b-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="8e15b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="8e15b-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="8e15b-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="8e15b-111">Rilevamento interessato.</span><span class="sxs-lookup"><span data-stu-id="8e15b-111">Affected track.</span></span>

</dd> <dt>

<span data-ttu-id="8e15b-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="8e15b-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="8e15b-113">Tipo di input o di input monitorato.</span><span class="sxs-lookup"><span data-stu-id="8e15b-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="8e15b-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="8e15b-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="8e15b-115">Input video, del tipo specificato nel membro **dwTo** , da usare.</span><span class="sxs-lookup"><span data-stu-id="8e15b-115">Video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e15b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e15b-116">Remarks</span></span>

<span data-ttu-id="8e15b-117">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="8e15b-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e15b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e15b-118">Requirements</span></span>



| <span data-ttu-id="8e15b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e15b-119">Requirement</span></span> | <span data-ttu-id="8e15b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8e15b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8e15b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e15b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8e15b-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8e15b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8e15b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e15b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8e15b-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8e15b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8e15b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e15b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e15b-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e15b-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e15b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e15b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e15b-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="8e15b-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8e15b-129">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="8e15b-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="8e15b-130">**VIDEO su MCI \_**</span><span class="sxs-lookup"><span data-stu-id="8e15b-130">**MCI\_SETVIDEO**</span></span>](mci-setvideo.md)
</dt> <dt>

<span data-ttu-id="8e15b-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8e15b-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

