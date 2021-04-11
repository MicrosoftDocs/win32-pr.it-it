---
title: Valori della sintassi dell'applicazione SNMP (SNMP. h)
description: I valori della sintassi dell'applicazione SNMP vengono utilizzati dalle applicazioni di gestione che utilizzano l'API di gestione SNMP Microsoft.
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d79ab6535c97fe4124aa1cb3f7ca11ce3eb02582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119530"
---
# <a name="snmp-application-syntax-values"></a><span data-ttu-id="5d58f-103">Valori della sintassi dell'applicazione SNMP</span><span class="sxs-lookup"><span data-stu-id="5d58f-103">SNMP Application Syntax Values</span></span>

<span data-ttu-id="5d58f-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="5d58f-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5d58f-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="5d58f-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5d58f-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="5d58f-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="5d58f-107">I valori della sintassi dell'applicazione SNMP vengono utilizzati dalle applicazioni di gestione che utilizzano l'API di gestione SNMP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5d58f-107">The SNMP Application Syntax Values are used by management applications that employ the Microsoft SNMP Management API.</span></span>



| <span data-ttu-id="5d58f-108">Costante</span><span class="sxs-lookup"><span data-stu-id="5d58f-108">Constant</span></span>                                                                                                                                                                                  | <span data-ttu-id="5d58f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d58f-109">Description</span></span>                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <span data-ttu-id="5d58f-110"><dt>**\_indirizzo IP ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-110"><dt>**ASN\_IPADDRESS**</dt></span></span> </dl>                             | <span data-ttu-id="5d58f-111">Indica una variabile dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="5d58f-111">Indicates an IP address variable.</span></span><br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <span data-ttu-id="5d58f-112"><dt>**\_COUNTER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-112"><dt>**ASN\_COUNTER32**</dt></span></span> </dl>                             | <span data-ttu-id="5d58f-113">Indica una variabile contatore.</span><span class="sxs-lookup"><span data-stu-id="5d58f-113">Indicates a counter variable.</span></span><br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <span data-ttu-id="5d58f-114"><dt>**\_GAUGE32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-114"><dt>**ASN\_GAUGE32**</dt></span></span> </dl>                                   | <span data-ttu-id="5d58f-115">Indica una variabile del misuratore.</span><span class="sxs-lookup"><span data-stu-id="5d58f-115">Indicates a gauge variable.</span></span> <span data-ttu-id="5d58f-116">Questa variabile descrive un tipo Unsigned32 in conformità con RFC 1902.</span><span class="sxs-lookup"><span data-stu-id="5d58f-116">This variable describes an Unsigned32 type in conformance with RFC 1902.</span></span><br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <span data-ttu-id="5d58f-117"><dt>**\_TimeTicks ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-117"><dt>**ASN\_TIMETICKS**</dt></span></span> </dl>                             | <span data-ttu-id="5d58f-118">Indica una variabile TimeTicks.</span><span class="sxs-lookup"><span data-stu-id="5d58f-118">Indicates a timeticks variable.</span></span><br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <span data-ttu-id="5d58f-119"><dt>**ASN \_ opaco**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-119"><dt>**ASN\_OPAQUE**</dt></span></span> </dl>                                      | <span data-ttu-id="5d58f-120">Indica una variabile opaca.</span><span class="sxs-lookup"><span data-stu-id="5d58f-120">Indicates an opaque variable.</span></span><br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <span data-ttu-id="5d58f-121"><dt>**\_COUNTER64 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-121"><dt>**ASN\_COUNTER64**</dt></span></span> </dl>                             | <span data-ttu-id="5d58f-122">Indica una variabile contatore che aumenta fino a quando non raggiunge un valore massimo di (2 ^ 64)-1.</span><span class="sxs-lookup"><span data-stu-id="5d58f-122">Indicates a counter variable that increases until it reaches a maximum value of (2^64) - 1.</span></span><br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <span data-ttu-id="5d58f-123"><dt>**\_UINTEGER32 ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-123"><dt>**ASN\_UINTEGER32**</dt></span></span> </dl>                          | <span data-ttu-id="5d58f-124">Indica una variabile di Unsigned Integer a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="5d58f-124">Indicates a 32-bit unsigned integer variable.</span></span> <span data-ttu-id="5d58f-125">Questa variabile descrive un tipo UInteger32 in conformità con RFC 1442.</span><span class="sxs-lookup"><span data-stu-id="5d58f-125">This variable describes a UInteger32 type in conformance with RFC 1442.</span></span><br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <span data-ttu-id="5d58f-126"><dt>**\_UNSIGNED32 RFC2578 \_ ASN**</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-126"><dt>**ASN\_RFC2578\_UNSIGNED32**</dt></span></span> </dl> | <span data-ttu-id="5d58f-127">Vedere ASN \_ GAUGE32.</span><span class="sxs-lookup"><span data-stu-id="5d58f-127">See ASN\_GAUGE32.</span></span><br/>                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="5d58f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d58f-128">Requirements</span></span>



| <span data-ttu-id="5d58f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d58f-129">Requirement</span></span> | <span data-ttu-id="5d58f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="5d58f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d58f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d58f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5d58f-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d58f-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="5d58f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d58f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5d58f-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5d58f-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5d58f-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d58f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d58f-136"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d58f-136"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d58f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d58f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d58f-138">Panoramica del protocollo Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="5d58f-138">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="5d58f-139">Riferimento SNMP</span><span class="sxs-lookup"><span data-stu-id="5d58f-139">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="5d58f-140">Costanti SNMP</span><span class="sxs-lookup"><span data-stu-id="5d58f-140">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

