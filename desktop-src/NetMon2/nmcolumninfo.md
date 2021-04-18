---
description: La struttura NMCOLUMNINFO definisce una colonna nel riquadro superiore del Visualizzatore eventi.
ms.assetid: 21e0a129-464b-45b3-9c6b-6594e62fbce9
title: Struttura NMCOLUMNINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EVENTCOLUMNINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b486590871f0af28736717d4c2f332aae342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318969"
---
# <a name="nmcolumninfo-structure"></a><span data-ttu-id="8e5e2-103">Struttura NMCOLUMNINFO</span><span class="sxs-lookup"><span data-stu-id="8e5e2-103">NMCOLUMNINFO structure</span></span>

<span data-ttu-id="8e5e2-104">La struttura **NMCOLUMNINFO** definisce una colonna nel riquadro superiore del Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-104">The **NMCOLUMNINFO** structure defines one column in the top pane of the Event Viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e5e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e5e2-105">Syntax</span></span>


```C++
typedef struct {
  LPSTR           szColumnName;
  NMCOLUMNVARIANT VariantData;
} EVENTCOLUMNINFO;
```



## <a name="members"></a><span data-ttu-id="8e5e2-106">Members</span><span class="sxs-lookup"><span data-stu-id="8e5e2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8e5e2-107">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="8e5e2-107">**szColumnName**</span></span>
</dt> <dd>

<span data-ttu-id="8e5e2-108">Nome visualizzabile di una colonna specifica.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-108">Displayable name of a specific column.</span></span> <span data-ttu-id="8e5e2-109">Se il nome è troppo lungo, non sarà completamente visibile nella configurazione predefinita del Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-109">If the name is too long, it will not be completely visible in the default Event Viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="8e5e2-110">**VariantData**</span><span class="sxs-lookup"><span data-stu-id="8e5e2-110">**VariantData**</span></span>
</dt> <dd>

<span data-ttu-id="8e5e2-111">Dati inseriti nella colonna.</span><span class="sxs-lookup"><span data-stu-id="8e5e2-111">The data inserted into the column.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8e5e2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e5e2-112">Requirements</span></span>



| <span data-ttu-id="8e5e2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e5e2-113">Requirement</span></span> | <span data-ttu-id="8e5e2-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8e5e2-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8e5e2-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e5e2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8e5e2-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8e5e2-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8e5e2-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e5e2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8e5e2-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8e5e2-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8e5e2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e5e2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e5e2-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e5e2-120"><dt>Netmon.h</dt></span></span> </dl> |



 

 




