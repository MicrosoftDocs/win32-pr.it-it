---
description: Identifica il set di regole di accesso per i dati di archiviazione protetti.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: Struttura PST_ACCESSRULESET (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331341"
---
# <a name="pst_accessruleset-structure"></a><span data-ttu-id="08786-103">\_Struttura ACCESSRULESET PST</span><span class="sxs-lookup"><span data-stu-id="08786-103">PST\_ACCESSRULESET structure</span></span>

<span data-ttu-id="08786-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="08786-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="08786-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="08786-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="08786-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="08786-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="08786-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="08786-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="08786-108">Identifica il set di regole di accesso per i dati di archiviazione protetti.</span><span class="sxs-lookup"><span data-stu-id="08786-108">Identifies the set of access rules for the protected storage data.</span></span>

## <a name="syntax"></a><span data-ttu-id="08786-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08786-109">Syntax</span></span>


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a><span data-ttu-id="08786-110">Members</span><span class="sxs-lookup"><span data-stu-id="08786-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="08786-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="08786-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="08786-112">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="08786-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="08786-113">**cRules**</span><span class="sxs-lookup"><span data-stu-id="08786-113">**cRules**</span></span>
</dt> <dd>

<span data-ttu-id="08786-114">Numero di regole nella matrice **rgRules** .</span><span class="sxs-lookup"><span data-stu-id="08786-114">The number of rules in the **rgRules** array.</span></span>

</dd> <dt>

<span data-ttu-id="08786-115">**rgRules**</span><span class="sxs-lookup"><span data-stu-id="08786-115">**rgRules**</span></span>
</dt> <dd>

<span data-ttu-id="08786-116">Puntatore a una matrice di strutture [**\_ ACCESSRULE PST**](pst-accessrule.md) .</span><span class="sxs-lookup"><span data-stu-id="08786-116">A pointer to an array of [**PST\_ACCESSRULE**](pst-accessrule.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08786-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08786-117">Requirements</span></span>



| <span data-ttu-id="08786-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="08786-118">Requirement</span></span> | <span data-ttu-id="08786-119">Valore</span><span class="sxs-lookup"><span data-stu-id="08786-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08786-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08786-120">Header</span></span><br/> | <dl> <span data-ttu-id="08786-121"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="08786-121"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08786-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08786-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08786-123">**\_ACCESSRULE PST**</span><span class="sxs-lookup"><span data-stu-id="08786-123">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> <dt>

[<span data-ttu-id="08786-124">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="08786-124">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> </dl>

 

 
