---
description: Il tipo di dati data/ora include l'ora e la data archiviate singolarmente, usando interi senza segno come campi di bit, compressi come indicato di seguito.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Data/ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313326"
---
# <a name="timedate"></a><span data-ttu-id="706ff-103">Data/ora</span><span class="sxs-lookup"><span data-stu-id="706ff-103">Time/Date</span></span>

<span data-ttu-id="706ff-104">Il tipo di dati data/ora include l'ora e la data archiviate singolarmente, usando interi senza segno come campi di bit, compressi come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="706ff-104">The Time/Date data type has the time and the date stored individually, using unsigned integers as bit fields, packed as follows.</span></span>

## <a name="time"></a><span data-ttu-id="706ff-105">Tempo</span><span class="sxs-lookup"><span data-stu-id="706ff-105">Time</span></span>

<span data-ttu-id="706ff-106">L'ora è codificata in un intero senza segno a 2 byte con i seguenti campi di bit.</span><span class="sxs-lookup"><span data-stu-id="706ff-106">Time is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="706ff-107">Contenuto</span><span class="sxs-lookup"><span data-stu-id="706ff-107">Contents</span></span>           | <span data-ttu-id="706ff-108">BITS</span><span class="sxs-lookup"><span data-stu-id="706ff-108">Bits</span></span>        | <span data-ttu-id="706ff-109">Intervallo di valori</span><span class="sxs-lookup"><span data-stu-id="706ff-109">Value range</span></span> |
|--------------------|-------------|-------------|
| <span data-ttu-id="706ff-110">ore</span><span class="sxs-lookup"><span data-stu-id="706ff-110">hours</span></span>              | <span data-ttu-id="706ff-111">0 1 2 3 4</span><span class="sxs-lookup"><span data-stu-id="706ff-111">0 1 2 3 4</span></span>   | <span data-ttu-id="706ff-112">0–23</span><span class="sxs-lookup"><span data-stu-id="706ff-112">0–23</span></span>        |
| <span data-ttu-id="706ff-113">minutes</span><span class="sxs-lookup"><span data-stu-id="706ff-113">minutes</span></span>            | <span data-ttu-id="706ff-114">5 6 7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="706ff-114">5 6 7 8 9 A</span></span> | <span data-ttu-id="706ff-115">0–59</span><span class="sxs-lookup"><span data-stu-id="706ff-115">0–59</span></span>        |
| <span data-ttu-id="706ff-116">intervalli di 2 secondi</span><span class="sxs-lookup"><span data-stu-id="706ff-116">2-second intervals</span></span> | <span data-ttu-id="706ff-117">B C D E F</span><span class="sxs-lookup"><span data-stu-id="706ff-117">B C D E F</span></span>   | <span data-ttu-id="706ff-118">0 – 29</span><span class="sxs-lookup"><span data-stu-id="706ff-118">0–29</span></span>        |



 

## <a name="date"></a><span data-ttu-id="706ff-119">Data</span><span class="sxs-lookup"><span data-stu-id="706ff-119">Date</span></span>

<span data-ttu-id="706ff-120">La data è codificata in un intero senza segno a 2 byte con i campi di bit seguenti.</span><span class="sxs-lookup"><span data-stu-id="706ff-120">Date is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="706ff-121">Contenuto</span><span class="sxs-lookup"><span data-stu-id="706ff-121">Contents</span></span> | <span data-ttu-id="706ff-122">BITS</span><span class="sxs-lookup"><span data-stu-id="706ff-122">Bits</span></span>          | <span data-ttu-id="706ff-123">Intervallo di valori</span><span class="sxs-lookup"><span data-stu-id="706ff-123">Value range</span></span>              |
|----------|---------------|--------------------------|
| <span data-ttu-id="706ff-124">anno</span><span class="sxs-lookup"><span data-stu-id="706ff-124">year</span></span>     | <span data-ttu-id="706ff-125">0 1 2 3 4 5 6</span><span class="sxs-lookup"><span data-stu-id="706ff-125">0 1 2 3 4 5 6</span></span> | <span data-ttu-id="706ff-126">0 – 119 (relativo a 1980)</span><span class="sxs-lookup"><span data-stu-id="706ff-126">0–119 (relative to 1980)</span></span> |
| <span data-ttu-id="706ff-127">month</span><span class="sxs-lookup"><span data-stu-id="706ff-127">month</span></span>    | <span data-ttu-id="706ff-128">7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="706ff-128">7 8 9 A</span></span>       | <span data-ttu-id="706ff-129">1–12</span><span class="sxs-lookup"><span data-stu-id="706ff-129">1–12</span></span>                     |
| <span data-ttu-id="706ff-130">day</span><span class="sxs-lookup"><span data-stu-id="706ff-130">day</span></span>      | <span data-ttu-id="706ff-131">B C D E F</span><span class="sxs-lookup"><span data-stu-id="706ff-131">B C D E F</span></span>     | <span data-ttu-id="706ff-132">1–31</span><span class="sxs-lookup"><span data-stu-id="706ff-132">1–31</span></span>                     |



 

 

 



