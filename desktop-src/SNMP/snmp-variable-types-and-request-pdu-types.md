---
title: Tipi di variabili SNMP e tipi PDU di richiesta
description: Le definizioni per alcuni tipi di variabile SNMP e i tipi di richiesta PDU sono state modificate. Il file SNMP. h esegue il mapping dei tipi obsoleti ai nuovi tipi corrispondenti.
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728954"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a><span data-ttu-id="738bd-104">Tipi di variabili SNMP e tipi PDU di richiesta</span><span class="sxs-lookup"><span data-stu-id="738bd-104">SNMP Variable Types and Request PDU Types</span></span>

<span data-ttu-id="738bd-105">\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="738bd-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="738bd-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="738bd-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="738bd-107">Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="738bd-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="738bd-108">Le definizioni per alcuni tipi di variabile SNMP e i tipi di richiesta PDU sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="738bd-108">The definitions for some SNMP variable types and request PDU types have changed.</span></span> <span data-ttu-id="738bd-109">Il file SNMP. h esegue il mapping dei tipi obsoleti ai nuovi tipi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="738bd-109">The Snmp.h file maps old types to the corresponding new types.</span></span>

## <a name="modified-snmp-variable-types"></a><span data-ttu-id="738bd-110">Tipi di variabili SNMP modificate</span><span class="sxs-lookup"><span data-stu-id="738bd-110">Modified SNMP Variable Types</span></span>

<span data-ttu-id="738bd-111">Quando si sviluppano applicazioni di gestione che usano l'API di gestione SNMP Microsoft, è consigliabile usare i nuovi tipi di variabili SNMP elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="738bd-111">You should use the new SNMP variable types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="738bd-112">La tabella elenca i tipi di variabili SNMP obsoleti con i nuovi tipi di variabile corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="738bd-112">The table lists the old SNMP variable types with the corresponding new variable types.</span></span>

| <span data-ttu-id="738bd-113">Tipo di variabile precedente</span><span class="sxs-lookup"><span data-stu-id="738bd-113">Old variable type</span></span>        | <span data-ttu-id="738bd-114">Nuovo tipo di variabile</span><span class="sxs-lookup"><span data-stu-id="738bd-114">New variable type</span></span> |
|--------------------------|-------------------|
| <span data-ttu-id="738bd-115">\_IPAddress RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-115">ASN\_RFC1155\_IPADDRESS</span></span>  | <span data-ttu-id="738bd-116">\_indirizzo IP ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-116">ASN\_IPADDRESS</span></span>    |
| <span data-ttu-id="738bd-117">\_Contatore RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-117">ASN\_RFC1155\_COUNTER</span></span>    | <span data-ttu-id="738bd-118">\_COUNTER32 ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-118">ASN\_COUNTER32</span></span>    |
| <span data-ttu-id="738bd-119">\_ \_ Misuratore RFC1155 ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-119">ASN\_RFC1155\_GAUGE</span></span>      | <span data-ttu-id="738bd-120">\_GAUGE32 ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-120">ASN\_GAUGE32</span></span>      |
| <span data-ttu-id="738bd-121">\_TimeTicks RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-121">ASN\_RFC1155\_TIMETICKS</span></span>  | <span data-ttu-id="738bd-122">\_TimeTicks ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-122">ASN\_TIMETICKS</span></span>    |
| <span data-ttu-id="738bd-123">\_Opaco RFC1155 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-123">ASN\_RFC1155\_OPAQUE</span></span>     | <span data-ttu-id="738bd-124">ASN \_ opaco</span><span class="sxs-lookup"><span data-stu-id="738bd-124">ASN\_OPAQUE</span></span>       |
| <span data-ttu-id="738bd-125">\_DISPSTRING RFC1213 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-125">ASN\_RFC1213\_DISPSTRING</span></span> | <span data-ttu-id="738bd-126">\_OCTETSTRING ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-126">ASN\_OCTETSTRING</span></span>  |



 

## <a name="modified-snmp-pdu-request-types"></a><span data-ttu-id="738bd-127">Tipi di richiesta PDU SNMP modificati</span><span class="sxs-lookup"><span data-stu-id="738bd-127">Modified SNMP PDU Request Types</span></span>

<span data-ttu-id="738bd-128">Quando si sviluppano applicazioni di gestione che usano l'API di gestione SNMP Microsoft, è necessario usare i nuovi tipi di PDU SNMP elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="738bd-128">You should use the new SNMP PDU types listed in the following table when you develop manager applications that use the Microsoft SNMP Management API.</span></span> <span data-ttu-id="738bd-129">La tabella elenca i vecchi tipi di PDU SNMP con i nuovi tipi PDU corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="738bd-129">The table lists the old SNMP PDU types with the corresponding new PDU types.</span></span>

| <span data-ttu-id="738bd-130">Tipo PDU precedente</span><span class="sxs-lookup"><span data-stu-id="738bd-130">Old PDU type</span></span>                 | <span data-ttu-id="738bd-131">Nuovo tipo PDU</span><span class="sxs-lookup"><span data-stu-id="738bd-131">New PDU type</span></span>        |
|------------------------------|---------------------|
| <span data-ttu-id="738bd-132">\_GetRequest RFC1157 ASN \_</span><span class="sxs-lookup"><span data-stu-id="738bd-132">ASN\_RFC1157\_GETREQUEST</span></span>     | <span data-ttu-id="738bd-133">\_Get SNMP PDU \_</span><span class="sxs-lookup"><span data-stu-id="738bd-133">SNMP\_PDU\_GET</span></span>      |
| <span data-ttu-id="738bd-134">\_GETNEXTREQUEST RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-134">ASN\_RFC1157\_GETNEXTREQUEST</span></span> | <span data-ttu-id="738bd-135">datanext di SNMP \_ PDU \_</span><span class="sxs-lookup"><span data-stu-id="738bd-135">SNMP\_PDU\_GETNEXT</span></span>  |
| <span data-ttu-id="738bd-136">\_GetResponse RFC1157 ASN \_</span><span class="sxs-lookup"><span data-stu-id="738bd-136">ASN\_RFC1157\_GETRESPONSE</span></span>    | <span data-ttu-id="738bd-137">\_risposta PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="738bd-137">SNMP\_PDU\_RESPONSE</span></span> |
| <span data-ttu-id="738bd-138">\_Richiesta RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-138">ASN\_RFC1157\_SETREQUEST</span></span>     | <span data-ttu-id="738bd-139">\_set PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="738bd-139">SNMP\_PDU\_SET</span></span>      |
| <span data-ttu-id="738bd-140">\_Trap RFC1157 \_ ASN</span><span class="sxs-lookup"><span data-stu-id="738bd-140">ASN\_RFC1157\_TRAP</span></span>           | <span data-ttu-id="738bd-141">\_V1TRAP PDU \_ SNMP</span><span class="sxs-lookup"><span data-stu-id="738bd-141">SNMP\_PDU\_V1TRAP</span></span>   |



 

 

 