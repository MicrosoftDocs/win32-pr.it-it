---
title: Struttura MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: La \_ struttura OVLY \_ Load \_ parametri di MCI contiene informazioni per il \_ comando di caricamento MCI per i dispositivi con sovrimpressione video.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- Struttura MCI_OVLY_LOAD_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047834"
---
# <a name="mci_ovly_load_parms-structure"></a><span data-ttu-id="17e4a-104">\_Struttura OVLY \_ Load \_ parametri di MCI</span><span class="sxs-lookup"><span data-stu-id="17e4a-104">MCI\_OVLY\_LOAD\_PARMS structure</span></span>

<span data-ttu-id="17e4a-105">La **struttura \_ OVLY \_ Load \_ parametri di MCI** contiene informazioni per il comando di [**\_ caricamento MCI**](mci-load.md) per i dispositivi con sovrimpressione video.</span><span class="sxs-lookup"><span data-stu-id="17e4a-105">The **MCI\_OVLY\_LOAD\_PARMS** structure contains information for the [**MCI\_LOAD**](mci-load.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e4a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17e4a-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a><span data-ttu-id="17e4a-107">Members</span><span class="sxs-lookup"><span data-stu-id="17e4a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="17e4a-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="17e4a-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="17e4a-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="17e4a-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="17e4a-110">**lpfilename**</span><span class="sxs-lookup"><span data-stu-id="17e4a-110">**lpfilename**</span></span>
</dt> <dd>

<span data-ttu-id="17e4a-111">Nome del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="17e4a-111">Name of file to load.</span></span>

</dd> <dt>

<span data-ttu-id="17e4a-112">**RC**</span><span class="sxs-lookup"><span data-stu-id="17e4a-112">**rc**</span></span>
</dt> <dd>

<span data-ttu-id="17e4a-113">Identifica l'area del buffer video da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="17e4a-113">Identifies the area of the video buffer to update.</span></span> <span data-ttu-id="17e4a-114">Le strutture [Rect](/previous-versions//ms536136(v=vs.85)) sono gestite in modo diverso in MCI rispetto ad altre parti di Windows; in MCI, **RC. Right** contiene la larghezza del rettangolo e la versione **RC. Bottom** contiene l'altezza.</span><span class="sxs-lookup"><span data-stu-id="17e4a-114">[RECT](/previous-versions//ms536136(v=vs.85)) structures are handled differently in MCI than in other parts of Windows; in MCI, **rc.right** contains the width of the rectangle and **rc.bottom** contains its height.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17e4a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="17e4a-115">Remarks</span></span>

<span data-ttu-id="17e4a-116">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="17e4a-116">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e4a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17e4a-117">Requirements</span></span>



| <span data-ttu-id="17e4a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e4a-118">Requirement</span></span> | <span data-ttu-id="17e4a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="17e4a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17e4a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17e4a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17e4a-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17e4a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="17e4a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17e4a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17e4a-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17e4a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17e4a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17e4a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17e4a-125"><dt>Mmsystem. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e4a-125"><dt>Mmsystem.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e4a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17e4a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e4a-127">**MCI**</span><span class="sxs-lookup"><span data-stu-id="17e4a-127">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="17e4a-128">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="17e4a-128">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="17e4a-129">**\_carico MCI**</span><span class="sxs-lookup"><span data-stu-id="17e4a-129">**MCI\_LOAD**</span></span>](mci-load.md)
</dt> <dt>

<span data-ttu-id="17e4a-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17e4a-130">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="17e4a-131">[RECT](/previous-versions//ms536136(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17e4a-131">[RECT](/previous-versions//ms536136(v=vs.85))</span></span>
</dt> </dl>

 

