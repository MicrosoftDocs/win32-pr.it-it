---
title: Identificatori di oggetto (SNMP)
description: Un identificatore di oggetto SNMP assegna un nome univoco a un oggetto e ne identifica la posizione all'interno di una struttura ad albero MIB (Management Information Base).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739330"
---
# <a name="object-identifiers-snmp"></a><span data-ttu-id="624fc-103">Identificatori di oggetto (SNMP)</span><span class="sxs-lookup"><span data-stu-id="624fc-103">Object Identifiers (SNMP)</span></span>

<span data-ttu-id="624fc-104">Un identificatore di oggetto SNMP assegna un nome univoco a un oggetto e ne identifica la posizione all'interno di una struttura ad albero MIB (Management Information Base).</span><span class="sxs-lookup"><span data-stu-id="624fc-104">An SNMP object identifier uniquely names an object and identifies its location within a Management Information Base (MIB) tree structure.</span></span> <span data-ttu-id="624fc-105">Gli identificatori di oggetto sono tipi di dati (ASN. 1) indipendenti dall'applicazione che sono costituiti da una sequenza di numeri interi non negativi o sottoidentificatori.</span><span class="sxs-lookup"><span data-stu-id="624fc-105">Object identifiers are application-independent Abstract Syntax Notation One (ASN.1) data types that consist of a sequence of non-negative integers, or subidentifiers.</span></span> <span data-ttu-id="624fc-106">Gli identificatori di oggetto devono avere un minimo di due sottoidentificatori e non devono superare 128 sottoidentificatori.</span><span class="sxs-lookup"><span data-stu-id="624fc-106">Object identifiers must have a minimum of two subidentifiers and they must not exceed 128 subidentifiers.</span></span>

<span data-ttu-id="624fc-107">L'ambiente di programmazione WinSNMP utilizza la struttura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) per gestire gli identificatori di oggetto.</span><span class="sxs-lookup"><span data-stu-id="624fc-107">The WinSNMP programming environment uses the [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure to manage object identifiers.</span></span> <span data-ttu-id="624fc-108">Il formato della matrice di identificatori di oggetto in una struttura **smiOID** è un sottoidentificatore per ogni elemento di matrice.</span><span class="sxs-lookup"><span data-stu-id="624fc-108">The format of the object identifier array in an **smiOID** structure is one subidentifier per array element.</span></span>

<span data-ttu-id="624fc-109">La rappresentazione di stringa numerica punteggiata di un identificatore di oggetto separa i relativi sottoidentificatori con i punti; ad esempio, "1.2.3.4.5.6".</span><span class="sxs-lookup"><span data-stu-id="624fc-109">The dotted numeric string representation of an object identifier separates its subidentifiers with periods; for example, "1.2.3.4.5.6".</span></span>

<span data-ttu-id="624fc-110">Per ulteriori informazioni, vedere [SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) e le RFC pertinenti.</span><span class="sxs-lookup"><span data-stu-id="624fc-110">For more information, see [The SNMP Management Information Base (MIB)](the-snmp-management-information-base-mib-.md) and the relevant RFCs.</span></span>

 

 




