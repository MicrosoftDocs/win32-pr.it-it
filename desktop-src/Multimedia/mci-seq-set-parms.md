---
title: Struttura MCI_SEQ_SET_PARMS (Mciapi. h)
description: La \_ struttura MCI seq \_ set \_ parametri contiene informazioni per il \_ comando set di MCI per i dispositivi MIDI Sequencer.
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- Struttura MCI_SEQ_SET_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963876"
---
# <a name="mci_seq_set_parms-structure"></a><span data-ttu-id="df330-104">\_ \_ Struttura parametri della serie MCI seq \_</span><span class="sxs-lookup"><span data-stu-id="df330-104">MCI\_SEQ\_SET\_PARMS structure</span></span>

<span data-ttu-id="df330-105">La struttura **MCI \_ seq \_ set \_ parametri** contiene informazioni per il comando [**\_ set di MCI**](mci-set.md) per i dispositivi MIDI Sequencer.</span><span class="sxs-lookup"><span data-stu-id="df330-105">The **MCI\_SEQ\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command for MIDI sequencer devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="df330-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df330-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="df330-107">Members</span><span class="sxs-lookup"><span data-stu-id="df330-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="df330-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="df330-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="df330-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="df330-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="df330-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="df330-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="df330-111">Formato dell'ora di Sequencer.</span><span class="sxs-lookup"><span data-stu-id="df330-111">Sequencer's time format.</span></span>

</dd> <dt>

<span data-ttu-id="df330-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="df330-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="df330-113">Canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="df330-113">Audio output channel.</span></span>

</dd> <dt>

<span data-ttu-id="df330-114">**dwTempo**</span><span class="sxs-lookup"><span data-stu-id="df330-114">**dwTempo**</span></span>
</dt> <dd>

<span data-ttu-id="df330-115">Tempo.</span><span class="sxs-lookup"><span data-stu-id="df330-115">Tempo.</span></span>

</dd> <dt>

<span data-ttu-id="df330-116">**dwPort**</span><span class="sxs-lookup"><span data-stu-id="df330-116">**dwPort**</span></span>
</dt> <dd>

<span data-ttu-id="df330-117">Porta.</span><span class="sxs-lookup"><span data-stu-id="df330-117">Port.</span></span>

</dd> <dt>

<span data-ttu-id="df330-118">**dwSlave**</span><span class="sxs-lookup"><span data-stu-id="df330-118">**dwSlave**</span></span>
</dt> <dd>

<span data-ttu-id="df330-119">Tipo di sincronizzazione utilizzato dal sequencer per l'operazione subordinata.</span><span class="sxs-lookup"><span data-stu-id="df330-119">Type of synchronization used by the sequencer for subordinate operation.</span></span>

</dd> <dt>

<span data-ttu-id="df330-120">**dwMaster**</span><span class="sxs-lookup"><span data-stu-id="df330-120">**dwMaster**</span></span>
</dt> <dd>

<span data-ttu-id="df330-121">Tipo di sincronizzazione utilizzato dal sequencer per l'operazione master.</span><span class="sxs-lookup"><span data-stu-id="df330-121">Type of synchronization used by the sequencer for master operation.</span></span>

</dd> <dt>

<span data-ttu-id="df330-122">**dwOffset**</span><span class="sxs-lookup"><span data-stu-id="df330-122">**dwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="df330-123">Offset dei dati.</span><span class="sxs-lookup"><span data-stu-id="df330-123">Data offset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df330-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="df330-124">Remarks</span></span>

<span data-ttu-id="df330-125">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="df330-125">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="df330-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df330-126">Requirements</span></span>



| <span data-ttu-id="df330-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="df330-127">Requirement</span></span> | <span data-ttu-id="df330-128">Valore</span><span class="sxs-lookup"><span data-stu-id="df330-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="df330-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df330-129">Minimum supported client</span></span><br/> | <span data-ttu-id="df330-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df330-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="df330-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df330-131">Minimum supported server</span></span><br/> | <span data-ttu-id="df330-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df330-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="df330-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df330-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="df330-134"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="df330-134"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df330-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df330-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df330-136">**MCI**</span><span class="sxs-lookup"><span data-stu-id="df330-136">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="df330-137">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="df330-137">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="df330-138">**SET di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="df330-138">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="df330-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df330-139">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

