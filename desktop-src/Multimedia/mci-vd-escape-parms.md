---
title: Struttura MCI_VD_ESCAPE_PARMS (Mciapi. h)
description: La \_ struttura MCI VD \_ escape \_ parametri contiene il comando inviato a un dispositivo per il comando di escape MCI per i \_ dispositivi videodisco.
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- Struttura MCI_VD_ESCAPE_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80712cd693e2c7ebe290be6b9827c1e051dd86a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301464"
---
# <a name="mci_vd_escape_parms-structure"></a><span data-ttu-id="76e92-104">\_ \_ Struttura parametri di escape MCI VD \_</span><span class="sxs-lookup"><span data-stu-id="76e92-104">MCI\_VD\_ESCAPE\_PARMS structure</span></span>

<span data-ttu-id="76e92-105">La struttura **MCI \_ VD \_ escape \_ parametri** contiene il comando inviato a un dispositivo per il comando di [**\_ escape MCI**](mci-escape.md) per i dispositivi videodisco.</span><span class="sxs-lookup"><span data-stu-id="76e92-105">The **MCI\_VD\_ESCAPE\_PARMS** structure contains the command sent to a device for the [**MCI\_ESCAPE**](mci-escape.md) command for videodisc devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="76e92-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76e92-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a><span data-ttu-id="76e92-107">Members</span><span class="sxs-lookup"><span data-stu-id="76e92-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="76e92-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="76e92-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="76e92-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="76e92-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="76e92-110">**lpstrCommand**</span><span class="sxs-lookup"><span data-stu-id="76e92-110">**lpstrCommand**</span></span>
</dt> <dd>

<span data-ttu-id="76e92-111">Comando da inviare al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76e92-111">Command to send to device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76e92-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="76e92-112">Remarks</span></span>

<span data-ttu-id="76e92-113">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="76e92-113">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="76e92-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76e92-114">Requirements</span></span>



| <span data-ttu-id="76e92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76e92-115">Requirement</span></span> | <span data-ttu-id="76e92-116">Valore</span><span class="sxs-lookup"><span data-stu-id="76e92-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="76e92-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76e92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76e92-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="76e92-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="76e92-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76e92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76e92-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="76e92-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="76e92-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76e92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="76e92-122"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="76e92-122"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76e92-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76e92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76e92-124">**MCI**</span><span class="sxs-lookup"><span data-stu-id="76e92-124">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="76e92-125">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="76e92-125">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="76e92-126">**\_escape MCI**</span><span class="sxs-lookup"><span data-stu-id="76e92-126">**MCI\_ESCAPE**</span></span>](mci-escape.md)
</dt> <dt>

<span data-ttu-id="76e92-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76e92-127">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

