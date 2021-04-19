---
description: Contiene un solo indirizzo di qualsiasi tipo di indirizzi supportati.
ms.assetid: 3f840842-8992-4fab-8820-cbbfc63242b8
title: Struttura INDIRIZZO2 (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4a8d66548aa683abf82b795d6a47e93fbdc03e08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311651"
---
# <a name="address2-structure"></a><span data-ttu-id="06c31-103">Struttura INDIRIZZO2</span><span class="sxs-lookup"><span data-stu-id="06c31-103">ADDRESS2 structure</span></span>

<span data-ttu-id="06c31-104">La struttura **Address** contiene un solo indirizzo di qualsiasi tipo di indirizzi supportati.</span><span class="sxs-lookup"><span data-stu-id="06c31-104">The **ADDRESS** structure contains a single address of any type of supported addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06c31-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
    BYTE                  IP6Address[IP6_ADDRESS_SIZE];
    BYTE                  IPXRawAddress[IPX_ADDRESS_SIZE];
    IPX_ADDRESS           IPXAddress;
    BYTE                  VinesIPRawAddress[VINES_IP_ADDRESS_SIZE];
    VINES_IP_ADDRESS      VinesIPAddress;
    ETHERNET_SRC_ADDRESS  EthernetSrcAddress;
    ETHERNET_DST_ADDRESS  EthernetDstAddress;
    TOKENRING_SRC_ADDRESS TokenringSrcAddress;
    TOKENRING_DST_ADDRESS TokenringDstAddress;
    FDDI_SRC_ADDRESS      FddiSrcAddress;
    FDDI_DST_ADDRESS      FddiDstAddress;
  };
  WORD  Flags;
} ADDRESS, *LPADDRESS;
```



## <a name="members"></a><span data-ttu-id="06c31-106">Members</span><span class="sxs-lookup"><span data-stu-id="06c31-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="06c31-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="06c31-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-108">Tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="06c31-108">Address type.</span></span> <span data-ttu-id="06c31-109">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="06c31-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="06c31-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="06c31-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="06c31-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="06c31-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="06c31-112">ADDRESS_TYPE_IP6</span><span class="sxs-lookup"><span data-stu-id="06c31-112">ADDRESS_TYPE_IP6</span></span></dd> <dd><span data-ttu-id="06c31-113">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="06c31-113">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="06c31-114">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="06c31-114">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="06c31-115">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="06c31-115">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="06c31-116">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="06c31-116">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="06c31-117">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="06c31-117">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="06c31-118">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="06c31-118">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="06c31-119">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="06c31-119">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="06c31-120">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="06c31-120">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="06c31-121">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="06c31-121">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="06c31-122">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="06c31-122">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="06c31-123">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="06c31-123">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="06c31-124">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-124">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-125">Visualizzazione dei dati espressi come indirizzo MAC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="06c31-125">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-126">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-126">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-127">Visualizzazione dei dati espressi come indirizzo IP non elaborato.</span><span class="sxs-lookup"><span data-stu-id="06c31-127">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-128">**IP6Address**</span><span class="sxs-lookup"><span data-stu-id="06c31-128">**IP6Address**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-129">Visualizzazione dei dati espressi come indirizzo IP non elaborato versione 6.</span><span class="sxs-lookup"><span data-stu-id="06c31-129">View of the data expressed as a raw IP version 6 address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-130">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-130">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-131">Visualizzazione dei dati espressi come un indirizzo IPX non elaborato.</span><span class="sxs-lookup"><span data-stu-id="06c31-131">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-132">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-132">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-133">Visualizzazione dei dati espressi come valore di indirizzo IPX decodificato.</span><span class="sxs-lookup"><span data-stu-id="06c31-133">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-134">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-134">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-135">Visualizzazione dei dati espressi come indirizzo IP delle viti non elaborate.</span><span class="sxs-lookup"><span data-stu-id="06c31-135">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-136">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-136">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-137">Visualizzazione dei dati espressi come indirizzo IP delle viti decodificate.</span><span class="sxs-lookup"><span data-stu-id="06c31-137">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-138">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-138">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-139">Visualizzazione dei dati espressi come indirizzo di origine Ethernet.</span><span class="sxs-lookup"><span data-stu-id="06c31-139">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-140">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-140">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-141">Visualizzazione dei dati espressi come indirizzo di destinazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="06c31-141">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-142">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-142">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-143">Visualizzazione dei dati come indirizzo di origine dell'anello di token.</span><span class="sxs-lookup"><span data-stu-id="06c31-143">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-144">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-144">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-145">Visualizzazione dei dati come indirizzo di destinazione dell'anello di token.</span><span class="sxs-lookup"><span data-stu-id="06c31-145">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-146">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-146">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-147">Visualizzazione dei dati espressi come indirizzo di origine FDDI.</span><span class="sxs-lookup"><span data-stu-id="06c31-147">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-148">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="06c31-148">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="06c31-149">Visualizzazione dei dati espressi come indirizzo di destinazione FDDI.</span><span class="sxs-lookup"><span data-stu-id="06c31-149">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="06c31-150">**Flag**</span><span class="sxs-lookup"><span data-stu-id="06c31-150">**Flags**</span></span>
<span data-ttu-id="06c31-151"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="06c31-151"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="06c31-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06c31-152">Requirements</span></span>



| <span data-ttu-id="06c31-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c31-153">Requirement</span></span> | <span data-ttu-id="06c31-154">Valore</span><span class="sxs-lookup"><span data-stu-id="06c31-154">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="06c31-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c31-155">Minimum supported client</span></span><br/> | <span data-ttu-id="06c31-156">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06c31-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="06c31-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06c31-157">Minimum supported server</span></span><br/> | <span data-ttu-id="06c31-158">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06c31-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="06c31-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06c31-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c31-160"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c31-160"><dt>Netmon.h</dt></span></span> </dl> |



 

 




