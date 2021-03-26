---
description: Questa classe è la classe del tipo di evento per il caricamento di immagini negli eventi di file di paging. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 7d2f08e8-ec1f-4630-922a-548b55eadfda
title: Classe PageFault_ImageLoadBacked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_ImageLoadBacked
- PageFault_ImageLoadBacked.FileObject
- PageFault_ImageLoadBacked.DeviceChar
- PageFault_ImageLoadBacked.FileChar
- PageFault_ImageLoadBacked.LoadFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1644db74c5c7c361acda796219ae1415ecc262bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980087"
---
# <a name="pagefault_imageloadbacked-class"></a><span data-ttu-id="f8430-104">\_Classe pagefault ImageLoadBacked</span><span class="sxs-lookup"><span data-stu-id="f8430-104">PageFault\_ImageLoadBacked class</span></span>

<span data-ttu-id="f8430-105">Questa classe è la classe del tipo di evento per il caricamento di immagini negli eventi di file di paging.</span><span class="sxs-lookup"><span data-stu-id="f8430-105">This class is the event type class for image load in page file events.</span></span>

<span data-ttu-id="f8430-106">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="f8430-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8430-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8430-107">Syntax</span></span>

``` syntax
[EventType{105}, EventTypeName{"ImageLoadBacked"}]
class PageFault_ImageLoadBacked : PageFault_V2
{
  uint32 FileObject;
  uint32 DeviceChar;
  uint16 FileChar;
  uint16 LoadFlags;
};
```

## <a name="members"></a><span data-ttu-id="f8430-108">Members</span><span class="sxs-lookup"><span data-stu-id="f8430-108">Members</span></span>

<span data-ttu-id="f8430-109">La **classe \_ ImageLoadBacked di pagefault** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8430-109">The **PageFault\_ImageLoadBacked** class has these types of members:</span></span>

-   [<span data-ttu-id="f8430-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8430-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8430-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8430-111">Properties</span></span>

<span data-ttu-id="f8430-112">La **classe \_ ImageLoadBacked di pagefault** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8430-112">The **PageFault\_ImageLoadBacked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8430-113">**DeviceChar**</span><span class="sxs-lookup"><span data-stu-id="f8430-113">**DeviceChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8430-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8430-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8430-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8430-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8430-116">Qualificatori: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f8430-116">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f8430-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f8430-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f8430-118">**Filechar**</span><span class="sxs-lookup"><span data-stu-id="f8430-118">**FileChar**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8430-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8430-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8430-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8430-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8430-121">Qualificatori: WmiDataId (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f8430-121">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f8430-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f8430-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f8430-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="f8430-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8430-124">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8430-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f8430-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8430-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8430-126">Qualificatori: WmiDataId (1), puntatore</span><span class="sxs-lookup"><span data-stu-id="f8430-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f8430-127">Corrisponde al valore di questo puntatore al valore del puntatore **FileObject** in un evento del [**\_ nome**](fileio-name.md) di FileIO per determinare il nome del file.</span><span class="sxs-lookup"><span data-stu-id="f8430-127">Match the value of this pointer to the **FileObject** pointer value in a [**FileIo\_Name**](fileio-name.md) event to determine the name of the file.</span></span>

</dd> <dt>

<span data-ttu-id="f8430-128">**LoadFlags**</span><span class="sxs-lookup"><span data-stu-id="f8430-128">**LoadFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8430-129">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f8430-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f8430-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8430-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8430-131">Qualificatori: WmiDataId (4), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="f8430-131">Qualifiers: WmiDataId(4), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="f8430-132">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f8430-132">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8430-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8430-133">Remarks</span></span>

<span data-ttu-id="f8430-134">L'evento viene registrato durante la creazione di una sezione di immagine, ad esempio il caricamento di una DLL, quando il gestore della memoria determina che l'immagine deve essere copiata ed eseguita dal file di paging.</span><span class="sxs-lookup"><span data-stu-id="f8430-134">The event is logged during an image section creation (for example, a DLL load) when the memory manager determines that the image needs to be copied into and run from the page file.</span></span> <span data-ttu-id="f8430-135">Le immagini vengono in genere eseguite dal file di origine, ma il file di paging può verificarsi quando il gestore della memoria determina che il file di origine può essere modificato in modo asincrono da Writer esistenti o quando il file di origine si trova in un supporto rimovibile o in un dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="f8430-135">Typically, images are run from the source file but pagefile-backing can occur when the memory manager determines that the source file may be modified asynchronously by existing writers or when the source file is on a removable media or a remote device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8430-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8430-136">Requirements</span></span>



| <span data-ttu-id="f8430-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8430-137">Requirement</span></span> | <span data-ttu-id="f8430-138">Valore</span><span class="sxs-lookup"><span data-stu-id="f8430-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f8430-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8430-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f8430-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8430-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f8430-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8430-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f8430-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8430-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8430-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8430-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8430-144">**PageFault \_ v2**</span><span class="sxs-lookup"><span data-stu-id="f8430-144">**PageFault\_V2**</span></span>](pagefault-v2.md)
</dt> </dl>

 

 




