---
title: Struttura MCI_PLAY_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri di MCI Play contiene informazioni sul posizionamento del \_ comando MCI Play.
ms.assetid: f1bacf61-ec14-4391-b227-20b35c0bbbc3
keywords:
- Struttura MCI_PLAY_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f207737d4eb93e280355d0e5041b6e7bfc1b3048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963741"
---
# <a name="mci_play_parms-structure"></a><span data-ttu-id="a52e6-104">\_Struttura parametri della riproduzione MCI \_</span><span class="sxs-lookup"><span data-stu-id="a52e6-104">MCI\_PLAY\_PARMS structure</span></span>

<span data-ttu-id="a52e6-105">La **struttura \_ \_ parametri di MCI Play** contiene informazioni sul posizionamento del comando [**MCI \_ Play**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="a52e6-105">The **MCI\_PLAY\_PARMS** structure contains positioning information for the [**MCI\_PLAY**](mci-play.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a52e6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a52e6-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_PLAY_PARMS;
```



## <a name="members"></a><span data-ttu-id="a52e6-107">Members</span><span class="sxs-lookup"><span data-stu-id="a52e6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a52e6-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="a52e6-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a52e6-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="a52e6-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a52e6-110">**dwFrom**</span><span class="sxs-lookup"><span data-stu-id="a52e6-110">**dwFrom**</span></span>
</dt> <dd>

<span data-ttu-id="a52e6-111">Posizione da cui riprodurre.</span><span class="sxs-lookup"><span data-stu-id="a52e6-111">Position to play from.</span></span>

</dd> <dt>

<span data-ttu-id="a52e6-112">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="a52e6-112">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="a52e6-113">Posizione in cui eseguire la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a52e6-113">Position to play to.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a52e6-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a52e6-114">Remarks</span></span>

<span data-ttu-id="a52e6-115">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="a52e6-115">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="a52e6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a52e6-116">Requirements</span></span>



| <span data-ttu-id="a52e6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a52e6-117">Requirement</span></span> | <span data-ttu-id="a52e6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a52e6-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a52e6-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a52e6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a52e6-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a52e6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a52e6-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a52e6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a52e6-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a52e6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a52e6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a52e6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a52e6-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a52e6-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a52e6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a52e6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52e6-126">**MCI**</span><span class="sxs-lookup"><span data-stu-id="a52e6-126">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a52e6-127">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="a52e6-127">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a52e6-128">**\_riproduzione MCI**</span><span class="sxs-lookup"><span data-stu-id="a52e6-128">**MCI\_PLAY**</span></span>](mci-play.md)
</dt> <dt>

<span data-ttu-id="a52e6-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a52e6-129">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

