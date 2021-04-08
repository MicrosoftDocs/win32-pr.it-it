---
title: Struttura MCI_SET_PARMS (Mciapi. h)
description: La \_ struttura set \_ parametri di MCI contiene informazioni per il \_ comando set di MCI.
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- Struttura MCI_SET_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971affd319ecae817b9c1159ab0f307d0c2a5c91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048052"
---
# <a name="mci_set_parms-structure"></a><span data-ttu-id="f8d09-104">\_ \_ Struttura parametri set MCI</span><span class="sxs-lookup"><span data-stu-id="f8d09-104">MCI\_SET\_PARMS structure</span></span>

<span data-ttu-id="f8d09-105">La **struttura \_ set \_ parametri di MCI** contiene informazioni per il comando [**\_ set di MCI**](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="f8d09-105">The **MCI\_SET\_PARMS** structure contains information for the [**MCI\_SET**](mci-set.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d09-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8d09-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a><span data-ttu-id="f8d09-107">Members</span><span class="sxs-lookup"><span data-stu-id="f8d09-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8d09-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="f8d09-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="f8d09-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="f8d09-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="f8d09-110">**dwTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f8d09-110">**dwTimeFormat**</span></span>
</dt> <dd>

<span data-ttu-id="f8d09-111">Formato ora per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8d09-111">Time format for device.</span></span>

</dd> <dt>

<span data-ttu-id="f8d09-112">**dwAudio**</span><span class="sxs-lookup"><span data-stu-id="f8d09-112">**dwAudio**</span></span>
</dt> <dd>

<span data-ttu-id="f8d09-113">Canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="f8d09-113">Audio output channel.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8d09-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8d09-114">Remarks</span></span>

<span data-ttu-id="f8d09-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="f8d09-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8d09-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8d09-116">Requirements</span></span>



| <span data-ttu-id="f8d09-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8d09-117">Requirement</span></span> | <span data-ttu-id="f8d09-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f8d09-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f8d09-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8d09-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f8d09-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8d09-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f8d09-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8d09-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f8d09-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f8d09-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f8d09-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8d09-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8d09-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8d09-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8d09-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8d09-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8d09-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="f8d09-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="f8d09-127">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="f8d09-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="f8d09-128">**SET di MCI \_**</span><span class="sxs-lookup"><span data-stu-id="f8d09-128">**MCI\_SET**</span></span>](mci-set.md)
</dt> <dt>

<span data-ttu-id="f8d09-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8d09-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

