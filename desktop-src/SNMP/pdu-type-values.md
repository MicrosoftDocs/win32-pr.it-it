---
title: Valori di tipo PDU (SNMP. h)
description: I valori di tipo PDU vengono usati nel \_ campo tipo PDU della PDU per descrivere il tipo.
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90086de73e53eb89b1f3e3925ae7669777a6a088
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478431"
---
# <a name="pdu-type-values"></a><span data-ttu-id="bc76d-103">Valori di tipo PDU</span><span class="sxs-lookup"><span data-stu-id="bc76d-103">PDU Type Values</span></span>

<span data-ttu-id="bc76d-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bc76d-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bc76d-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="bc76d-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bc76d-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="bc76d-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="bc76d-107">I valori di tipo PDU vengono usati nel **campo \_ tipo PDU** della PDU per descrivere il tipo.</span><span class="sxs-lookup"><span data-stu-id="bc76d-107">The PDU type values are used in the **pdu\_type** field of the PDU to describe its type.</span></span>



| <span data-ttu-id="bc76d-108">Costante</span><span class="sxs-lookup"><span data-stu-id="bc76d-108">Constant</span></span>                                                                                                                                                                   | <span data-ttu-id="bc76d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc76d-109">Description</span></span>                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <span data-ttu-id="bc76d-110"><dt>**\_Get SNMP PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-110"><dt>**SNMP\_PDU\_GET**</dt></span></span> </dl>                | <span data-ttu-id="bc76d-111">Ricerca e recupero di un valore da una variabile SNMP specificata.</span><span class="sxs-lookup"><span data-stu-id="bc76d-111">Search and retrieve a value from a specified SNMP variable.</span></span><br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <span data-ttu-id="bc76d-112"><dt>**datanext di SNMP \_ PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-112"><dt>**SNMP\_PDU\_GETNEXT**</dt></span></span> </dl>    | <span data-ttu-id="bc76d-113">Cercare e recuperare il valore di una variabile SNMP senza conoscere il nome esatto della variabile.</span><span class="sxs-lookup"><span data-stu-id="bc76d-113">Search and retrieve the value of an SNMP variable without knowing the exact name of the variable.</span></span><br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <span data-ttu-id="bc76d-114"><dt>**\_risposta PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-114"><dt>**SNMP\_PDU\_RESPONSE**</dt></span></span> </dl> | <span data-ttu-id="bc76d-115">Rispondere a una \_ richiesta SNMP PDU \_ Get o a un'istanza di SNMP \_ PDU \_ GetNext.</span><span class="sxs-lookup"><span data-stu-id="bc76d-115">Reply to an SNMP\_PDU\_GET or an SNMP\_PDU\_GETNEXT request.</span></span><br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <span data-ttu-id="bc76d-116"><dt>**\_set PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-116"><dt>**SNMP\_PDU\_SET**</dt></span></span> </dl>                | <span data-ttu-id="bc76d-117">Archivia un valore in una variabile SNMP specificata.</span><span class="sxs-lookup"><span data-stu-id="bc76d-117">Store a value in a specified SNMP variable.</span></span><br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <span data-ttu-id="bc76d-118"><dt>**\_V1TRAP PDU \_ SNMP**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-118"><dt>**SNMP\_PDU\_V1TRAP**</dt></span></span> </dl>       | <span data-ttu-id="bc76d-119">Indica che il Trap PDU è formattato in modo da essere conforme allo standard SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="bc76d-119">Indicates that the PDU trap is formatted to conform with the SNMPv1 standard.</span></span><br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <span data-ttu-id="bc76d-120"><dt>**SNMP \_ PDU \_ GetBulk**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-120"><dt>**SNMP\_PDU\_GETBULK**</dt></span></span> </dl>    | <span data-ttu-id="bc76d-121">Eseguire ricerche e recuperare più valori con una singola richiesta.</span><span class="sxs-lookup"><span data-stu-id="bc76d-121">Search and retrieve multiple values with a single request.</span></span><br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <span data-ttu-id="bc76d-122"><dt>**informazioni su SNMP \_ PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-122"><dt>**SNMP\_PDU\_INFORM**</dt></span></span> </dl>       | <span data-ttu-id="bc76d-123">Indica una PDU di richiesta di informazioni.</span><span class="sxs-lookup"><span data-stu-id="bc76d-123">Indicates an inform request PDU.</span></span><br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <span data-ttu-id="bc76d-124"><dt>**\_trap SNMP PDU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-124"><dt>**SNMP\_PDU\_TRAP**</dt></span></span> </dl>             | <span data-ttu-id="bc76d-125">Segnala al sistema di gestione un evento straordinario in SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="bc76d-125">Alerts the management system to an extraordinary event under SNMPv2C.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="bc76d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc76d-126">Requirements</span></span>



| <span data-ttu-id="bc76d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc76d-127">Requirement</span></span> | <span data-ttu-id="bc76d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="bc76d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bc76d-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc76d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bc76d-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc76d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="bc76d-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc76d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bc76d-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc76d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bc76d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc76d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc76d-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc76d-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc76d-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc76d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc76d-136">Panoramica del protocollo Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="bc76d-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="bc76d-137">Riferimento SNMP</span><span class="sxs-lookup"><span data-stu-id="bc76d-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="bc76d-138">Costanti SNMP</span><span class="sxs-lookup"><span data-stu-id="bc76d-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

