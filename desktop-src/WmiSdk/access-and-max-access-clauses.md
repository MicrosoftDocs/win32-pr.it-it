---
description: Ogni definizione di oggetto MIB contiene una clausola ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) che definisce i diritti di accesso all'oggetto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Clausole ACCESS e MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315253"
---
# <a name="access-and-max-access-clauses"></a><span data-ttu-id="fab1c-103">Clausole ACCESS e MAX-ACCESS</span><span class="sxs-lookup"><span data-stu-id="fab1c-103">ACCESS and MAX-ACCESS Clauses</span></span>

<span data-ttu-id="fab1c-104">Ogni definizione di oggetto MIB contiene una clausola ACCESS (SNMPv1) o MAX-ACCESS (SNMPv2C) che definisce i diritti di accesso all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fab1c-104">Each MIB object definition contains either an ACCESS (SNMPv1) or MAX-ACCESS (SNMPv2C) clause that defines the access rights to the object.</span></span>

> [!Note]  
> <span data-ttu-id="fab1c-105">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fab1c-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="fab1c-106">Nella tabella seguente viene elencato il mapping della clausola SNMPv1 ACCESS.</span><span class="sxs-lookup"><span data-stu-id="fab1c-106">The following table lists the mapping of the SNMPv1 ACCESS clause.</span></span>



| <span data-ttu-id="fab1c-107">Clausola di accesso MIB</span><span class="sxs-lookup"><span data-stu-id="fab1c-107">MIB ACCESS clause</span></span> | <span data-ttu-id="fab1c-108">Qualificatore CIM</span><span class="sxs-lookup"><span data-stu-id="fab1c-108">CIM qualifier</span></span>       |
|-------------------|---------------------|
| <span data-ttu-id="fab1c-109">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="fab1c-109">read-only</span></span>         | <span data-ttu-id="fab1c-110">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="fab1c-110">**Read**</span></span>            |
| <span data-ttu-id="fab1c-111">lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fab1c-111">read-write</span></span>        | <span data-ttu-id="fab1c-112">**Lettura**, **scrittura**</span><span class="sxs-lookup"><span data-stu-id="fab1c-112">**Read**, **Write**</span></span> |
| <span data-ttu-id="fab1c-113">sola scrittura</span><span class="sxs-lookup"><span data-stu-id="fab1c-113">write-only</span></span>        | <span data-ttu-id="fab1c-114">**Scrittura**</span><span class="sxs-lookup"><span data-stu-id="fab1c-114">**Write**</span></span>           |
| <span data-ttu-id="fab1c-115">non accessibile</span><span class="sxs-lookup"><span data-stu-id="fab1c-115">not-accessible</span></span>    | <span data-ttu-id="fab1c-116">**Non \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="fab1c-116">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="fab1c-117">La tabella seguente elenca il mapping della clausola SNMPv2C MAX-ACCESS.</span><span class="sxs-lookup"><span data-stu-id="fab1c-117">The following table lists the mapping of the SNMPv2C MAX-ACCESS clause.</span></span>



| <span data-ttu-id="fab1c-118">Clausola di accesso MIB</span><span class="sxs-lookup"><span data-stu-id="fab1c-118">MIB-ACCESS clause</span></span>     | <span data-ttu-id="fab1c-119">Qualificatore CIM</span><span class="sxs-lookup"><span data-stu-id="fab1c-119">CIM qualifier</span></span>       |
|-----------------------|---------------------|
| <span data-ttu-id="fab1c-120">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="fab1c-120">read-only</span></span>             | <span data-ttu-id="fab1c-121">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="fab1c-121">**Read**</span></span>            |
| <span data-ttu-id="fab1c-122">lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fab1c-122">read-write</span></span>            | <span data-ttu-id="fab1c-123">**Lettura**, **scrittura**</span><span class="sxs-lookup"><span data-stu-id="fab1c-123">**Read**, **Write**</span></span> |
| <span data-ttu-id="fab1c-124">lettura-creazione</span><span class="sxs-lookup"><span data-stu-id="fab1c-124">read-create</span></span>           | <span data-ttu-id="fab1c-125">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="fab1c-125">**Read**</span></span>            |
| <span data-ttu-id="fab1c-126">accessibilità per notifica</span><span class="sxs-lookup"><span data-stu-id="fab1c-126">accessible-for-notify</span></span> | <span data-ttu-id="fab1c-127">**Non \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="fab1c-127">**Not\_Accessible**</span></span> |
| <span data-ttu-id="fab1c-128">non accessibile</span><span class="sxs-lookup"><span data-stu-id="fab1c-128">not-accessible</span></span>        | <span data-ttu-id="fab1c-129">**Non \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="fab1c-129">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="fab1c-130">Quando un oggetto MIB viene mappato a non accessibile e non è una proprietà con chiave della classe, non esiste alcun mapping dell'oggetto MIB stesso.</span><span class="sxs-lookup"><span data-stu-id="fab1c-130">When a MIB object maps to not-accessible and is not a keyed property of the class, there is no mapping of the MIB object itself.</span></span>

 

 



