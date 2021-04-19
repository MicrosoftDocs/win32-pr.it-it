---
description: Pacchetti le informazioni sul tipo di oggetto, sulla versione e sulle dimensioni richieste in molte strutture NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Struttura NDIS_OBJECT_HEADER (Ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311681"
---
# <a name="ndis_object_header-structure"></a><span data-ttu-id="dae00-103">Struttura dell'intestazione dell' \_ oggetto NDIS \_</span><span class="sxs-lookup"><span data-stu-id="dae00-103">NDIS\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="dae00-104">La struttura dell' **\_ \_ intestazione dell'oggetto NDIS** impacca le informazioni sul tipo di oggetto, sulla versione e sulle dimensioni necessarie in molte strutture NDIS 6,0.</span><span class="sxs-lookup"><span data-stu-id="dae00-104">The **NDIS\_OBJECT\_HEADER** structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dae00-105">Syntax</span></span>


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="dae00-106">Members</span><span class="sxs-lookup"><span data-stu-id="dae00-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dae00-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dae00-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="dae00-108">Specifica il tipo di oggetto NDIS descritto da una struttura.</span><span class="sxs-lookup"><span data-stu-id="dae00-108">Specifies the type of NDIS object that a structure describes.</span></span>

</dd> <dt>

<span data-ttu-id="dae00-109">**Revisione**</span><span class="sxs-lookup"><span data-stu-id="dae00-109">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="dae00-110">Specifica il numero di revisione della struttura.</span><span class="sxs-lookup"><span data-stu-id="dae00-110">Specifies the revision number of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="dae00-111">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="dae00-111">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="dae00-112">Specifica la dimensione totale, in byte, della struttura NDIS che contiene l' **intestazione dell' \_ oggetto \_ NDIS**.</span><span class="sxs-lookup"><span data-stu-id="dae00-112">Specifies the total size, in bytes, of the NDIS structure that contains the **NDIS\_OBJECT\_HEADER**.</span></span> <span data-ttu-id="dae00-113">Questa dimensione include le dimensioni del membro **dell' \_ \_ intestazione dell'oggetto NDIS** e di tutti gli altri membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="dae00-113">This size includes the size of the **NDIS\_OBJECT\_HEADER** member and all other members of the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dae00-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dae00-114">Requirements</span></span>



| <span data-ttu-id="dae00-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae00-115">Requirement</span></span> | <span data-ttu-id="dae00-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dae00-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae00-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dae00-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dae00-118">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="dae00-118">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dae00-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dae00-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dae00-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dae00-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dae00-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="dae00-121">Redistributable</span></span><br/>          | <span data-ttu-id="dae00-122">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="dae00-122">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="dae00-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dae00-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dae00-124"><dt>Ntddndis. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dae00-124"><dt>Ntddndis.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae00-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dae00-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae00-126">**\_Elenco BSSID \_ DOT11**</span><span class="sxs-lookup"><span data-stu-id="dae00-126">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> </dl>

 

 




