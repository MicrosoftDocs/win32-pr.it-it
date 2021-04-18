---
description: Indica il percorso di un archivio certificati.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Enumerazione CAPICOM_STORE_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331050"
---
# <a name="capicom_store_location-enumeration"></a><span data-ttu-id="cf2a9-103">\_Enumerazione percorso archivio CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="cf2a9-103">CAPICOM\_STORE\_LOCATION enumeration</span></span>

<span data-ttu-id="cf2a9-104">Il tipo di enumerazione del **\_ \_ percorso dell'archivio CAPICOM** indica il percorso di un [*archivio certificati*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cf2a9-104">The **CAPICOM\_STORE\_LOCATION** enumeration type indicates the location of a [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="cf2a9-105">Membri</span><span class="sxs-lookup"><span data-stu-id="cf2a9-105">Members</span></span>



| <span data-ttu-id="cf2a9-106">Membro</span><span class="sxs-lookup"><span data-stu-id="cf2a9-106">Member</span></span>                                      | <span data-ttu-id="cf2a9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf2a9-107">Description</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="cf2a9-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cf2a9-108">Value</span></span> |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="cf2a9-109">**\_Archivio di memoria CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="cf2a9-109">**CAPICOM\_MEMORY\_STORE**</span></span>                  | <span data-ttu-id="cf2a9-110">L'archivio è un archivio di memoria.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-110">The store is a memory store.</span></span> <span data-ttu-id="cf2a9-111">Eventuali modifiche apportate al contenuto dell'archivio non vengono rese permanente.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-111">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                              | <span data-ttu-id="cf2a9-112">0</span><span class="sxs-lookup"><span data-stu-id="cf2a9-112">0</span></span>     |
| <span data-ttu-id="cf2a9-113">**\_Archivio del computer locale \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="cf2a9-113">**CAPICOM\_LOCAL\_MACHINE\_STORE**</span></span>          | <span data-ttu-id="cf2a9-114">L'archivio è un archivio del computer locale.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-114">The store is a local machine store.</span></span> <span data-ttu-id="cf2a9-115">Gli archivi di computer locali possono essere archivi di lettura/scrittura solo se l'utente dispone di autorizzazioni di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-115">Local machine stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="cf2a9-116">Se l'utente dispone di autorizzazioni di lettura/scrittura e se l'archivio è aperto in lettura/scrittura, le modifiche apportate al contenuto dell'archivio vengono rese permanente.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-116">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> | <span data-ttu-id="cf2a9-117">1</span><span class="sxs-lookup"><span data-stu-id="cf2a9-117">1</span></span>     |
| <span data-ttu-id="cf2a9-118">**\_ \_ archivio utente corrente CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="cf2a9-118">**CAPICOM\_CURRENT\_USER\_STORE**</span></span>           | <span data-ttu-id="cf2a9-119">L'archivio è un archivio utente corrente.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-119">The store is a current user store.</span></span> <span data-ttu-id="cf2a9-120">Un archivio utente corrente può essere un archivio di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-120">A current user store may be a read/write store.</span></span> <span data-ttu-id="cf2a9-121">In caso contrario, le modifiche apportate al contenuto dell'archivio vengono rese permanente.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-121">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                      | <span data-ttu-id="cf2a9-122">2</span><span class="sxs-lookup"><span data-stu-id="cf2a9-122">2</span></span>     |
| <span data-ttu-id="cf2a9-123">**\_archivio utenti di Active \_ directory \_ di \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="cf2a9-123">**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</span></span> | <span data-ttu-id="cf2a9-124">L'archivio è un archivio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-124">The store is an Active Directory store.</span></span> <span data-ttu-id="cf2a9-125">Gli archivi di Active Directory possono essere aperti solo in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-125">Active Directory stores can be opened only in read-only mode.</span></span> <span data-ttu-id="cf2a9-126">I certificati non possono essere aggiunti o rimossi dagli archivi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-126">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                                                                                        | <span data-ttu-id="cf2a9-127">3</span><span class="sxs-lookup"><span data-stu-id="cf2a9-127">3</span></span>     |
| <span data-ttu-id="cf2a9-128">**\_ \_ \_ archivio utenti smart card \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="cf2a9-128">**CAPICOM\_SMART\_CARD\_USER\_STORE**</span></span>       | <span data-ttu-id="cf2a9-129">Gli archivi supportano gli archivi certificati basati su smart card.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-129">Stores support smart card–based certificate stores.</span></span> <span data-ttu-id="cf2a9-130">L'archivio è il gruppo di smart card presenti.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-130">The store is the group of present smart cards.</span></span> <span data-ttu-id="cf2a9-131">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="cf2a9-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                         | <span data-ttu-id="cf2a9-132">4</span><span class="sxs-lookup"><span data-stu-id="cf2a9-132">4</span></span>     |



## <a name="remarks"></a><span data-ttu-id="cf2a9-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf2a9-133">Remarks</span></span>

<span data-ttu-id="cf2a9-134">Il tipo di enumerazione del **\_ \_ percorso dell'archivio CAPICOM** viene usato dai metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf2a9-134">The **CAPICOM\_STORE\_LOCATION** enumeration type is used by the following methods:</span></span>

-   [<span data-ttu-id="cf2a9-135">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="cf2a9-135">**PrivateKey.Open**</span></span>](privatekey-open.md)
-   [<span data-ttu-id="cf2a9-136">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="cf2a9-136">**Store.Open**</span></span>](store-open.md)

## <a name="requirements"></a><span data-ttu-id="cf2a9-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cf2a9-137">Requirements</span></span>



| <span data-ttu-id="cf2a9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf2a9-138">Requirement</span></span> | <span data-ttu-id="cf2a9-139">Valore</span><span class="sxs-lookup"><span data-stu-id="cf2a9-139">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2a9-140">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cf2a9-140">Redistributable</span></span><br/> | <span data-ttu-id="cf2a9-141">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf2a9-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="cf2a9-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cf2a9-142">Header</span></span><br/>          | <dl> <span data-ttu-id="cf2a9-143"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf2a9-143"><dt>Capicom.h</dt></span></span> </dl> |



 

 
