---
title: MCI_HMS_HOUR macro (Mciapi. h)
description: La \_ macro MCI HMS \_ hour Recupera il componente hours da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR macro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048743"
---
# <a name="mci_hms_hour-macro"></a><span data-ttu-id="55563-104">\_Macro di ora della settime MCI \_</span><span class="sxs-lookup"><span data-stu-id="55563-104">MCI\_HMS\_HOUR macro</span></span>

<span data-ttu-id="55563-105">La macro **MCI \_ HMS \_ hour** Recupera il componente hours da un parametro contenente le informazioni relative a ore/minuti/secondi (HMS) compressi.</span><span class="sxs-lookup"><span data-stu-id="55563-105">The **MCI\_HMS\_HOUR** macro retrieves the hours component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="55563-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55563-106">Syntax</span></span>


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="55563-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="55563-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55563-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="55563-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="55563-109">Tempo in formato HMS.</span><span class="sxs-lookup"><span data-stu-id="55563-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55563-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55563-110">Return value</span></span>

<span data-ttu-id="55563-111">Restituisce il componente relativo alle ore delle informazioni di HMS specificate.</span><span class="sxs-lookup"><span data-stu-id="55563-111">Returns the hours component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="55563-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="55563-112">Remarks</span></span>

<span data-ttu-id="55563-113">L'ora nel formato HMS è espressa come valore **DWORD** con il byte meno significativo contenente le ore, il successivo byte meno significativo che contiene minuti e il successivo byte meno significativo contenente i secondi.</span><span class="sxs-lookup"><span data-stu-id="55563-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="55563-114">Il byte più significativo è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="55563-114">The most significant byte is unused.</span></span>

<span data-ttu-id="55563-115">La macro **MCI \_ HMS \_ hour** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="55563-115">The **MCI\_HMS\_HOUR** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a><span data-ttu-id="55563-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55563-116">Requirements</span></span>



| <span data-ttu-id="55563-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="55563-117">Requirement</span></span> | <span data-ttu-id="55563-118">Valore</span><span class="sxs-lookup"><span data-stu-id="55563-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="55563-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55563-119">Minimum supported client</span></span><br/> | <span data-ttu-id="55563-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55563-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="55563-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55563-121">Minimum supported server</span></span><br/> | <span data-ttu-id="55563-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="55563-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55563-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55563-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="55563-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="55563-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55563-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55563-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55563-126">MCI</span><span class="sxs-lookup"><span data-stu-id="55563-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="55563-127">Macro MCI</span><span class="sxs-lookup"><span data-stu-id="55563-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





