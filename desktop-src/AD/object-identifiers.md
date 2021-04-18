---
title: Identificatori di oggetto (AD DS)
description: Gli identificatori di oggetto (OID) sono valori numerici univoci emessi da varie autorità emittenti per identificare in modo univoco elementi dati, sintassi e altre parti di applicazioni distribuite.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificatori di oggetto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "106299325"
---
# <a name="object-identifiers-ad-ds"></a><span data-ttu-id="17635-104">Identificatori di oggetto (AD DS)</span><span class="sxs-lookup"><span data-stu-id="17635-104">Object Identifiers (AD DS)</span></span>

<span data-ttu-id="17635-105">Gli identificatori di oggetto (OID) sono valori numerici univoci emessi da varie autorità emittenti per identificare in modo univoco elementi dati, sintassi e altre parti di applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="17635-105">Object Identifiers (OIDs) are unique numeric values issued by various issuing authorities to uniquely identify data elements, syntaxes, and other parts of distributed applications.</span></span> <span data-ttu-id="17635-106">OID si trovano in applicazioni OSI, directory X. 500, SNMP e altre applicazioni in cui l'unicità è importante.</span><span class="sxs-lookup"><span data-stu-id="17635-106">OIDs are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="17635-107">OID sono basati su una struttura ad albero, in cui un'autorità emittente superiore, ad esempio l'immagine ISO, alloca un ramo della struttura ad albero a una sottoautorizzazione, che a sua volta può allocare sottorami.</span><span class="sxs-lookup"><span data-stu-id="17635-107">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a subauthority, who in turn can allocate subbranches.</span></span>

<span data-ttu-id="17635-108">Il protocollo LDAP (RFC 2251) richiede un servizio directory per identificare classi di oggetti, attributi e sintassi con OID.</span><span class="sxs-lookup"><span data-stu-id="17635-108">The LDAP protocol (RFC 2251) requires a directory service to identify object classes, attributes, and syntaxes with OIDs.</span></span> <span data-ttu-id="17635-109">Questa operazione fa parte dell'Legacy X. 500 LDAP.</span><span class="sxs-lookup"><span data-stu-id="17635-109">This is part of the LDAP X.500 legacy.</span></span>

<span data-ttu-id="17635-110">OID in Active Directory Domain Services includono alcuni rilasciati dall'ISO per le classi e gli attributi X. 500 e alcuni emessi da Microsoft e da altre autorità emittenti.</span><span class="sxs-lookup"><span data-stu-id="17635-110">OIDs in Active Directory Domain Services include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft and other issuing authorities.</span></span> <span data-ttu-id="17635-111">La notazione OID è una stringa punteggiata di numeri, ad esempio "1.2.840.113556.1.5.9", descritta nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="17635-111">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.9", which is described in the following table.</span></span>



| <span data-ttu-id="17635-112">Valore</span><span class="sxs-lookup"><span data-stu-id="17635-112">Value</span></span>  | <span data-ttu-id="17635-113">Significato</span><span class="sxs-lookup"><span data-stu-id="17635-113">Meaning</span></span>          | <span data-ttu-id="17635-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17635-114">Description</span></span>                                              |
|--------|------------------|----------------------------------------------------------|
| <span data-ttu-id="17635-115">1</span><span class="sxs-lookup"><span data-stu-id="17635-115">1</span></span>      | <span data-ttu-id="17635-116">ISO</span><span class="sxs-lookup"><span data-stu-id="17635-116">ISO</span></span>              | <span data-ttu-id="17635-117">Identifica l'autorità radice.</span><span class="sxs-lookup"><span data-stu-id="17635-117">Identifies the root authority.</span></span>                           |
| <span data-ttu-id="17635-118">2</span><span class="sxs-lookup"><span data-stu-id="17635-118">2</span></span>      | <span data-ttu-id="17635-119">ANSI</span><span class="sxs-lookup"><span data-stu-id="17635-119">ANSI</span></span>             | <span data-ttu-id="17635-120">Designazione del gruppo assegnata da ISO.</span><span class="sxs-lookup"><span data-stu-id="17635-120">Group designation assigned by ISO.</span></span>                       |
| <span data-ttu-id="17635-121">840</span><span class="sxs-lookup"><span data-stu-id="17635-121">840</span></span>    | <span data-ttu-id="17635-122">USA</span><span class="sxs-lookup"><span data-stu-id="17635-122">USA</span></span>              | <span data-ttu-id="17635-123">Designazione del paese/area geografica assegnata dal gruppo.</span><span class="sxs-lookup"><span data-stu-id="17635-123">Country/region designation assigned by the group.</span></span>        |
| <span data-ttu-id="17635-124">113556</span><span class="sxs-lookup"><span data-stu-id="17635-124">113556</span></span> | <span data-ttu-id="17635-125">Microsoft</span><span class="sxs-lookup"><span data-stu-id="17635-125">Microsoft</span></span>        | <span data-ttu-id="17635-126">Designazione dell'organizzazione assegnata dal paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="17635-126">Organization designation assigned by the country/region.</span></span> |
| <span data-ttu-id="17635-127">1</span><span class="sxs-lookup"><span data-stu-id="17635-127">1</span></span>      | <span data-ttu-id="17635-128">Active Directory</span><span class="sxs-lookup"><span data-stu-id="17635-128">Active Directory</span></span> | <span data-ttu-id="17635-129">Assegnati dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="17635-129">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="17635-130">5</span><span class="sxs-lookup"><span data-stu-id="17635-130">5</span></span>      | <span data-ttu-id="17635-131">Classi</span><span class="sxs-lookup"><span data-stu-id="17635-131">Classes</span></span>          | <span data-ttu-id="17635-132">Assegnati dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="17635-132">Assigned by the organization.</span></span>                            |
| <span data-ttu-id="17635-133">9</span><span class="sxs-lookup"><span data-stu-id="17635-133">9</span></span>      | <span data-ttu-id="17635-134">classe **User**</span><span class="sxs-lookup"><span data-stu-id="17635-134">**user** class</span></span>   | <span data-ttu-id="17635-135">Assegnati dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="17635-135">Assigned by the organization.</span></span>                            |



 

<span data-ttu-id="17635-136">Per ulteriori informazioni e per una descrizione di due procedure utilizzate per ottenere OID validi da usare per l'estensione dello schema di Active Directory, vedere [ottenere un identificatore di oggetto](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="17635-136">For more information, and a discussion of two procedures used to obtain valid OIDs for use in extending the Active Directory schema, see [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>

 

 




