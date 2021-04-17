---
title: Struttura MCI_VCR_SEEK_PARMS (VCR. h)
description: La \_ struttura parametri di MCI VCR \_ Seek \_ contiene i parametri per il \_ comando di ricerca MCI per i registratori di nastri video.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- Struttura MCI_VCR_SEEK_PARMS di Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302011a3e4bf10eb3a81db4a163f94f4322dea98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476006"
---
# <a name="mci_vcr_seek_parms-structure"></a><span data-ttu-id="12952-104">\_ \_ Struttura parametri di ricerca VCR MCI \_</span><span class="sxs-lookup"><span data-stu-id="12952-104">MCI\_VCR\_SEEK\_PARMS structure</span></span>

<span data-ttu-id="12952-105">La struttura **parametri di MCI \_ VCR \_ Seek \_** contiene i parametri per il comando di [**\_ ricerca MCI**](mci-seek.md) per i registratori di nastri video.</span><span class="sxs-lookup"><span data-stu-id="12952-105">The **MCI\_VCR\_SEEK\_PARMS** structure contains parameters for the [**MCI\_SEEK**](mci-seek.md) command for video-cassette recorders.</span></span>

## <a name="syntax"></a><span data-ttu-id="12952-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12952-106">Syntax</span></span>


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a><span data-ttu-id="12952-107">Members</span><span class="sxs-lookup"><span data-stu-id="12952-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="12952-108">**dwCallback**</span><span class="sxs-lookup"><span data-stu-id="12952-108">**dwCallback**</span></span>
</dt> <dd>

<span data-ttu-id="12952-109">La parola di ordine inferiore specifica un handle di finestra utilizzato per il \_ flag di notifica MCI.</span><span class="sxs-lookup"><span data-stu-id="12952-109">The low-order word specifies a window handle used for the MCI\_NOTIFY flag.</span></span>

</dd> <dt>

<span data-ttu-id="12952-110">**dwTo**</span><span class="sxs-lookup"><span data-stu-id="12952-110">**dwTo**</span></span>
</dt> <dd>

<span data-ttu-id="12952-111">Posizione in cui eseguire la ricerca.</span><span class="sxs-lookup"><span data-stu-id="12952-111">Position to seek to.</span></span>

</dd> <dt>

<span data-ttu-id="12952-112">**dwMark**</span><span class="sxs-lookup"><span data-stu-id="12952-112">**dwMark**</span></span>
</dt> <dd>

<span data-ttu-id="12952-113">Contrassegno numerato da cercare.</span><span class="sxs-lookup"><span data-stu-id="12952-113">Numbered mark to seek for.</span></span>

</dd> <dt>

<span data-ttu-id="12952-114">**dwAt**</span><span class="sxs-lookup"><span data-stu-id="12952-114">**dwAt**</span></span>
</dt> <dd>

<span data-ttu-id="12952-115">Ora di inizio della ricerca.</span><span class="sxs-lookup"><span data-stu-id="12952-115">Time when seek begins.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12952-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="12952-116">Remarks</span></span>

<span data-ttu-id="12952-117">Le posizioni vengono specificate nel formato ora corrente.</span><span class="sxs-lookup"><span data-stu-id="12952-117">Positions are specified in the current time format.</span></span>

<span data-ttu-id="12952-118">Quando si assegnano dati ai membri di questa struttura, impostare i flag corrispondenti nel parametro *fdwCommand* della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per convalidare i membri.</span><span class="sxs-lookup"><span data-stu-id="12952-118">When assigning data to the members of this structure, set the corresponding flags in the *fdwCommand* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to validate the members.</span></span>

## <a name="requirements"></a><span data-ttu-id="12952-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12952-119">Requirements</span></span>



| <span data-ttu-id="12952-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12952-120">Requirement</span></span> | <span data-ttu-id="12952-121">Valore</span><span class="sxs-lookup"><span data-stu-id="12952-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12952-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12952-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12952-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="12952-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="12952-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12952-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12952-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="12952-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12952-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12952-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12952-127"><dt>VCR. h</dt></span><span class="sxs-lookup"><span data-stu-id="12952-127"><dt>Vcr.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12952-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12952-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12952-129">**MCI**</span><span class="sxs-lookup"><span data-stu-id="12952-129">**MCI**</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="12952-130">**Strutture MCI**</span><span class="sxs-lookup"><span data-stu-id="12952-130">**MCI Structures**</span></span>](mci-structures.md)
</dt> <dt>

[<span data-ttu-id="12952-131">**\_ricerca MCI**</span><span class="sxs-lookup"><span data-stu-id="12952-131">**MCI\_SEEK**</span></span>](mci-seek.md)
</dt> <dt>

<span data-ttu-id="12952-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="12952-132">[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))</span></span>
</dt> </dl>

 

