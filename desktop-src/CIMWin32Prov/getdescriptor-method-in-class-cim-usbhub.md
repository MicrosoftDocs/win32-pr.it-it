---
description: Il metodo descrittore restituisce il descrittore dell'hub USB come specificato dai parametri di input.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Metodo GetDescriptor della classe CIM_USBHub (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966062"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a><span data-ttu-id="6177e-103">Metodo GetDescriptor della classe CIM \_ USBHub</span><span class="sxs-lookup"><span data-stu-id="6177e-103">GetDescriptor method of the CIM\_USBHub class</span></span>

<span data-ttu-id="6177e-104">Il metodo **descrittore** restituisce il descrittore dell'hub USB come specificato dai parametri di input.</span><span class="sxs-lookup"><span data-stu-id="6177e-104">The **GetDescriptor** method returns the USB hub descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6177e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6177e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6177e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6177e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6177e-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="6177e-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6177e-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6177e-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6177e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6177e-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="6177e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6177e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6177e-111">*RequestType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6177e-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6177e-112">Identificatore con mapping bit per il tipo di richiesta del descrittore e il destinatario.</span><span class="sxs-lookup"><span data-stu-id="6177e-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="6177e-113">Per i valori appropriati per ogni bit, vedere la specifica USB.</span><span class="sxs-lookup"><span data-stu-id="6177e-113">For the appropriate values for each bit, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="6177e-114">*RequestValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6177e-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6177e-115">Contiene il tipo di descrittore nel byte elevato e l'indice del descrittore, ad esempio indice o offset nella matrice di descrittori, nel byte minimo.</span><span class="sxs-lookup"><span data-stu-id="6177e-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="6177e-116">Per ulteriori informazioni, vedere la specifica USB.</span><span class="sxs-lookup"><span data-stu-id="6177e-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="6177e-117">*RequestIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6177e-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6177e-118">Specifica il codice dell'identificatore di lingua a 2 byte usato dal dispositivo USB per la restituzione di dati del descrittore di stringa.</span><span class="sxs-lookup"><span data-stu-id="6177e-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="6177e-119">Il parametro è in genere 0 (zero) per i descrittori non di stringa.</span><span class="sxs-lookup"><span data-stu-id="6177e-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="6177e-120">Per ulteriori informazioni, vedere la specifica USB.</span><span class="sxs-lookup"><span data-stu-id="6177e-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="6177e-121">*RequestLength* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6177e-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6177e-122">In input, lunghezza (in ottetti) del descrittore che deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="6177e-122">On input, the length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="6177e-123">Se questo valore è inferiore alla lunghezza effettiva del descrittore, viene restituita solo la lunghezza richiesta.</span><span class="sxs-lookup"><span data-stu-id="6177e-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="6177e-124">Se è maggiore della lunghezza effettiva, viene restituita la lunghezza effettiva.</span><span class="sxs-lookup"><span data-stu-id="6177e-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="6177e-125">Nell'output, la lunghezza (in ottetti) del buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="6177e-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="6177e-126">Se il descrittore richiesto non esiste, il contenuto di questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="6177e-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="6177e-127">*Buffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6177e-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6177e-128">Il buffer restituisce le informazioni del descrittore richieste.</span><span class="sxs-lookup"><span data-stu-id="6177e-128">Buffer returns the requested descriptor information.</span></span> <span data-ttu-id="6177e-129">Se il descrittore non esiste, il contenuto del buffer non è definito.</span><span class="sxs-lookup"><span data-stu-id="6177e-129">If the descriptor does not exist, the contents of the buffer are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6177e-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6177e-130">Return value</span></span>

<span data-ttu-id="6177e-131">Restituisce un valore pari a 0 (zero) se il descrittore USB viene restituito correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="6177e-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="6177e-132">In una sottoclasse, il set di possibili codici restituiti può essere specificato utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="6177e-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="6177e-133">Le stringhe a cui viene convertito il contenuto **mofqualifier** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="6177e-133">The strings to which the **mofqualifier** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="6177e-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="6177e-134">Remarks</span></span>

<span data-ttu-id="6177e-135">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="6177e-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6177e-136">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="6177e-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6177e-137">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6177e-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6177e-138">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6177e-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6177e-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6177e-139">Requirements</span></span>



| <span data-ttu-id="6177e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6177e-140">Requirement</span></span> | <span data-ttu-id="6177e-141">Valore</span><span class="sxs-lookup"><span data-stu-id="6177e-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6177e-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6177e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6177e-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6177e-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6177e-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6177e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6177e-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6177e-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6177e-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6177e-146">Namespace</span></span><br/>                | <span data-ttu-id="6177e-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6177e-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6177e-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6177e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="6177e-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6177e-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="6177e-150">MOF</span><span class="sxs-lookup"><span data-stu-id="6177e-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6177e-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6177e-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6177e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="6177e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6177e-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6177e-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6177e-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6177e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6177e-155">**\_Usbhub CIM**</span><span class="sxs-lookup"><span data-stu-id="6177e-155">**CIM\_USBHub**</span></span>](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[<span data-ttu-id="6177e-156">**\_Usbhub CIM**</span><span class="sxs-lookup"><span data-stu-id="6177e-156">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> </dl>

 

