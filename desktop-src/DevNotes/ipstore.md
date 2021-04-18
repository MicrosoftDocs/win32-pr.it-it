---
description: Fornisce metodi standard COM per gestire gli elementi di dati di archiviazione protetti.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Interfaccia IPStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324703"
---
# <a name="ipstore-interface"></a><span data-ttu-id="29b62-103">Interfaccia IPStore</span><span class="sxs-lookup"><span data-stu-id="29b62-103">IPStore interface</span></span>

<span data-ttu-id="29b62-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29b62-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="29b62-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="29b62-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="29b62-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="29b62-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="29b62-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="29b62-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="29b62-108">\[Questa interfaccia può essere modificata o non disponibile nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="29b62-108">\[This interface may be altered or unavailable in future versions of Windows.\]</span></span>

<span data-ttu-id="29b62-109">Fornisce metodi standard COM per gestire gli elementi di dati di archiviazione protetti.</span><span class="sxs-lookup"><span data-stu-id="29b62-109">Provides COM-standard methods to manage protected storage data items.</span></span> <span data-ttu-id="29b62-110">Il metodo [**PStoreCreateInstance**](pstorecreateinstance.md) restituisce un puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="29b62-110">The [**PStoreCreateInstance**](pstorecreateinstance.md) method returns a pointer to this interface.</span></span>

## <a name="members"></a><span data-ttu-id="29b62-111">Membri</span><span class="sxs-lookup"><span data-stu-id="29b62-111">Members</span></span>

<span data-ttu-id="29b62-112">L'interfaccia **IPStore** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="29b62-112">The **IPStore** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="29b62-113">**IPStore** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="29b62-113">**IPStore** also has these types of members:</span></span>

