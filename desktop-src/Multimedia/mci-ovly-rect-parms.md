---
title: Struttura MCI_OVLY_RECT_PARMS (Mciapi. h)
description: La \_ struttura OVLY \_ Rect \_ parametri di MCI contiene informazioni sul posizionamento per i \_ comandi put MCI e MCI \_ Where per i dispositivi con sovrimpressione video.
ms.assetid: 1cfd8e51-c76f-4a1c-905c-efacbd8146f4
keywords:
- Struttura MCI_OVLY_RECT_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_RECT_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68a6b51d980b6ca0a3c223f414571a42b2e3ae3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475094"
---
# <a name="mci_ovly_rect_parms-structure"></a><span data-ttu-id="0fd8c-104">\_ \_ Struttura parametri OVLY Rect di MCI \_</span><span class="sxs-lookup"><span data-stu-id="0fd8c-104">MCI\_OVLY\_RECT\_PARMS structure</span></span>

<span data-ttu-id="0fd8c-105">La **struttura \_ OVLY \_ Rect \_ parametri di MCI** contiene informazioni sul posizionamento per i comandi [**\_ put MCI**](mci-put.md) e [**MCI \_ where**](mci-where.md) per i dispositivi con sovrimpressione video.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-105">The **MCI\_OVLY\_RECT\_PARMS** structure contains positioning information for the [**MCI\_PUT**](mci-put.md) and [**MCI\_WHERE**](mci-where.md) commands for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd8c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fd8c-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  RECT      rc;
} MCI_OVLY_RECT_PARMS;
```



## <a name="members"></a><span data-ttu-id="0fd8c-107">Members</span><span class="sxs-lookup"><span data-stu-id="0fd8c-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0fd8c-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="0fd8c-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="0fd8c-110">**RC**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-110">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="0fd8c-111">Rettangolo contenente le informazioni sul posizionamento.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-111">Rectangle containing positioning information.</span></span> <span data-ttu-id="0fd8c-112">Le strutture [Rect](/previous-versions//ms536136(v=vs.85)) sono gestite in modo diverso in MCI rispetto ad altre parti di Windows; in MCI, **RC. Right** contiene la larghezza del rettangolo e la versione **RC. Bottom** contiene l'altezza.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-112">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fd8c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fd8c-113">Remarks</span></span>

<span data-ttu-id="0fd8c-114">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="0fd8c-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd8c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fd8c-115">Requirements</span></span>



| <span data-ttu-id="0fd8c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd8c-116">Requirement</span></span> | <span data-ttu-id="0fd8c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0fd8c-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd8c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fd8c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd8c-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0fd8c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0fd8c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fd8c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd8c-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0fd8c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0fd8c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fd8c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd8c-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd8c-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd8c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fd8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd8c-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0fd8c-126">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="0fd8c-127">**\_put MCI**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-127">**MCI\_PUT**</span></span>](mci-put.md)
</dt> <dt>

[<span data-ttu-id="0fd8c-128">**MCI \_ dove**</span><span class="sxs-lookup"><span data-stu-id="0fd8c-128">**MCI\_WHERE**</span></span>](mci-where.md)
</dt> <dt>

<span data-ttu-id="0fd8c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fd8c-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0fd8c-130">[RECT](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0fd8c-130">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

