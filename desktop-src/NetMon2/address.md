---
description: È obsoleto e non deve essere utilizzato.
ms.assetid: cbe89779-403d-406e-af3c-d6530bf3008e
title: Struttura ADDRESS (Netmon. h)
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
ms.openlocfilehash: c577758401bede53c79fd109caa6d8b9cb3d9163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312836"
---
# <a name="address-structure"></a><span data-ttu-id="835e8-103">Struttura degli indirizzi</span><span class="sxs-lookup"><span data-stu-id="835e8-103">ADDRESS structure</span></span>

<span data-ttu-id="835e8-104">La struttura degli **indirizzi** è obsoleta e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="835e8-104">The **ADDRESS** structure is obsolete and should not be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="835e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="835e8-105">Syntax</span></span>


```C++
typedef struct _ADDRESS {
  DWORD Type;
  union {
    BYTE                  MACAddress[MAC_ADDRESS_SIZE];
    BYTE                  IPAddress[IP_ADDRESS_SIZE];
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



## <a name="members"></a><span data-ttu-id="835e8-106">Members</span><span class="sxs-lookup"><span data-stu-id="835e8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="835e8-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="835e8-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-108">Tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="835e8-108">Address type.</span></span> <span data-ttu-id="835e8-109">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="835e8-109">Values can be one of the following:</span></span>

<dl> <dd><span data-ttu-id="835e8-110">ADDRESS_TYPE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="835e8-110">ADDRESS_TYPE_ETHERNET</span></span></dd> <dd><span data-ttu-id="835e8-111">ADDRESS_TYPE_IP</span><span class="sxs-lookup"><span data-stu-id="835e8-111">ADDRESS_TYPE_IP</span></span></dd> <dd><span data-ttu-id="835e8-112">ADDRESS_TYPE_IPX</span><span class="sxs-lookup"><span data-stu-id="835e8-112">ADDRESS_TYPE_IPX</span></span></dd> <dd><span data-ttu-id="835e8-113">ADDRESS_TYPE_TOKENRING</span><span class="sxs-lookup"><span data-stu-id="835e8-113">ADDRESS_TYPE_TOKENRING</span></span></dd> <dd><span data-ttu-id="835e8-114">ADDRESS_TYPE_FDDI</span><span class="sxs-lookup"><span data-stu-id="835e8-114">ADDRESS_TYPE_FDDI</span></span></dd> <dd><span data-ttu-id="835e8-115">ADDRESS_TYPE_XNS</span><span class="sxs-lookup"><span data-stu-id="835e8-115">ADDRESS_TYPE_XNS</span></span></dd> <dd><span data-ttu-id="835e8-116">ADDRESS_TYPE_ANY</span><span class="sxs-lookup"><span data-stu-id="835e8-116">ADDRESS_TYPE_ANY</span></span></dd> <dd><span data-ttu-id="835e8-117">ADDRESS_TYPE_ANY_GROUP</span><span class="sxs-lookup"><span data-stu-id="835e8-117">ADDRESS_TYPE_ANY_GROUP</span></span></dd> <dd><span data-ttu-id="835e8-118">ADDRESS_TYPE_FIND_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="835e8-118">ADDRESS_TYPE_FIND_HIGHEST</span></span></dd> <dd><span data-ttu-id="835e8-119">ADDRESS_TYPE_VINES_IP</span><span class="sxs-lookup"><span data-stu-id="835e8-119">ADDRESS_TYPE_VINES_IP</span></span></dd> <dd><span data-ttu-id="835e8-120">ADDRESS_TYPE_LOCAL_ONLY</span><span class="sxs-lookup"><span data-stu-id="835e8-120">ADDRESS_TYPE_LOCAL_ONLY</span></span></dd> <dd><span data-ttu-id="835e8-121">ADDRESS_TYPE_ATM</span><span class="sxs-lookup"><span data-stu-id="835e8-121">ADDRESS_TYPE_ATM</span></span></dd> <dd><span data-ttu-id="835e8-122">ADDRESS_TYPE_1394</span><span class="sxs-lookup"><span data-stu-id="835e8-122">ADDRESS_TYPE_1394</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="835e8-123">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-123">**MACAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-124">Visualizzazione dei dati espressi come indirizzo MAC non elaborato.</span><span class="sxs-lookup"><span data-stu-id="835e8-124">View of the data expressed as a raw MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-125">**IPAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-125">**IPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-126">Visualizzazione dei dati espressi come indirizzo IP non elaborato.</span><span class="sxs-lookup"><span data-stu-id="835e8-126">View of the data expressed as a raw IP address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-127">**IPXRawAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-127">**IPXRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-128">Visualizzazione dei dati espressi come un indirizzo IPX non elaborato.</span><span class="sxs-lookup"><span data-stu-id="835e8-128">View of the data expressed as a raw IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-129">**IPXAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-129">**IPXAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-130">Visualizzazione dei dati espressi come valore di indirizzo IPX decodificato.</span><span class="sxs-lookup"><span data-stu-id="835e8-130">View of the data expressed as a decoded IPX address value.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-131">**VinesIPRawAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-131">**VinesIPRawAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-132">Visualizzazione dei dati espressi come indirizzo IP delle viti non elaborate.</span><span class="sxs-lookup"><span data-stu-id="835e8-132">View of the data expressed as a raw Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-133">**VinesIPAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-133">**VinesIPAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-134">Visualizzazione dei dati espressi come indirizzo IP delle viti decodificate.</span><span class="sxs-lookup"><span data-stu-id="835e8-134">View of the data expressed as a decoded Vines IP address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-135">**EthernetSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-135">**EthernetSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-136">Visualizzazione dei dati espressi come indirizzo di origine Ethernet.</span><span class="sxs-lookup"><span data-stu-id="835e8-136">View of the data expressed as an Ethernet source address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-137">**EthernetDstAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-137">**EthernetDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-138">Visualizzazione dei dati espressi come indirizzo di destinazione Ethernet.</span><span class="sxs-lookup"><span data-stu-id="835e8-138">View of the data expressed as an Ethernet destination address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-139">**TokenringSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-139">**TokenringSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-140">Visualizzazione dei dati come indirizzo di origine dell'anello di token.</span><span class="sxs-lookup"><span data-stu-id="835e8-140">A view of the data as a token ring source address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-141">**TokenringDstAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-141">**TokenringDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-142">Visualizzazione dei dati come indirizzo di destinazione dell'anello di token.</span><span class="sxs-lookup"><span data-stu-id="835e8-142">A view of the data as a token ring destination address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-143">**FddiSrcAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-143">**FddiSrcAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-144">Visualizzazione dei dati espressi come indirizzo di origine FDDI.</span><span class="sxs-lookup"><span data-stu-id="835e8-144">View of the data expressed as an FDDI source address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-145">**FddiDstAddress**</span><span class="sxs-lookup"><span data-stu-id="835e8-145">**FddiDstAddress**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-146">Visualizzazione dei dati espressi come indirizzo di destinazione FDDI.</span><span class="sxs-lookup"><span data-stu-id="835e8-146">View of the data expressed as an FDDI destination address.</span></span>

</dd> <dt>

<span data-ttu-id="835e8-147">**Flag**</span><span class="sxs-lookup"><span data-stu-id="835e8-147">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="835e8-148">Set di flag che modificano le proprietà dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="835e8-148">A set of flags that modify the address properties.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="835e8-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="835e8-149">Requirements</span></span>



| <span data-ttu-id="835e8-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="835e8-150">Requirement</span></span> | <span data-ttu-id="835e8-151">Valore</span><span class="sxs-lookup"><span data-stu-id="835e8-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="835e8-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="835e8-152">Minimum supported client</span></span><br/> | <span data-ttu-id="835e8-153">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="835e8-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="835e8-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="835e8-154">Minimum supported server</span></span><br/> | <span data-ttu-id="835e8-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="835e8-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="835e8-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="835e8-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="835e8-157"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="835e8-157"><dt>Netmon.h</dt></span></span> </dl> |



 

 




