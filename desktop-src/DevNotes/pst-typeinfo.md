---
description: Descrive un tipo o un sottotipo.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: Struttura PST_TYPEINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331714"
---
# <a name="pst_typeinfo-structure"></a><span data-ttu-id="76441-103">\_Struttura TYPEINFO PST</span><span class="sxs-lookup"><span data-stu-id="76441-103">PST\_TYPEINFO structure</span></span>

<span data-ttu-id="76441-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76441-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="76441-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="76441-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="76441-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="76441-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="76441-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="76441-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="76441-108">Descrive un tipo o un sottotipo.</span><span class="sxs-lookup"><span data-stu-id="76441-108">Describes a type or a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="76441-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76441-109">Syntax</span></span>


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="76441-110">Members</span><span class="sxs-lookup"><span data-stu-id="76441-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="76441-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="76441-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="76441-112">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="76441-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="76441-113">**szDisplayName**</span><span class="sxs-lookup"><span data-stu-id="76441-113">**szDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="76441-114">Puntatore a una stringa di caratteri wide che rappresenta il nome visualizzato per il tipo.</span><span class="sxs-lookup"><span data-stu-id="76441-114">A pointer to a wide character string that represents the display name for the type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76441-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76441-115">Requirements</span></span>



| <span data-ttu-id="76441-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="76441-116">Requirement</span></span> | <span data-ttu-id="76441-117">Valore</span><span class="sxs-lookup"><span data-stu-id="76441-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="76441-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76441-118">Header</span></span><br/> | <dl> <span data-ttu-id="76441-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="76441-119"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76441-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76441-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76441-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="76441-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> <dt>

[<span data-ttu-id="76441-122">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="76441-122">**CreateType**</span></span>](ipstore-createtype.md)
</dt> <dt>

[<span data-ttu-id="76441-123">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="76441-123">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)
</dt> <dt>

[<span data-ttu-id="76441-124">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="76441-124">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
