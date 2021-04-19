---
description: Le costanti seguenti vengono utilizzate da PStore.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Costanti PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328183"
---
# <a name="pstore-constants"></a><span data-ttu-id="30470-103">Costanti PStore</span><span class="sxs-lookup"><span data-stu-id="30470-103">PStore Constants</span></span>

<span data-ttu-id="30470-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="30470-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="30470-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="30470-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="30470-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="30470-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="30470-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="30470-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="30470-108">Le costanti seguenti vengono utilizzate da PStore.</span><span class="sxs-lookup"><span data-stu-id="30470-108">The following constants are used by PStore.</span></span>

<span data-ttu-id="30470-109">Codici di errore di archiviazione protetta</span><span class="sxs-lookup"><span data-stu-id="30470-109">Protected Storage Error Codes</span></span>



| <span data-ttu-id="30470-110">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="30470-110">Constant/value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="30470-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30470-111">Description</span></span>                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <span data-ttu-id="30470-112"><dt>**Pst \_ E \_ OK**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="30470-112"><dt>**PST\_E\_OK**</dt> <dt>0x00000000L</dt></span></span> </dl>                             | <span data-ttu-id="30470-113">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="30470-113">The operation was successful.</span></span><br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <span data-ttu-id="30470-114"><dt>**Pst \_ \_Tipo E \_ esistente**</dt> <dt>0x800C0004L</dt></span><span class="sxs-lookup"><span data-stu-id="30470-114"><dt>**PST\_E\_TYPE\_EXISTS**</dt> <dt>0x800C0004L</dt></span></span> </dl> | <span data-ttu-id="30470-115">L'elemento dati esiste già nell'archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="30470-115">The data item already exists in the protected storage.</span></span> <br/> |



<span data-ttu-id="30470-116">Valori della clausola di accesso</span><span class="sxs-lookup"><span data-stu-id="30470-116">Access Clause Values</span></span>



| <span data-ttu-id="30470-117">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="30470-117">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="30470-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30470-118">Description</span></span>                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <span data-ttu-id="30470-119"><dt>**Pst \_ AUTHENTICODE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30470-119"><dt>**PST\_AUTHENTICODE**</dt> <dt>1</dt></span></span> </dl>                       | <span data-ttu-id="30470-120">Punta a una struttura di [**\_ AUTHENTICODEDATA PST**](pst-authenticodedata.md) .</span><span class="sxs-lookup"><span data-stu-id="30470-120">Points to a [**PST\_AUTHENTICODEDATA**](pst-authenticodedata.md) structure.</span></span><br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <span data-ttu-id="30470-121"><dt> **\_ \_ Controllo binario PST**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="30470-121"><dt>**PST\_BINARY\_CHECK** </dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="30470-122">Punta a una struttura di **\_ BINARYCHECKDATA PST** .</span><span class="sxs-lookup"><span data-stu-id="30470-122">Points to a **PST\_BINARYCHECKDATA** structure.</span></span><br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <span data-ttu-id="30470-123"><dt>**Pst \_ \_Descrittore di sicurezza**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="30470-123"><dt>**PST\_SECURITY\_DESCRIPTOR**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="30470-124">Punta a un descrittore di sicurezza di Windows valido.</span><span class="sxs-lookup"><span data-stu-id="30470-124">Points to a valid Windows security descriptor.</span></span> <br/>                              |



## <a name="requirements"></a><span data-ttu-id="30470-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30470-125">Requirements</span></span>



| <span data-ttu-id="30470-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="30470-126">Requirement</span></span> | <span data-ttu-id="30470-127">Valore</span><span class="sxs-lookup"><span data-stu-id="30470-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="30470-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30470-128">Header</span></span><br/> | <dl> <span data-ttu-id="30470-129"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="30470-129"><dt>Pstore.h</dt></span></span> </dl> |



 

 
