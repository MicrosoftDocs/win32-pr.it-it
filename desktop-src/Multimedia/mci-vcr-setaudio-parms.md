---
title: Struttura MCI_VCR_SETAUDIO_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ contiene i \_ parametri per il \_ comando MCI sefonica per i registratori di nastri video.
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- Struttura MCI_VCR_SETAUDIO_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 143345f494f381054335d2dfec3b0c10222adca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873429"
---
# <a name="mci_vcr_setaudio_parms-structure"></a><span data-ttu-id="fe504-104">\_ \_ Struttura parametri del videoregistratore \_ MCI</span><span class="sxs-lookup"><span data-stu-id="fe504-104">MCI\_VCR\_SETAUDIO\_PARMS structure</span></span>

<span data-ttu-id="fe504-105">La **struttura \_ \_ \_ parametri di MCI VCR** contiene i parametri per il comando [**MCI \_ sefonica**](mci-setaudio.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="fe504-105">The **MCI\_VCR\_SETAUDIO\_PARMS** structure contains parameters for the [**MCI\_SETAUDIO**](mci-setaudio.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe504-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe504-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a><span data-ttu-id="fe504-107">Members</span><span class="sxs-lookup"><span data-stu-id="fe504-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe504-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="fe504-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="fe504-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="fe504-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="fe504-110">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="fe504-110">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="fe504-111">Traccia audio.</span><span class="sxs-lookup"><span data-stu-id="fe504-111">Audio track.</span></span>

</dd> <dt>

<span data-ttu-id="fe504-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="fe504-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="fe504-113">Tipo di input o di input monitorato.</span><span class="sxs-lookup"><span data-stu-id="fe504-113">Type of input or monitored input.</span></span>

</dd> <dt>

<span data-ttu-id="fe504-114">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="fe504-114">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="fe504-115">Input audio (del tipo specificato nel membro **dwTo** ) da usare.</span><span class="sxs-lookup"><span data-stu-id="fe504-115">Audio input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe504-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe504-116">Remarks</span></span>

<span data-ttu-id="fe504-117">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="fe504-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe504-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe504-118">Requirements</span></span>



| <span data-ttu-id="fe504-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe504-119">Requirement</span></span> | <span data-ttu-id="fe504-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fe504-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fe504-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe504-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fe504-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe504-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fe504-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe504-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fe504-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe504-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fe504-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe504-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe504-126"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe504-126"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe504-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe504-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe504-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="fe504-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fe504-129">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="fe504-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="fe504-130">**sefonica MCI \_**</span><span class="sxs-lookup"><span data-stu-id="fe504-130">**MCI\_SETAUDIO**</span></span>](mci-setaudio.md)
</dt> <dt>

<span data-ttu-id="fe504-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe504-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

