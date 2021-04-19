---
description: Le costanti seguenti vengono usate con il protocollo COPP (Certified Output Protocol) per i meccanismi di protezione dell'output specifici.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: Flag del tipo di protezione COPP (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333600"
---
# <a name="copp-protection-type-flags"></a><span data-ttu-id="aeb2e-103">Flag del tipo di protezione COPP</span><span class="sxs-lookup"><span data-stu-id="aeb2e-103">COPP Protection Type Flags</span></span>

<span data-ttu-id="aeb2e-104">Le costanti seguenti vengono usate con il protocollo COPP (Certified Output Protocol) per i meccanismi di protezione dell'output specifici.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-104">The follow constants are used with Certified Output Protection Protocol (COPP) to specific output protection mechanisms.</span></span>



| <span data-ttu-id="aeb2e-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="aeb2e-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="aeb2e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aeb2e-106">Description</span></span>                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <span data-ttu-id="aeb2e-107"><dt>**Copp \_ 0x80000000 \_ sconosciuto ProtectionType**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-107"><dt>**COPP\_ProtectionType\_Unknown**</dt> <dt>0x80000000</dt></span></span> </dl>     | <span data-ttu-id="aeb2e-108">Meccanismo di protezione sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-108">Unknown protection mechanism.</span></span><br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <span data-ttu-id="aeb2e-109"><dt>**Copp \_ ProtectionType \_ None**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-109"><dt>**COPP\_ProtectionType\_None**</dt> <dt>0x00000000</dt></span></span> </dl>                 | <span data-ttu-id="aeb2e-110">Nessun meccanismo di protezione.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-110">No protection mechanisms.</span></span><br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <span data-ttu-id="aeb2e-111"><dt>**Copp \_ 0x00000001 ProtectionType \_ HDCP**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-111"><dt>**COPP\_ProtectionType\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="aeb2e-112">High-Bandwidth protezione del contenuto digitali (HDCP).</span><span class="sxs-lookup"><span data-stu-id="aeb2e-112">High-Bandwidth Digital Content Protection (HDCP).</span></span><br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <span data-ttu-id="aeb2e-113"><dt>**Copp \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-113"><dt>**COPP\_ProtectionType\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                     | <span data-ttu-id="aeb2e-114">Protezione copia analoga (ACP).</span><span class="sxs-lookup"><span data-stu-id="aeb2e-114">Analog Copy Protection (ACP).</span></span><br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <span data-ttu-id="aeb2e-115"><dt>**Copp \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-115"><dt>**COPP\_ProtectionType\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="aeb2e-116">Sistema di gestione della generazione di copia analogico (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="aeb2e-116">Copy Generation Management System   Analog (CGMS-A).</span></span><br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <span data-ttu-id="aeb2e-117"><dt>**Copp \_ ProtectionType \_ mask**</dt> <dt>0x80000007</dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-117"><dt>**COPP\_ProtectionType\_Mask**</dt> <dt>0x80000007</dt></span></span> </dl>                 | <span data-ttu-id="aeb2e-118">Maschera di maschera per isolare i flag validi.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-118">Bitmask to isolate valid flags.</span></span><br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <span data-ttu-id="aeb2e-119"><dt>**Copp \_ 0x7FFFFFF8 \_ riservato ProtectionType**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-119"><dt>**COPP\_ProtectionType\_Reserved**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl> | <span data-ttu-id="aeb2e-120">Riservato.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-120">Reserved.</span></span> <span data-ttu-id="aeb2e-121">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-121">Must be zero.</span></span><br/>                              |



## <a name="remarks"></a><span data-ttu-id="aeb2e-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="aeb2e-122">Remarks</span></span>

<span data-ttu-id="aeb2e-123">Alcuni metodi restituiscono un flag singolo da questo tipo di enumerazione e alcuni metodi restituiscono **un operatore OR** bit per bit di uno o più flag.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-123">Some methods return a single flag from this enumeration type, and some methods return a bitwise **OR** of one or more flags.</span></span>

<span data-ttu-id="aeb2e-124">Questi flag vengono usati nelle query e nei comandi COPP seguenti.</span><span class="sxs-lookup"><span data-stu-id="aeb2e-124">These flags are used in the following COPP queries and commands.</span></span>

-   <span data-ttu-id="aeb2e-125">Livello di protezione globale</span><span class="sxs-lookup"><span data-stu-id="aeb2e-125">Global Protection Level</span></span>
-   <span data-ttu-id="aeb2e-126">Livello di protezione locale</span><span class="sxs-lookup"><span data-stu-id="aeb2e-126">Local Protection Level</span></span>
-   <span data-ttu-id="aeb2e-127">Tipo di protezione</span><span class="sxs-lookup"><span data-stu-id="aeb2e-127">Protection Type</span></span>
-   <span data-ttu-id="aeb2e-128">Imposta il livello di protezione</span><span class="sxs-lookup"><span data-stu-id="aeb2e-128">Set Protection Level</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb2e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aeb2e-129">Requirements</span></span>



| <span data-ttu-id="aeb2e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb2e-130">Requirement</span></span> | <span data-ttu-id="aeb2e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="aeb2e-131">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="aeb2e-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aeb2e-132">Header</span></span><br/> | <dl> <span data-ttu-id="aeb2e-133"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb2e-133"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb2e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aeb2e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb2e-135">Costanti e GUID</span><span class="sxs-lookup"><span data-stu-id="aeb2e-135">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="aeb2e-136">Uso di COPP (Certified Output Protocol)</span><span class="sxs-lookup"><span data-stu-id="aeb2e-136">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




