---
title: Struttura MCI_STATUS_PARMS (Mciapi. h)
description: La \_ \_ struttura parametri status MCI contiene informazioni per il \_ comando MCI status.
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- Struttura MCI_STATUS_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8295f2e747752889c10083c6bb794ba2df7ac273
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963875"
---
# <a name="mci_status_parms-structure"></a><span data-ttu-id="a04d8-104">\_ \_ Struttura parametri stato MCI</span><span class="sxs-lookup"><span data-stu-id="a04d8-104">MCI\_STATUS\_PARMS structure</span></span>

<span data-ttu-id="a04d8-105">La **struttura \_ \_ parametri status MCI** contiene informazioni per il comando [**MCI \_ status**](mci-status.md) .</span><span class="sxs-lookup"><span data-stu-id="a04d8-105">The **MCI\_STATUS\_PARMS** structure contains information for the [**MCI\_STATUS**](mci-status.md) command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a04d8-106">Syntax</span></span>


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a><span data-ttu-id="a04d8-107">Members</span><span class="sxs-lookup"><span data-stu-id="a04d8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a04d8-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="a04d8-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="a04d8-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="a04d8-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="a04d8-110">**dwReturn**</span><span class="sxs-lookup"><span data-stu-id="a04d8-110">**dwReturn**</span></span>
</dt> <dd>

<span data-ttu-id="a04d8-111">Contiene informazioni sulla restituzione.</span><span class="sxs-lookup"><span data-stu-id="a04d8-111">Contains information on return.</span></span>

</dd> <dt>

<span data-ttu-id="a04d8-112">**dwItem**</span><span class="sxs-lookup"><span data-stu-id="a04d8-112">**dwItem**</span></span>
</dt> <dd>

<span data-ttu-id="a04d8-113">Funzionalità sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="a04d8-113">Capability being queried.</span></span>

</dd> <dt>

<span data-ttu-id="a04d8-114">**dwTrack**</span><span class="sxs-lookup"><span data-stu-id="a04d8-114">**dwTrack**</span></span>
</dt> <dd>

<span data-ttu-id="a04d8-115">Lunghezza o numero di tracce.</span><span class="sxs-lookup"><span data-stu-id="a04d8-115">Length or number of tracks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a04d8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a04d8-116">Remarks</span></span>

<span data-ttu-id="a04d8-117">Il \_ \_ flag elemento stato MCI deve essere impostato nel parametro *FdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare il membro **dwItem** , che deve contenere una delle costanti che indicano le informazioni sullo stato richieste.</span><span class="sxs-lookup"><span data-stu-id="a04d8-117">The MCI\_STATUS\_ITEM flag must be set in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the **dwItem** member, which should contain one of the constants indicating what status information is being requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="a04d8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a04d8-118">Requirements</span></span>



| <span data-ttu-id="a04d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a04d8-119">Requirement</span></span> | <span data-ttu-id="a04d8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a04d8-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a04d8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a04d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a04d8-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a04d8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a04d8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a04d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a04d8-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a04d8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a04d8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a04d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a04d8-126"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a04d8-126"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a04d8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a04d8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04d8-128">**MCI**</span><span class="sxs-lookup"><span data-stu-id="a04d8-128">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a04d8-129">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="a04d8-129">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="a04d8-130">**\_stato MCI**</span><span class="sxs-lookup"><span data-stu-id="a04d8-130">**MCI\_STATUS**</span></span>](mci-status.md)
</dt> <dt>

<span data-ttu-id="a04d8-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a04d8-131">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

