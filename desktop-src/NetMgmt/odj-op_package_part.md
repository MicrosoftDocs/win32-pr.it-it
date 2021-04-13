---
title: OP_PACKAGE_PART
description: Definizione di OP_PACKAGE_PART IDL
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "104224570"
---
# <a name="op_package_part-structure"></a><span data-ttu-id="d84f6-103">Struttura OP_PACKAGE_PART</span><span class="sxs-lookup"><span data-stu-id="d84f6-103">OP_PACKAGE_PART structure</span></span>

<span data-ttu-id="d84f6-104">Definisce una struttura che contiene un set di dati identificato da un GUID.</span><span class="sxs-lookup"><span data-stu-id="d84f6-104">Defines a structure that contains a data set identified by a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="d84f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d84f6-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a><span data-ttu-id="d84f6-106">Members</span><span class="sxs-lookup"><span data-stu-id="d84f6-106">Members</span></span>

### <a name="parttype"></a><span data-ttu-id="d84f6-107">PartType</span><span class="sxs-lookup"><span data-stu-id="d84f6-107">PartType</span></span>

<span data-ttu-id="d84f6-108">Identifica la struttura serializzata contenuta nella parte per la tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="d84f6-108">Identifies the serialized structure contained in Part per the following table:</span></span>

|<span data-ttu-id="d84f6-109">PartType</span><span class="sxs-lookup"><span data-stu-id="d84f6-109">PartType</span></span>|<span data-ttu-id="d84f6-110">Significato</span><span class="sxs-lookup"><span data-stu-id="d84f6-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="d84f6-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span><span class="sxs-lookup"><span data-stu-id="d84f6-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span></span>|<span data-ttu-id="d84f6-112">Contiene una struttura di ODJ_WIN7_BLOB serializzata.</span><span class="sxs-lookup"><span data-stu-id="d84f6-112">Contains a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="d84f6-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span><span class="sxs-lookup"><span data-stu-id="d84f6-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span></span>|<span data-ttu-id="d84f6-114">Contiene una struttura di OP_JOIN_PROV2_PART serializzata.</span><span class="sxs-lookup"><span data-stu-id="d84f6-114">Contains a serialized OP_JOIN_PROV2_PART structure.</span></span>|
|<span data-ttu-id="d84f6-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span><span class="sxs-lookup"><span data-stu-id="d84f6-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span></span>|<span data-ttu-id="d84f6-116">Contiene una struttura di OP_JOIN_PROV3_PART serializzata.</span><span class="sxs-lookup"><span data-stu-id="d84f6-116">Contains a serialized OP_JOIN_PROV3_PART structure.</span></span>|
|<span data-ttu-id="d84f6-117">GUID_CERT_PROVIDER {9c0971e9-832F-4873-8e87-ef1419d4781e}</span><span class="sxs-lookup"><span data-stu-id="d84f6-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span></span>|<span data-ttu-id="d84f6-118">Contiene una struttura di OP_CERT_PART serializzata.</span><span class="sxs-lookup"><span data-stu-id="d84f6-118">Contains a serialized OP_CERT_PART structure.</span></span>|
|<span data-ttu-id="d84f6-119">GUID_POLICY_PROVIDER {68fb602a-0C09-48ce-b75f-07b7bd58f7ec}</span><span class="sxs-lookup"><span data-stu-id="d84f6-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span></span>|<span data-ttu-id="d84f6-120">Contiene una struttura di OP_POLICY_PART serializzata.</span><span class="sxs-lookup"><span data-stu-id="d84f6-120">Contains a serialized OP_POLICY_PART structure.</span></span>|

### <a name="ulflags"></a><span data-ttu-id="d84f6-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="d84f6-121">ulFlags</span></span>

<span data-ttu-id="d84f6-122">Deve essere impostato su zero o più dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="d84f6-122">Must be set to zero or more of the following flags:</span></span>

|<span data-ttu-id="d84f6-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d84f6-123">Value</span></span>|<span data-ttu-id="d84f6-124">Significato</span><span class="sxs-lookup"><span data-stu-id="d84f6-124">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="d84f6-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d84f6-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span></span>|<span data-ttu-id="d84f6-126">Questa parte del pacchetto è considerata essenziale.</span><span class="sxs-lookup"><span data-stu-id="d84f6-126">This package part is considered essential.</span></span> <span data-ttu-id="d84f6-127">Se il consumer non riconosce questa parte del pacchetto o non è in grado di elaborarla correttamente, l'operazione complessiva deve avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d84f6-127">If the consumer does not recognize this package part or fails to successfully process it, the overall operation must fail.</span></span>|

### <a name="part"></a><span data-ttu-id="d84f6-128">Parte</span><span class="sxs-lookup"><span data-stu-id="d84f6-128">Part</span></span>

<span data-ttu-id="d84f6-129">Contiene una struttura serializzata in una struttura OP_BLOB.</span><span class="sxs-lookup"><span data-stu-id="d84f6-129">Contains a serialized structure in an OP_BLOB structure.</span></span> <span data-ttu-id="d84f6-130">La struttura specifica è determinata da PartType.</span><span class="sxs-lookup"><span data-stu-id="d84f6-130">The specific structure is determined by PartType.</span></span>

### <a name="extension"></a><span data-ttu-id="d84f6-131">Estensione</span><span class="sxs-lookup"><span data-stu-id="d84f6-131">Extension</span></span>

<span data-ttu-id="d84f6-132">Riservato per utilizzi futuri e deve essere impostato su tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="d84f6-132">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="d84f6-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d84f6-133">See also</span></span>

[<span data-ttu-id="d84f6-134">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="d84f6-134">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="d84f6-135">**\_BLOB op**</span><span class="sxs-lookup"><span data-stu-id="d84f6-135">**OP\_BLOB**</span></span>](odj-op_blob.md)
