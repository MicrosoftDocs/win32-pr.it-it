---
description: Contiene informazioni sulla clausola Access per l'archiviazione protetta.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: Struttura PST_ACCESSCLAUSE (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325199"
---
# <a name="pst_accessclause-structure"></a><span data-ttu-id="f1e56-103">\_Struttura ACCESSCLAUSE PST</span><span class="sxs-lookup"><span data-stu-id="f1e56-103">PST\_ACCESSCLAUSE structure</span></span>

<span data-ttu-id="f1e56-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f1e56-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f1e56-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f1e56-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f1e56-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="f1e56-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f1e56-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f1e56-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f1e56-108">Contiene informazioni sulla clausola Access per l'archiviazione protetta.</span><span class="sxs-lookup"><span data-stu-id="f1e56-108">Contains information about the access clause for the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e56-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1e56-109">Syntax</span></span>


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a><span data-ttu-id="f1e56-110">Members</span><span class="sxs-lookup"><span data-stu-id="f1e56-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1e56-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="f1e56-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f1e56-112">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="f1e56-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="f1e56-113">**ClauseType**</span><span class="sxs-lookup"><span data-stu-id="f1e56-113">**ClauseType**</span></span>
</dt> <dd>

<span data-ttu-id="f1e56-114">Tipo di dati a cui fa riferimento il membro **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="f1e56-114">The type of data that is pointed to by the **pbClauseData** member.</span></span> <span data-ttu-id="f1e56-115">Per altre informazioni, vedere [**tipi di PStore**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="f1e56-115">For more information, see [**PStore Types**](pstore-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1e56-116">**cbClauseData**</span><span class="sxs-lookup"><span data-stu-id="f1e56-116">**cbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="f1e56-117">Dimensione dei dati a cui fa riferimento il membro **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="f1e56-117">The size of the data that is pointed to by the **pbClauseData** member.</span></span>

</dd> <dt>

<span data-ttu-id="f1e56-118">**pbClauseData**</span><span class="sxs-lookup"><span data-stu-id="f1e56-118">**pbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="f1e56-119">Puntatore ai dati della clausola di accesso.</span><span class="sxs-lookup"><span data-stu-id="f1e56-119">A pointer to the access clause data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1e56-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1e56-120">Requirements</span></span>



| <span data-ttu-id="f1e56-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e56-121">Requirement</span></span> | <span data-ttu-id="f1e56-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e56-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e56-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1e56-123">Header</span></span><br/> | <dl> <span data-ttu-id="f1e56-124"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1e56-124"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e56-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1e56-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e56-126">**\_ACCESSRULE PST**</span><span class="sxs-lookup"><span data-stu-id="f1e56-126">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> </dl>

 

 
