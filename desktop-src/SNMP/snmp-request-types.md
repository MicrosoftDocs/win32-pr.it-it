---
title: Tipi di richiesta SNMP (SNMP. h)
description: I tipi di richiesta SNMP vengono utilizzati per descrivere l'operazione che il servizio SNMP sta richiedendo all'agente di estensione di eseguire.
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c37b0064b66fd31f3dbd07dfb593b3fa5900e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478430"
---
# <a name="snmp-request-types"></a><span data-ttu-id="2879e-103">Tipi di richiesta SNMP</span><span class="sxs-lookup"><span data-stu-id="2879e-103">SNMP Request Types</span></span>

<span data-ttu-id="2879e-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="2879e-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2879e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="2879e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="2879e-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="2879e-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="2879e-107">I tipi di richiesta SNMP vengono utilizzati per descrivere l'operazione che il servizio SNMP sta richiedendo all'agente di estensione di eseguire.</span><span class="sxs-lookup"><span data-stu-id="2879e-107">The SNMP Request Types are used to describe the operation that the SNMP service is requesting the extension agent to perform.</span></span>



| <span data-ttu-id="2879e-108">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="2879e-108">Constant/value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="2879e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2879e-109">Description</span></span>                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <span data-ttu-id="2879e-110"><dt>**SNMP \_ ESTENSIONE \_ Get**</dt> <dt>SNMP \_ PDU \_ Get</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-110"><dt>**SNMP\_EXTENSION\_GET**</dt> <dt>SNMP\_PDU\_GET</dt></span></span> </dl>                       | <span data-ttu-id="2879e-111">Recuperare il valore dei valori delle variabili specificate.</span><span class="sxs-lookup"><span data-stu-id="2879e-111">Retrieve the value of values of the specified variables.</span></span><br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <span data-ttu-id="2879e-112"><dt>**SNMP \_ ESTENSIONE \_ get \_ Next**</dt> <dt>SNMP \_ PDU \_ GetNext</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-112"><dt>**SNMP\_EXTENSION\_GET\_NEXT**</dt> <dt>SNMP\_PDU\_GETNEXT</dt></span></span> </dl>   | <span data-ttu-id="2879e-113">Recuperare il valore o i valori del successore lessicografico delle variabili specificate.</span><span class="sxs-lookup"><span data-stu-id="2879e-113">Retrieve the value or values of the lexicographic successor of the specified variables.</span></span><br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <span data-ttu-id="2879e-114"><dt>**SNMP \_ ESTENSIONE \_ get \_ bulk**</dt> <dt>SNMP \_ PDU \_ GetBulk</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-114"><dt>**SNMP\_EXTENSION\_GET\_BULK**</dt> <dt>SNMP\_PDU\_GETBULK</dt></span></span> </dl>   | <span data-ttu-id="2879e-115">Eseguire ricerche e recuperare più valori con una singola richiesta.</span><span class="sxs-lookup"><span data-stu-id="2879e-115">Search and retrieve multiple values with a single request.</span></span><br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <span data-ttu-id="2879e-116"><dt>**\_test del \_ set di estensioni SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-116"><dt>**SNMP\_EXTENSION\_SET\_TEST**</dt></span></span> </dl>                                                                           | <span data-ttu-id="2879e-117">Convalidare i valori delle variabili specificate.</span><span class="sxs-lookup"><span data-stu-id="2879e-117">Validate the values of the specified variables.</span></span> <span data-ttu-id="2879e-118">Questa operazione ottimizza la probabilità di un'operazione di scrittura riuscita durante la richiesta di COMMIT.</span><span class="sxs-lookup"><span data-stu-id="2879e-118">This operation maximizes the probability of a successful write operation during the COMMIT request.</span></span> <span data-ttu-id="2879e-119">Per ulteriori informazioni, vedere la funzione [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) .</span><span class="sxs-lookup"><span data-stu-id="2879e-119">For more information, see the [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) function.</span></span><br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <span data-ttu-id="2879e-120"><dt>**SNMP \_ set di estensioni di \_ \_ commit**</dt> SNMP del set di estensioni <dt> \_ \_</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-120"><dt>**SNMP\_EXTENSION\_SET\_COMMIT**</dt> <dt>SNMP\_PDU\_SET</dt></span></span> </dl> | <span data-ttu-id="2879e-121">Scrive i nuovi valori nelle variabili specificate.</span><span class="sxs-lookup"><span data-stu-id="2879e-121">Write the new values to the specified variables.</span></span><br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <span data-ttu-id="2879e-122"><dt>**\_ \_ Annulla set di estensioni SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-122"><dt>**SNMP\_EXTENSION\_SET\_UNDO**</dt></span></span> </dl>                                                                           | <span data-ttu-id="2879e-123">Reimpostare i valori delle variabili specificate sui rispettivi valori prima della richiesta di COMMIT.</span><span class="sxs-lookup"><span data-stu-id="2879e-123">Reset the values of the specified variables to their values before the COMMIT request.</span></span><br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <span data-ttu-id="2879e-124"><dt>**\_pulizia del \_ set di estensioni SNMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-124"><dt>**SNMP\_EXTENSION\_SET\_CLEANUP**</dt></span></span> </dl>                                                                  | <span data-ttu-id="2879e-125">Rilascia le risorse allocate nelle richieste e nelle operazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="2879e-125">Release the resources allocated in previous requests and operations.</span></span><br/>                                                                                                                                                                             |



## <a name="requirements"></a><span data-ttu-id="2879e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2879e-126">Requirements</span></span>



| <span data-ttu-id="2879e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2879e-127">Requirement</span></span> | <span data-ttu-id="2879e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2879e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2879e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2879e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2879e-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2879e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="2879e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2879e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2879e-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2879e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2879e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2879e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2879e-134"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="2879e-134"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2879e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2879e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2879e-136">Panoramica del protocollo Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="2879e-136">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="2879e-137">Riferimento SNMP</span><span class="sxs-lookup"><span data-stu-id="2879e-137">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="2879e-138">Costanti SNMP</span><span class="sxs-lookup"><span data-stu-id="2879e-138">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

