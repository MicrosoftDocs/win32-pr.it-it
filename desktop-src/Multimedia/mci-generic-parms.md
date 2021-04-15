---
title: Struttura MCI_GENERIC_PARMS (Mciapi. h)
description: La \_ struttura parametri generica MCI \_ contiene l'handle della finestra che riceve i messaggi di notifica. Questa struttura viene utilizzata per i messaggi di comando MCI con elenchi di parametri vuoti.
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- Struttura MCI_GENERIC_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476229"
---
# <a name="mci_generic_parms-structure"></a><span data-ttu-id="babcc-105">\_Struttura parametri generica MCI \_</span><span class="sxs-lookup"><span data-stu-id="babcc-105">MCI\_GENERIC\_PARMS structure</span></span>

<span data-ttu-id="babcc-106">La **struttura \_ \_ parametri generica MCI** contiene l'handle della finestra che riceve i messaggi di notifica.</span><span class="sxs-lookup"><span data-stu-id="babcc-106">The **MCI\_GENERIC\_PARMS** structure contains the handle of the window that receives notification messages.</span></span> <span data-ttu-id="babcc-107">Questa struttura viene utilizzata per i messaggi di comando MCI con elenchi di parametri vuoti.</span><span class="sxs-lookup"><span data-stu-id="babcc-107">This structure is used for MCI command messages that have empty parameter lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="babcc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="babcc-108">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a><span data-ttu-id="babcc-109">Members</span><span class="sxs-lookup"><span data-stu-id="babcc-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="babcc-110">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="babcc-110">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="babcc-111">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="babcc-111">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="babcc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="babcc-112">Remarks</span></span>

<span data-ttu-id="babcc-113">Le **strutture \_ \_ parametri** di MCI Close e **MCI \_ realizzano \_ parametri** sono identiche alla struttura **\_ \_ parametri generica MCI** .</span><span class="sxs-lookup"><span data-stu-id="babcc-113">The **MCI\_CLOSE\_PARMS** and **MCI\_REALIZE\_PARMS** structures are identical to the **MCI\_GENERIC\_PARMS** structure.</span></span>

<span data-ttu-id="babcc-114">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="babcc-114">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="babcc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="babcc-115">Requirements</span></span>



| <span data-ttu-id="babcc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="babcc-116">Requirement</span></span> | <span data-ttu-id="babcc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="babcc-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="babcc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="babcc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="babcc-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="babcc-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="babcc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="babcc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="babcc-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="babcc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="babcc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="babcc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="babcc-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="babcc-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="babcc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="babcc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="babcc-125">**MCI**</span><span class="sxs-lookup"><span data-stu-id="babcc-125">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="babcc-126">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="babcc-126">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

<span data-ttu-id="babcc-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="babcc-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

