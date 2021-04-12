---
title: Struttura MCI_VD_PLAY_PARMS (Mciapi. h)
description: La \_ struttura MCI VD \_ Play \_ parametri contiene informazioni sulla posizione e sulla velocità del \_ comando MCI Play per i dispositivi videodisco.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- Struttura MCI_VD_PLAY_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ab04ba5cf0a2b507370a4b777c19fd60a05c30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048406"
---
# <a name="mci_vd_play_parms-structure"></a><span data-ttu-id="5ec74-104">\_Struttura parametri di MCI VD \_ Play \_</span><span class="sxs-lookup"><span data-stu-id="5ec74-104">MCI\_VD\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="5ec74-105">La struttura **MCI \_ VD \_ Play \_ parametri** contiene informazioni sulla posizione e sulla velocità del comando [**MCI \_ Play**](mci-play.md) per i dispositivi videodisco.</span><span class="sxs-lookup"><span data-stu-id="5ec74-105">The **MCI\_VD\_PLAY\_PARMS** structure contains position and speed information for the [**MCI\_PLAY**](mci-play.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ec74-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ec74-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="5ec74-107">Members</span><span class="sxs-lookup"><span data-stu-id="5ec74-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ec74-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="5ec74-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="5ec74-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="5ec74-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="5ec74-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="5ec74-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="5ec74-111">Posizione da cui riprodurre.</span><span class="sxs-lookup"><span data-stu-id="5ec74-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="5ec74-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="5ec74-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="5ec74-113">Posizione in cui eseguire la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="5ec74-113">Position to play to.</span></span>

</dd> <dt>

<span data-ttu-id="5ec74-114">**dwSpeed**</span><span class="sxs-lookup"><span data-stu-id="5ec74-114">**dwSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="5ec74-115">Velocità di riproduzione in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="5ec74-115">Playback speed in frames per second.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ec74-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ec74-116">Remarks</span></span>

<span data-ttu-id="5ec74-117">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="5ec74-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

<span data-ttu-id="5ec74-118">È possibile usare la struttura [**MCI \_ Play \_ parametri**](mci-play-parms.md) anziché **MCI \_ VD \_ Play \_ parametri** se non si usano i membri dati estesi.</span><span class="sxs-lookup"><span data-stu-id="5ec74-118">You can use the [**MCI\_PLAY\_PARMS**](mci-play-parms.md) structure instead of **MCI\_VD\_PLAY\_PARMS** if you are not using the extended data members.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ec74-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ec74-119">Requirements</span></span>



| <span data-ttu-id="5ec74-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ec74-120">Requirement</span></span> | <span data-ttu-id="5ec74-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5ec74-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec74-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ec74-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5ec74-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5ec74-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5ec74-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ec74-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5ec74-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5ec74-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5ec74-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ec74-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ec74-127"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ec74-127"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ec74-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ec74-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ec74-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="5ec74-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="5ec74-130">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="5ec74-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="5ec74-131">**\_riproduzione MCI**</span><span class="sxs-lookup"><span data-stu-id="5ec74-131">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

[<span data-ttu-id="5ec74-132">**parametri di MCI \_ Play \_**</span><span class="sxs-lookup"><span data-stu-id="5ec74-132">**MCI\_PLAY\_PARMS**</span></span>](mci-play-parms.md)
</dt> <dt>

<span data-ttu-id="5ec74-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5ec74-133">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

