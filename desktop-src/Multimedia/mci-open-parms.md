---
title: Struttura MCI_OPEN_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri aperta di MCI contiene informazioni per il \_ comando di apertura di MCI.
ms.assetid: d22cefeb-3d49-47cf-a946-f73c77ae43fd
keywords:
- Struttura MCI_OPEN_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 658f97a9b2677347c9818265c1f05c2115c95fdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119547"
---
# <a name="mci_open_parms-structure"></a><span data-ttu-id="bc504-104">\_ \_ Struttura parametri aperta MCI</span><span class="sxs-lookup"><span data-stu-id="bc504-104">MCI\_OPEN\_PARMS structure</span></span>

<span data-ttu-id="bc504-105">La **struttura \_ \_ parametri aperta di MCI** contiene informazioni per il comando di [**\_ apertura di MCI**](mci-open.md) .</span><span class="sxs-lookup"><span data-stu-id="bc504-105">The **MCI\_OPEN\_PARMS** structure contains information for the [**MCI\_OPEN**](mci-open.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc504-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc504-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
} MCI_OPEN_PARMS;
```



## <a name="members"></a><span data-ttu-id="bc504-107">Members</span><span class="sxs-lookup"><span data-stu-id="bc504-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc504-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="bc504-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="bc504-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="bc504-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="bc504-110">**wDeviceID**</span><span class="sxs-lookup"><span data-stu-id="bc504-110">**wDeviceID**</span></span>
</dt> <dd>

<span data-ttu-id="bc504-111">Identificatore restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc504-111">Identifier returned to application.</span></span>

</dd> <dt>

<span data-ttu-id="bc504-112">**lpstrDeviceType**</span><span class="sxs-lookup"><span data-stu-id="bc504-112">**lpstrDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="bc504-113">Nome o identificatore costante del tipo di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bc504-113">Name or constant identifier of the device type.</span></span> <span data-ttu-id="bc504-114">Il nome del dispositivo viene in genere ottenuto dal registro di sistema o dal file di SYSTEM.INI. Se questo membro è una costante, può essere uno dei valori elencati nei tipi di [dispositivo MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="bc504-114">(The name of the device is typically obtained from the registry or SYSTEM.INI file.) If this member is a constant, it can be one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc504-115">**lpstrElementName**</span><span class="sxs-lookup"><span data-stu-id="bc504-115">**lpstrElementName**</span></span>
</dt> <dd>

<span data-ttu-id="bc504-116">Elemento Device (spesso un percorso).</span><span class="sxs-lookup"><span data-stu-id="bc504-116">Device element (often a path).</span></span>

</dd> <dt>

<span data-ttu-id="bc504-117">**lpstrAlias**</span><span class="sxs-lookup"><span data-stu-id="bc504-117">**lpstrAlias**</span></span>
</dt> <dd>

<span data-ttu-id="bc504-118">Alias del dispositivo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bc504-118">Optional device alias.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc504-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc504-119">Remarks</span></span>

<span data-ttu-id="bc504-120">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="bc504-120">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc504-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc504-121">Requirements</span></span>



| <span data-ttu-id="bc504-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc504-122">Requirement</span></span> | <span data-ttu-id="bc504-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bc504-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc504-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc504-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc504-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc504-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bc504-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc504-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc504-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc504-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bc504-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc504-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc504-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc504-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc504-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc504-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc504-131">**MCI**</span><span class="sxs-lookup"><span data-stu-id="bc504-131">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="bc504-132">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="bc504-132">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="bc504-133">**\_aperto MCI**</span><span class="sxs-lookup"><span data-stu-id="bc504-133">**MCI\_OPEN**</span></span>](mci-open.md)
</dt> <dt>

<span data-ttu-id="bc504-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc504-134">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

