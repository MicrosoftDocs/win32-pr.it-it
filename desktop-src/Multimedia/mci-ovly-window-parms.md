---
title: Struttura MCI_OVLY_WINDOW_PARMS (Mciapi. h)
description: La \_ struttura parametri della finestra OVLY di MCI \_ \_ contiene informazioni sulla visualizzazione della finestra per il \_ comando della finestra MCI per i dispositivi con sovrimpressione video.
ms.assetid: 1189f31e-6e54-4279-a23d-b4e21c6cd276
keywords:
- Struttura MCI_OVLY_WINDOW_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OVLY_WINDOW_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a554c9ed4e4869eab333b93736a0400ef93053cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963742"
---
# <a name="mci_ovly_window_parms-structure"></a><span data-ttu-id="bd59b-104">\_ \_ Struttura parametri della finestra OVLY MCI \_</span><span class="sxs-lookup"><span data-stu-id="bd59b-104">MCI\_OVLY\_WINDOW\_PARMS structure</span></span>

<span data-ttu-id="bd59b-105">La **struttura \_ \_ \_ parametri della finestra OVLY di MCI** contiene informazioni sulla visualizzazione della finestra per il comando della [**\_ finestra MCI**](mci-window.md) per i dispositivi con sovrimpressione video.</span><span class="sxs-lookup"><span data-stu-id="bd59b-105">The **MCI\_OVLY\_WINDOW\_PARMS** structure contains window-display information for the [**MCI\_WINDOW**](mci-window.md) command for video-overlay devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd59b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd59b-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  HWND      hWnd;
  UINT      nCmdShow;
  LPCTSTR   lpstrText;
} MCI_OVLY_WINDOW_PARMS;
```



## <a name="members"></a><span data-ttu-id="bd59b-107">Members</span><span class="sxs-lookup"><span data-stu-id="bd59b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bd59b-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="bd59b-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="bd59b-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="bd59b-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="bd59b-110">**hWnd**</span><span class="sxs-lookup"><span data-stu-id="bd59b-110">**hWnd**</span></span>
</dt> <dd>

<span data-ttu-id="bd59b-111">Handle per la finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bd59b-111">Handle to display window.</span></span>

</dd> <dt>

<span data-ttu-id="bd59b-112">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="bd59b-112">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="bd59b-113">Comando di visualizzazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="bd59b-113">Window-display command.</span></span>

</dd> <dt>

<span data-ttu-id="bd59b-114">**lpstrText**</span><span class="sxs-lookup"><span data-stu-id="bd59b-114">**lpstrText**</span></span>
</dt> <dd>

<span data-ttu-id="bd59b-115">Didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="bd59b-115">Window caption.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd59b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd59b-116">Remarks</span></span>

<span data-ttu-id="bd59b-117">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="bd59b-117">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd59b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd59b-118">Requirements</span></span>



| <span data-ttu-id="bd59b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd59b-119">Requirement</span></span> | <span data-ttu-id="bd59b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bd59b-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bd59b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd59b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd59b-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd59b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bd59b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd59b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd59b-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bd59b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bd59b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd59b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd59b-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd59b-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd59b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd59b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd59b-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="bd59b-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bd59b-129">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="bd59b-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="bd59b-130">**\_finestra MCI**</span><span class="sxs-lookup"><span data-stu-id="bd59b-130">**MCI\_WINDOW**</span></span>](mci-window.md)
</dt> <dt>

<span data-ttu-id="bd59b-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bd59b-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