-   [<span data-ttu-id="29b62-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="29b62-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="29b62-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="29b62-115">Methods</span></span>

<span data-ttu-id="29b62-116">L'interfaccia **IPStore** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="29b62-116">The **IPStore** interface has these methods.</span></span>



| <span data-ttu-id="29b62-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="29b62-117">Method</span></span>                                                   | <span data-ttu-id="29b62-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29b62-118">Description</span></span>                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29b62-119">**CloseItem**</span><span class="sxs-lookup"><span data-stu-id="29b62-119">**CloseItem**</span></span>](ipstore-closeitem.md)                   | <span data-ttu-id="29b62-120">Chiude un elemento dati specificato dall'archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="29b62-120">Closes a specified data item from protected storage.</span></span><br/>                                                       |
| [<span data-ttu-id="29b62-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="29b62-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)           | <span data-ttu-id="29b62-122">Crea il sottotipo specificato all'interno del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="29b62-122">Creates the specified subtype within the specified type.</span></span><br/>                                                   |
| [<span data-ttu-id="29b62-123">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="29b62-123">**CreateType**</span></span>](ipstore-createtype.md)                 | <span data-ttu-id="29b62-124">Crea il tipo specificato con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="29b62-124">Creates the specified type with the specified name.</span></span><br/>                                                        |
| [<span data-ttu-id="29b62-125">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="29b62-125">**DeleteItem**</span></span>](ipstore-deleteitem.md)                 | <span data-ttu-id="29b62-126">Elimina l'elemento specificato dall'archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="29b62-126">Deletes the specified item from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="29b62-127">**DeleteSubtype**</span><span class="sxs-lookup"><span data-stu-id="29b62-127">**DeleteSubtype**</span></span>](ipstore-deletesubtype.md)           | <span data-ttu-id="29b62-128">Elimina il sottotipo di elemento specificato dalla risorsa di archiviazione protetta.</span><span class="sxs-lookup"><span data-stu-id="29b62-128">Deletes the specified item subtype from the protected storage.</span></span><br/>                                             |
| [<span data-ttu-id="29b62-129">**DeleteType**</span><span class="sxs-lookup"><span data-stu-id="29b62-129">**DeleteType**</span></span>](ipstore-deletetype.md)                 | <span data-ttu-id="29b62-130">Elimina il tipo specificato dalla risorsa di archiviazione protetta.</span><span class="sxs-lookup"><span data-stu-id="29b62-130">Deletes the specified type from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="29b62-131">**EnumItems**</span><span class="sxs-lookup"><span data-stu-id="29b62-131">**EnumItems**</span></span>](ipstore-enumitems.md)                   | <span data-ttu-id="29b62-132">Restituisce il puntatore a interfaccia di un sottotipo per l'enumerazione degli elementi nel database di archiviazione protetta.</span><span class="sxs-lookup"><span data-stu-id="29b62-132">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span><br/>        |
| [<span data-ttu-id="29b62-133">**EnumSubtypes**</span><span class="sxs-lookup"><span data-stu-id="29b62-133">**EnumSubtypes**</span></span>](ipstore-enumsubtypes.md)             | <span data-ttu-id="29b62-134">Restituisce un'interfaccia per l'enumerazione dei sottotipi dei tipi attualmente registrati nel database protetto.</span><span class="sxs-lookup"><span data-stu-id="29b62-134">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span><br/> |
| [<span data-ttu-id="29b62-135">**EnumTypes**</span><span class="sxs-lookup"><span data-stu-id="29b62-135">**EnumTypes**</span></span>](ipstore-enumtypes.md)                   | <span data-ttu-id="29b62-136">Restituisce un'interfaccia per l'enumerazione dei tipi attualmente registrati nel database protetto.</span><span class="sxs-lookup"><span data-stu-id="29b62-136">Returns an interface for enumerating the types currently registered in the protected database.</span></span><br/>             |
| [<span data-ttu-id="29b62-137">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="29b62-137">**GetInfo**</span></span>](ipstore-getinfo.md)                       | <span data-ttu-id="29b62-138">Recupera le informazioni sul provider di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="29b62-138">Retrieves information about the storage provider.</span></span><br/>                                                          |
| [<span data-ttu-id="29b62-139">**GetProvParam**</span><span class="sxs-lookup"><span data-stu-id="29b62-139">**GetProvParam**</span></span>](ipstore-getprovparam.md)             | <span data-ttu-id="29b62-140">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="29b62-140">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="29b62-141">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="29b62-141">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)         | <span data-ttu-id="29b62-142">Recupera le informazioni associate a un sottotipo.</span><span class="sxs-lookup"><span data-stu-id="29b62-142">Retrieves information associated with a subtype.</span></span><br/>                                                           |
| [<span data-ttu-id="29b62-143">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="29b62-143">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)               | <span data-ttu-id="29b62-144">Recupera le informazioni associate a un tipo.</span><span class="sxs-lookup"><span data-stu-id="29b62-144">Retrieves information associated with a type.</span></span><br/>                                                              |
| [<span data-ttu-id="29b62-145">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="29b62-145">**OpenItem**</span></span>](ipstore-openitem.md)                     | <span data-ttu-id="29b62-146">Apre un elemento per più accessi.</span><span class="sxs-lookup"><span data-stu-id="29b62-146">Opens an item for multiple accesses.</span></span><br/>                                                                       |
| [<span data-ttu-id="29b62-147">**ReadAccessRuleSet**</span><span class="sxs-lookup"><span data-stu-id="29b62-147">**ReadAccessRuleSet**</span></span>](ipstore-readaccessruleset.md)   | <span data-ttu-id="29b62-148">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="29b62-148">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="29b62-149">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="29b62-149">**ReadItem**</span></span>](ipstore-readitem.md)                     | <span data-ttu-id="29b62-150">Legge l'elemento dati specificato dall'archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="29b62-150">Reads the specified data item from protected storage.</span></span><br/>                                                      |
| [<span data-ttu-id="29b62-151">**SetProvParam**</span><span class="sxs-lookup"><span data-stu-id="29b62-151">**SetProvParam**</span></span>](ipstore-setprovparam.md)             | <span data-ttu-id="29b62-152">Imposta le informazioni sul parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="29b62-152">Sets the specified parameter information.</span></span><br/>                                                                  |
| [<span data-ttu-id="29b62-153">**WriteAccessRuleset**</span><span class="sxs-lookup"><span data-stu-id="29b62-153">**WriteAccessRuleset**</span></span>](ipstore-writeaccessruleset.md) | <span data-ttu-id="29b62-154">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="29b62-154">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="29b62-155">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="29b62-155">**WriteItem**</span></span>](ipstore-writeitem.md)                   | <span data-ttu-id="29b62-156">Scrive un elemento di dati in un archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="29b62-156">Writes a data item to protected storage.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="29b62-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29b62-157">Requirements</span></span>



| <span data-ttu-id="29b62-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="29b62-158">Requirement</span></span> | <span data-ttu-id="29b62-159">Valore</span><span class="sxs-lookup"><span data-stu-id="29b62-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29b62-160">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29b62-160">Header</span></span><br/> | <dl> <span data-ttu-id="29b62-161"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="29b62-161"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="29b62-162">DLL</span><span class="sxs-lookup"><span data-stu-id="29b62-162">DLL</span></span><br/>    | <dl> <span data-ttu-id="29b62-163"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29b62-163"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
