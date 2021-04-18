---
description: L'oggetto record è un contenitore per la conservazione e il trasferimento di un numero variabile di valori.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Oggetto record
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329953"
---
# <a name="record-object"></a><span data-ttu-id="0c557-103">Oggetto record</span><span class="sxs-lookup"><span data-stu-id="0c557-103">Record object</span></span>

<span data-ttu-id="0c557-104">L'oggetto **record** è un contenitore per la conservazione e il trasferimento di un numero variabile di valori.</span><span class="sxs-lookup"><span data-stu-id="0c557-104">The **Record** object is a container for holding and transferring a variable number of values.</span></span> <span data-ttu-id="0c557-105">I campi all'interno del record sono indicizzati numericamente e possono contenere stringhe, numeri interi, oggetti e valori null.</span><span class="sxs-lookup"><span data-stu-id="0c557-105">Fields within the record are numerically indexed and can contain strings, integers, objects, and null values.</span></span> <span data-ttu-id="0c557-106">I campi che superano le dimensioni del record allocato vengono considerati come aventi valori null permanenti.</span><span class="sxs-lookup"><span data-stu-id="0c557-106">Fields beyond the allocated record size are treated as having permanently null values.</span></span> <span data-ttu-id="0c557-107">Il campo numero 0 è riservato.</span><span class="sxs-lookup"><span data-stu-id="0c557-107">Field number 0 is reserved.</span></span>

## <a name="members"></a><span data-ttu-id="0c557-108">Membri</span><span class="sxs-lookup"><span data-stu-id="0c557-108">Members</span></span>

<span data-ttu-id="0c557-109">L'oggetto **record** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0c557-109">The **Record** object has these types of members:</span></span>

-   [<span data-ttu-id="0c557-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="0c557-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c557-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c557-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c557-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0c557-112">Methods</span></span>

<span data-ttu-id="0c557-113">L'oggetto **record** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0c557-113">The **Record** object has these methods.</span></span>



| <span data-ttu-id="0c557-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="0c557-114">Method</span></span>                                  | <span data-ttu-id="0c557-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c557-115">Description</span></span>                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c557-116">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="0c557-116">**ClearData**</span></span>](record-cleardata.md)   | <span data-ttu-id="0c557-117">Cancella i dati in tutti i campi e li imposta su null.</span><span class="sxs-lookup"><span data-stu-id="0c557-117">Clears the data in all fields, setting them to null.</span></span><br/>                                      |
| [<span data-ttu-id="0c557-118">**FormatText**</span><span class="sxs-lookup"><span data-stu-id="0c557-118">**FormatText**</span></span>](record-formattext.md) | <span data-ttu-id="0c557-119">Formatta i campi in base al modello nel campo 0.</span><span class="sxs-lookup"><span data-stu-id="0c557-119">Formats fields according to the template in field 0.</span></span><br/>                                      |
| [<span data-ttu-id="0c557-120">**ReadStream**</span><span class="sxs-lookup"><span data-stu-id="0c557-120">**ReadStream**</span></span>](record-readstream.md) | <span data-ttu-id="0c557-121">Legge un numero specificato di byte da un campo record contenente dati di flusso.</span><span class="sxs-lookup"><span data-stu-id="0c557-121">Reads a specified number of bytes from a record field holding stream data.</span></span><br/>                |
| [<span data-ttu-id="0c557-122">**Sestream**</span><span class="sxs-lookup"><span data-stu-id="0c557-122">**SetStream**</span></span>](record-setstream.md)   | <span data-ttu-id="0c557-123">Copia il contenuto del file specificato nel campo record designato come dati di flusso.</span><span class="sxs-lookup"><span data-stu-id="0c557-123">Copies the content of the specified file into the designated record field as stream data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0c557-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c557-124">Properties</span></span>

<span data-ttu-id="0c557-125">L'oggetto **record** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c557-125">The **Record** object has these properties.</span></span>



| <span data-ttu-id="0c557-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c557-126">Property</span></span>                                             | <span data-ttu-id="0c557-127">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="0c557-127">Access type</span></span>           | <span data-ttu-id="0c557-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c557-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c557-129">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="0c557-129">**DataSize**</span></span>](record-datasize.md)<br/>       |                       | <span data-ttu-id="0c557-130">Restituisce la dimensione dei dati per il campo designato.</span><span class="sxs-lookup"><span data-stu-id="0c557-130">Returns the size of the data for the designated field.</span></span><br/>                             |
| [<span data-ttu-id="0c557-131">**FieldCount**</span><span class="sxs-lookup"><span data-stu-id="0c557-131">**FieldCount**</span></span>](record-fieldcount.md)<br/>   |                       | <span data-ttu-id="0c557-132">Restituisce il numero di campi presenti nel record.</span><span class="sxs-lookup"><span data-stu-id="0c557-132">Returns the number of fields in the record.</span></span><br/>                                        |
| [<span data-ttu-id="0c557-133">**IntegerData**</span><span class="sxs-lookup"><span data-stu-id="0c557-133">**IntegerData**</span></span>](record-integerdata.md)<br/> | <span data-ttu-id="0c557-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0c557-134">Read/write</span></span><br/> | <span data-ttu-id="0c557-135">Trasferisce i dati Integer a 32 bit all'interno o all'esterno di un campo specificato all'interno del record.</span><span class="sxs-lookup"><span data-stu-id="0c557-135">Transfers 32-bit integer data in to or out of a specified field within the record.</span></span><br/> |
| [<span data-ttu-id="0c557-136">**IsNull**</span><span class="sxs-lookup"><span data-stu-id="0c557-136">**IsNull**</span></span>](record-isnull.md)<br/>           |                       | <span data-ttu-id="0c557-137">Restituisce true se il campo indicato è null e false se il campo contiene dati.</span><span class="sxs-lookup"><span data-stu-id="0c557-137">Returns True if the indicated field is null and False if the field contains data.</span></span><br/>  |
| [<span data-ttu-id="0c557-138">**StringData**</span><span class="sxs-lookup"><span data-stu-id="0c557-138">**StringData**</span></span>](record-stringdata.md)<br/>   | <span data-ttu-id="0c557-139">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="0c557-139">Read/write</span></span><br/> | <span data-ttu-id="0c557-140">Trasferisce i dati stringa in o da un campo specificato all'interno del record.</span><span class="sxs-lookup"><span data-stu-id="0c557-140">Transfers string data in to or out of a specified field within the record.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="0c557-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c557-141">Requirements</span></span>



| <span data-ttu-id="0c557-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c557-142">Requirement</span></span> | <span data-ttu-id="0c557-143">Valore</span><span class="sxs-lookup"><span data-stu-id="0c557-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c557-144">Versione</span><span class="sxs-lookup"><span data-stu-id="0c557-144">Version</span></span><br/> | <span data-ttu-id="0c557-145">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c557-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0c557-146">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0c557-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0c557-147">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="0c557-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0c557-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0c557-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="0c557-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c557-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0c557-150">IID</span><span class="sxs-lookup"><span data-stu-id="0c557-150">IID</span></span><br/>     | <span data-ttu-id="0c557-151">IID \_ IRecord è definito come 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0c557-151">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="0c557-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c557-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c557-153">**Metodo CreaRecord**</span><span class="sxs-lookup"><span data-stu-id="0c557-153">**CreateRecord Method**</span></span>](installer-createrecord.md)
</dt> <dt>

[<span data-ttu-id="0c557-154">Esempi di script di Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0c557-154">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




