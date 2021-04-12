---
title: Struttura MCI_RECORD_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri record MCI contiene informazioni sul posizionamento per il \_ comando record MCI.
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- Struttura MCI_RECORD_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633ce192d0f4b2467cb744d614ea38056eafb60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475088"
---
# <a name="mci_record_parms-structure"></a><span data-ttu-id="55bfb-104">\_ \_ Struttura parametri record MCI</span><span class="sxs-lookup"><span data-stu-id="55bfb-104">MCI\_RECORD\_PARMS structure</span></span>

<span data-ttu-id="55bfb-105">La **struttura \_ \_ parametri record MCI** contiene informazioni sul posizionamento per il comando [**\_ record MCI**](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="55bfb-105">The **MCI\_RECORD\_PARMS** structure contains positioning information for the [**MCI\_RECORD**](mci-record.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bfb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55bfb-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a><span data-ttu-id="55bfb-107">Members</span><span class="sxs-lookup"><span data-stu-id="55bfb-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="55bfb-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="55bfb-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="55bfb-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="55bfb-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="55bfb-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="55bfb-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="55bfb-111">Posizione da cui riprodurre.</span><span class="sxs-lookup"><span data-stu-id="55bfb-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="55bfb-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="55bfb-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="55bfb-113">Posizione in cui eseguire la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="55bfb-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55bfb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="55bfb-114">Remarks</span></span>

<span data-ttu-id="55bfb-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="55bfb-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bfb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55bfb-116">Requirements</span></span>



| <span data-ttu-id="55bfb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55bfb-117">Requirement</span></span> | <span data-ttu-id="55bfb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="55bfb-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55bfb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55bfb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55bfb-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55bfb-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="55bfb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55bfb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55bfb-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55bfb-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55bfb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55bfb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bfb-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="55bfb-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55bfb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55bfb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bfb-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="55bfb-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="55bfb-127">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="55bfb-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="55bfb-128">**\_record MCI**</span><span class="sxs-lookup"><span data-stu-id="55bfb-128">**MCI\_RECORD**</span></span>](mci-record.md)
</dt> <dt>

<span data-ttu-id="55bfb-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="55bfb-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

