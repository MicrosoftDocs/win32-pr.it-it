---
description: Descrive una regola per l'accesso agli elementi archiviati in un archivio protetto.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: Struttura PST_ACCESSRULE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331343"
---
# <a name="pst_accessrule-structure"></a><span data-ttu-id="3b7e3-103">\_Struttura ACCESSRULE PST</span><span class="sxs-lookup"><span data-stu-id="3b7e3-103">PST\_ACCESSRULE structure</span></span>

<span data-ttu-id="3b7e3-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="3b7e3-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="3b7e3-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="3b7e3-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="3b7e3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="3b7e3-108">Descrive una regola per l'accesso agli elementi archiviati in un archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-108">Describes a rule for access to items stored in protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b7e3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b7e3-109">Syntax</span></span>


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a><span data-ttu-id="3b7e3-110">Members</span><span class="sxs-lookup"><span data-stu-id="3b7e3-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="3b7e3-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="3b7e3-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="3b7e3-112">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="3b7e3-113">**AccessModeFlags**</span><span class="sxs-lookup"><span data-stu-id="3b7e3-113">**AccessModeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="3b7e3-114">Modalità di accesso a cui si riferisce un set specificato di clausole di accesso.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-114">The access modes to which a specified set of access clauses pertain.</span></span>



| <span data-ttu-id="3b7e3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3b7e3-115">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="3b7e3-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3b7e3-116">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="3b7e3-117"><dt>**Pst \_ Leggi**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="3b7e3-117"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="3b7e3-118">Modalità di accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-118">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="3b7e3-119"><dt>**Pst \_ Scrivi**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="3b7e3-119"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="3b7e3-120">Modalità di accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="3b7e3-120">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b7e3-121">**cClauses**</span><span class="sxs-lookup"><span data-stu-id="3b7e3-121">**cClauses**</span></span>
</dt> <dd>

<span data-ttu-id="3b7e3-122">Numero di strutture nella matrice **rgClauses** .</span><span class="sxs-lookup"><span data-stu-id="3b7e3-122">The number of structures in the **rgClauses** array.</span></span>

</dd> <dt>

<span data-ttu-id="3b7e3-123">**rgClauses**</span><span class="sxs-lookup"><span data-stu-id="3b7e3-123">**rgClauses**</span></span>
</dt> <dd>

<span data-ttu-id="3b7e3-124">Puntatore a una matrice di strutture [**\_ ACCESSCLAUSE PST**](pst-accessclause.md) .</span><span class="sxs-lookup"><span data-stu-id="3b7e3-124">A pointer to an array of [**PST\_ACCESSCLAUSE**](pst-accessclause.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b7e3-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b7e3-125">Requirements</span></span>



| <span data-ttu-id="3b7e3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b7e3-126">Requirement</span></span> | <span data-ttu-id="3b7e3-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3b7e3-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7e3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b7e3-128">Header</span></span><br/> | <dl> <span data-ttu-id="3b7e3-129"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b7e3-129"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b7e3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b7e3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b7e3-131">**\_ACCESSCLAUSE PST**</span><span class="sxs-lookup"><span data-stu-id="3b7e3-131">**PST\_ACCESSCLAUSE**</span></span>](pst-accessclause.md)
</dt> <dt>

[<span data-ttu-id="3b7e3-132">**\_ACCESSRULESET PST**</span><span class="sxs-lookup"><span data-stu-id="3b7e3-132">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> </dl>

 

 
