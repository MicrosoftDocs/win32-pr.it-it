---
description: Tipi di dati per i metodi di archiviazione protetti.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Tipi PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328177"
---
# <a name="pstore-types"></a><span data-ttu-id="0201f-103">Tipi PStore</span><span class="sxs-lookup"><span data-stu-id="0201f-103">PStore Types</span></span>

<span data-ttu-id="0201f-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0201f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0201f-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0201f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0201f-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0201f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0201f-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0201f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0201f-108">Tipi di dati per i metodi di archiviazione protetti.</span><span class="sxs-lookup"><span data-stu-id="0201f-108">The data types for Protected Storage methods.</span></span>


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

<span data-ttu-id="0201f-109">**\_ACCESSMODE PST**</span><span class="sxs-lookup"><span data-stu-id="0201f-109">**PST\_ACCESSMODE**</span></span>
</dt> <dd>

<span data-ttu-id="0201f-110">Definisce la modalità di lettura o scrittura della regola di accesso.</span><span class="sxs-lookup"><span data-stu-id="0201f-110">Defines the read or write mode of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="0201f-111">**\_ACCESSCLAUSETYPE PST**</span><span class="sxs-lookup"><span data-stu-id="0201f-111">**PST\_ACCESSCLAUSETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="0201f-112">Definisce il tipo di clausola della regola di accesso.</span><span class="sxs-lookup"><span data-stu-id="0201f-112">Defines the clause type of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="0201f-113">**\_chiave PST**</span><span class="sxs-lookup"><span data-stu-id="0201f-113">**PST\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="0201f-114">Definisce la chiave per l'elemento archiviato.</span><span class="sxs-lookup"><span data-stu-id="0201f-114">Defines the key for the stored item.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0201f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0201f-115">Requirements</span></span>



| <span data-ttu-id="0201f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0201f-116">Requirement</span></span> | <span data-ttu-id="0201f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0201f-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0201f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0201f-118">Header</span></span><br/> | <dl> <span data-ttu-id="0201f-119"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0201f-119"><dt>Pstore.h</dt></span></span> </dl> |



 

 
