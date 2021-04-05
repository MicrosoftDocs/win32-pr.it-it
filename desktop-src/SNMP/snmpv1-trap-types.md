---
title: Tipi trap SNMPv1 (SNMP. h)
description: I tipi trap SNMPv1 descrivono un set predefinito di tipi trap generici formattati in modo da essere conformi allo standard SNMPv1 Trap PDU.
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1091bc6af4fa4b1ddfadbaf35e3e69250ded6dcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874554"
---
# <a name="snmpv1-trap-types"></a><span data-ttu-id="b508b-103">Tipi trap SNMPv1</span><span class="sxs-lookup"><span data-stu-id="b508b-103">SNMPv1 Trap Types</span></span>

<span data-ttu-id="b508b-104">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="b508b-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b508b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b508b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b508b-106">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="b508b-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="b508b-107">I tipi trap SNMPv1 descrivono un set predefinito di tipi trap generici formattati in modo da essere conformi allo standard SNMPv1 Trap PDU.</span><span class="sxs-lookup"><span data-stu-id="b508b-107">The SNMPv1 trap types describe a predefined set of generic trap types that are formatted to comply with the SNMPv1 trap PDU standard.</span></span>



| <span data-ttu-id="b508b-108">Costante</span><span class="sxs-lookup"><span data-stu-id="b508b-108">Constant</span></span>                                                                                                                                                                                                          | <span data-ttu-id="b508b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b508b-109">Description</span></span>                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <span data-ttu-id="b508b-110"><dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-110"><dt>**SNMP\_GENERICTRAP\_COLDSTART**</dt></span></span> </dl>             | <span data-ttu-id="b508b-111">Indica una trap di avvio a freddo.</span><span class="sxs-lookup"><span data-stu-id="b508b-111">Indicates a cold start trap.</span></span> <span data-ttu-id="b508b-112">L'agente sta inizializzando le entità di protocollo in modalità gestita.</span><span class="sxs-lookup"><span data-stu-id="b508b-112">The agent is initializing protocol entities on the managed mode.</span></span> <span data-ttu-id="b508b-113">Potrebbe modificare gli oggetti nella relativa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b508b-113">It may alter objects in its view.</span></span><br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <span data-ttu-id="b508b-114"><dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-114"><dt>**SNMP\_GENERICTRAP\_WARMSTART**</dt></span></span> </dl>             | <span data-ttu-id="b508b-115">Indica una trap di avvio a caldo.</span><span class="sxs-lookup"><span data-stu-id="b508b-115">Indicates a warm start trap.</span></span> <span data-ttu-id="b508b-116">L'agente viene reinizializzato, ma non modifica gli oggetti nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b508b-116">The agent is reinitializing itself but it will not alter objects in its view.</span></span><br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <span data-ttu-id="b508b-117"><dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-117"><dt>**SNMP\_GENERICTRAP\_LINKDOWN**</dt></span></span> </dl>                | <span data-ttu-id="b508b-118">Indica un trap di collegamento.</span><span class="sxs-lookup"><span data-stu-id="b508b-118">Indicates a link-down trap.</span></span> <span data-ttu-id="b508b-119">Un'interfaccia collegata è cambiata dallo stato attivo allo stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="b508b-119">An attached interface has changed from the up state to the down state.</span></span> <span data-ttu-id="b508b-120">La prima variabile nell'elenco delle associazioni variabili identifica l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b508b-120">The first variable in the variable bindings list identifies the interface.</span></span><br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <span data-ttu-id="b508b-121"><dt>**SNMP \_ GENERICTRAP \_ LINKUP**</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-121"><dt>**SNMP\_GENERICTRAP\_LINKUP**</dt></span></span> </dl>                      | <span data-ttu-id="b508b-122">Indica una trap di collegamento.</span><span class="sxs-lookup"><span data-stu-id="b508b-122">Indicates a link-up trap.</span></span> <span data-ttu-id="b508b-123">Un'interfaccia collegata è cambiata dall'inizio fino allo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b508b-123">An attached interface has changed from the down start to the up state.</span></span> <span data-ttu-id="b508b-124">La prima variabile nell'elenco delle associazioni variabili identifica l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b508b-124">The first variable in the variable bindings list identifies the interface.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <span data-ttu-id="b508b-125"><dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-125"><dt>**SNMP\_GENERICTRAP\_AUTHFAILURE**</dt></span></span> </dl>       | <span data-ttu-id="b508b-126">Indica una trap di errore di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b508b-126">Indicates an authentication failure trap.</span></span> <span data-ttu-id="b508b-127">Un messaggio SNMP è stato inviato da un'entità SNMP, ma è stato erroneamente richiesto di appartenere a una community nota.</span><span class="sxs-lookup"><span data-stu-id="b508b-127">An SNMP entity has sent an SNMP message, but it has falsely claimed to belong to a known community.</span></span><br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <span data-ttu-id="b508b-128"><dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-128"><dt>**SNMP\_GENERICTRAP\_EGPNEIGHLOSS**</dt></span></span> </dl>    | <span data-ttu-id="b508b-129">Indica un trap di perdita Neighbor EGP.</span><span class="sxs-lookup"><span data-stu-id="b508b-129">Indicates an EGP neighbor loss trap.</span></span> <span data-ttu-id="b508b-130">Un peer EGP è stato modificato in stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="b508b-130">An EGP peer has changed to the down state.</span></span> <span data-ttu-id="b508b-131">La prima variabile nell'elenco Binding variabili identifica l'indirizzo IP del peer EGP.</span><span class="sxs-lookup"><span data-stu-id="b508b-131">The first variable in the variable bindings list identifies the IP address of the EGP peer.</span></span><br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <span data-ttu-id="b508b-132"><dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-132"><dt>**SNMP\_GENERICTRAP\_ENTERSPECIFIC**</dt></span></span> </dl> | <span data-ttu-id="b508b-133">Indica una trap specifica dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b508b-133">Indicates an enterprise-specific trap.</span></span> <span data-ttu-id="b508b-134">Si è verificato un evento straordinario.</span><span class="sxs-lookup"><span data-stu-id="b508b-134">An extraordinary event has occurred.</span></span> <span data-ttu-id="b508b-135">Viene identificato nel parametro *specificTrap* con un valore specifico dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b508b-135">It is identified in the *specificTrap* parameter with an enterprise-specific value.</span></span><br/>               |



## <a name="requirements"></a><span data-ttu-id="b508b-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b508b-136">Requirements</span></span>



| <span data-ttu-id="b508b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b508b-137">Requirement</span></span> | <span data-ttu-id="b508b-138">Valore</span><span class="sxs-lookup"><span data-stu-id="b508b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b508b-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b508b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b508b-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b508b-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="b508b-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b508b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b508b-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b508b-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b508b-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b508b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b508b-144"><dt>SNMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b508b-144"><dt>Snmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b508b-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b508b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b508b-146">Panoramica del protocollo Simple Network Management Protocol (SNMP)</span><span class="sxs-lookup"><span data-stu-id="b508b-146">Simple Network Management Protocol (SNMP) Overview</span></span>](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[<span data-ttu-id="b508b-147">Riferimento SNMP</span><span class="sxs-lookup"><span data-stu-id="b508b-147">SNMP Reference</span></span>](snmp-reference.md)
</dt> <dt>

[<span data-ttu-id="b508b-148">Costanti SNMP</span><span class="sxs-lookup"><span data-stu-id="b508b-148">SNMP Constants</span></span>](snmp-constants.md)
</dt> </dl>

 

