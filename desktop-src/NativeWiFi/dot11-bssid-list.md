---
description: Contiene un elenco di identificatori del set di servizi di base (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Struttura DOT11_BSSID_LIST (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313765"
---
# <a name="dot11_bssid_list-structure"></a><span data-ttu-id="bf89a-103">\_Struttura DOT11 BSSID \_ List</span><span class="sxs-lookup"><span data-stu-id="bf89a-103">DOT11\_BSSID\_LIST structure</span></span>

<span data-ttu-id="bf89a-104">La struttura dell' **\_ \_ elenco BSSID di DOT11** contiene un elenco di identificatori del set di servizi di base (BSS).</span><span class="sxs-lookup"><span data-stu-id="bf89a-104">The **DOT11\_BSSID\_LIST** structure contains a list of basic service set (BSS) identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf89a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf89a-105">Syntax</span></span>


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a><span data-ttu-id="bf89a-106">Members</span><span class="sxs-lookup"><span data-stu-id="bf89a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf89a-107">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="bf89a-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="bf89a-108">Struttura [**di \_ \_ intestazione di un oggetto NDIS**](ndis-object-header.md) che contiene le informazioni sul tipo, la versione e le dimensioni di una struttura NDIS.</span><span class="sxs-lookup"><span data-stu-id="bf89a-108">An [**NDIS\_OBJECT\_HEADER**](ndis-object-header.md) structure that contains the type, version, and, size information of an NDIS structure.</span></span> <span data-ttu-id="bf89a-109">Per la maggior parte delle strutture **DOT11 \_ BSSID \_ List** , impostare il membro del **tipo** su **tipo di \_ oggetto NDIS \_ \_ default**, impostare il membro **Revisione** su **DOT11 \_ BSSID \_ List \_ Revision \_ 1** e impostare il membro **size** su **sizeof (DOT11 \_ BSSID \_ List)**.</span><span class="sxs-lookup"><span data-stu-id="bf89a-109">For most **DOT11\_BSSID\_LIST** structures, set the **Type** member to **NDIS\_OBJECT\_TYPE\_DEFAULT**, set the **Revision** member to **DOT11\_BSSID\_LIST\_REVISION\_1**, and set the **Size** member to **sizeof(DOT11\_BSSID\_LIST)**.</span></span>

</dd> <dt>

<span data-ttu-id="bf89a-110">**uNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="bf89a-110">**uNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="bf89a-111">Numero di voci nella struttura.</span><span class="sxs-lookup"><span data-stu-id="bf89a-111">The number of entries in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="bf89a-112">**uTotalNumOfEntries**</span><span class="sxs-lookup"><span data-stu-id="bf89a-112">**uTotalNumOfEntries**</span></span>
</dt> <dd>

<span data-ttu-id="bf89a-113">Il numero totale di voci supportate.</span><span class="sxs-lookup"><span data-stu-id="bf89a-113">The total number of entries supported.</span></span>

</dd> <dt>

<span data-ttu-id="bf89a-114">**BSSIDs**</span><span class="sxs-lookup"><span data-stu-id="bf89a-114">**BSSIDs**</span></span>
</dt> <dd>

<span data-ttu-id="bf89a-115">Elenco di identificatori BSS.</span><span class="sxs-lookup"><span data-stu-id="bf89a-115">A list of BSS identifiers.</span></span> <span data-ttu-id="bf89a-116">Un identificatore BSS viene archiviato come tipo [**di \_ \_ indirizzo Mac DOT11**](dot11-mac-address-type.md) .</span><span class="sxs-lookup"><span data-stu-id="bf89a-116">A BSS identifier is stored as a [**DOT11\_MAC\_ADDRESS**](dot11-mac-address-type.md) type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf89a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf89a-117">Requirements</span></span>



| <span data-ttu-id="bf89a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf89a-118">Requirement</span></span> | <span data-ttu-id="bf89a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bf89a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf89a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf89a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf89a-121">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="bf89a-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf89a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf89a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf89a-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf89a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bf89a-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bf89a-124">Redistributable</span></span><br/>          | <span data-ttu-id="bf89a-125">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="bf89a-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="bf89a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf89a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf89a-127"><dt>Windot11. h (include Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf89a-127"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf89a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf89a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf89a-129">**\_parametri di connessione WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="bf89a-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




