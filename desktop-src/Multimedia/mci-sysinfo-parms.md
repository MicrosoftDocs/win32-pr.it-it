---
title: Struttura MCI_SYSINFO_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri di MCI sysinfo contiene informazioni per il \_ comando MCI sysinfo.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- Struttura MCI_SYSINFO_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300958"
---
# <a name="mci_sysinfo_parms-structure"></a><span data-ttu-id="9f842-104">\_ \_ Struttura parametri di MCI sysinfo</span><span class="sxs-lookup"><span data-stu-id="9f842-104">MCI\_SYSINFO\_PARMS structure</span></span>

<span data-ttu-id="9f842-105">La **struttura \_ \_ parametri di MCI sysinfo** contiene informazioni per il comando [**MCI \_ sysinfo**](mci-sysinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9f842-105">The **MCI\_SYSINFO\_PARMS** structure contains information for the [**MCI\_SYSINFO**](mci-sysinfo.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f842-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f842-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a><span data-ttu-id="9f842-107">Members</span><span class="sxs-lookup"><span data-stu-id="9f842-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f842-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="9f842-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="9f842-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="9f842-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="9f842-110">**lpstrReturn**</span><span class="sxs-lookup"><span data-stu-id="9f842-110">**lpstrReturn**</span></span>
</dt> <dd>

<span data-ttu-id="9f842-111">Puntatore a un buffer fornito dall'utente per la stringa restituita.</span><span class="sxs-lookup"><span data-stu-id="9f842-111">Pointer to a user-supplied buffer for the return string.</span></span> <span data-ttu-id="9f842-112">Viene inoltre utilizzato per restituire un valore **DWORD** quando \_ viene utilizzato il flag di quantità di MCI sysinfo \_ .</span><span class="sxs-lookup"><span data-stu-id="9f842-112">It is also used to return a **DWORD** value when the MCI\_SYSINFO\_QUANTITY flag is used.</span></span>

</dd> <dt>

<span data-ttu-id="9f842-113">**dwRetSize**</span><span class="sxs-lookup"><span data-stu-id="9f842-113">**dwRetSize**</span></span>
</dt> <dd>

<span data-ttu-id="9f842-114">Dimensione, in byte, del buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="9f842-114">Size, in bytes, of return buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9f842-115">**dwNumber**</span><span class="sxs-lookup"><span data-stu-id="9f842-115">**dwNumber**</span></span>
</dt> <dd>

<span data-ttu-id="9f842-116">Numero che indica la posizione del dispositivo nella tabella del dispositivo MCI o nell'elenco di dispositivi aperti se \_ è impostato il flag di apertura di MCI sysinfo \_ .</span><span class="sxs-lookup"><span data-stu-id="9f842-116">Number indicating the device position in the MCI device table or in the list of open devices if the MCI\_SYSINFO\_OPEN flag is set.</span></span>

</dd> <dt>

<span data-ttu-id="9f842-117">**wDeviceType**</span><span class="sxs-lookup"><span data-stu-id="9f842-117">**wDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="9f842-118">Tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9f842-118">Type of device.</span></span> <span data-ttu-id="9f842-119">Questo membro può essere uno dei valori elencati in [tipi di dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="9f842-119">This member can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f842-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f842-120">Remarks</span></span>

<span data-ttu-id="9f842-121">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="9f842-121">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f842-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f842-122">Requirements</span></span>



| <span data-ttu-id="9f842-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f842-123">Requirement</span></span> | <span data-ttu-id="9f842-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9f842-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9f842-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f842-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9f842-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f842-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9f842-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f842-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9f842-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f842-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9f842-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f842-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f842-130"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f842-130"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f842-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f842-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f842-132">**MCI**</span><span class="sxs-lookup"><span data-stu-id="9f842-132">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9f842-133">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="9f842-133">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="9f842-134">**\_sysinfo MCI**</span><span class="sxs-lookup"><span data-stu-id="9f842-134">**MCI\_SYSINFO**</span></span>](mci-sysinfo.md)
</dt> <dt>

<span data-ttu-id="9f842-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9f842-135">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

