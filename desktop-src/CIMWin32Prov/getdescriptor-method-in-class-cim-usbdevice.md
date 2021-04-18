---
description: Il metodo descrittore restituisce il descrittore di dispositivo USB come specificato dai parametri di input.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Metodo GetDescriptor della classe CIM_USBDevice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304687"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a><span data-ttu-id="4ae37-103">Metodo GetDescriptor della classe CIM_USBDevice (Wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="4ae37-103">GetDescriptor method of the CIM_USBDevice class (Wmcodecdsp.h)</span></span>

<span data-ttu-id="4ae37-104">Il metodo **descrittore** restituisce il descrittore di dispositivo USB come specificato dai parametri di input.</span><span class="sxs-lookup"><span data-stu-id="4ae37-104">The **GetDescriptor** method returns the USB device descriptor as specified by the input parameters.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4ae37-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4ae37-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4ae37-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4ae37-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4ae37-107">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="4ae37-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4ae37-108">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4ae37-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae37-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ae37-109">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="4ae37-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ae37-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae37-111">*RequestType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ae37-111">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae37-112">Identificatore con mapping bit per il tipo di richiesta del descrittore e il destinatario.</span><span class="sxs-lookup"><span data-stu-id="4ae37-112">Bit-mapped identifier for the type of descriptor request and the recipient.</span></span> <span data-ttu-id="4ae37-113">Vedere la specifica USB per i valori appropriati per ogni bit.</span><span class="sxs-lookup"><span data-stu-id="4ae37-113">Refer to the USB specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="4ae37-114">*RequestValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ae37-114">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae37-115">Contiene il tipo di descrittore nel byte elevato e l'indice del descrittore, ad esempio indice o offset nella matrice di descrittori, nel byte minimo.</span><span class="sxs-lookup"><span data-stu-id="4ae37-115">Contains the descriptor type in the high byte and the descriptor index (for example, index or offset into the descriptor array) in the low byte.</span></span> <span data-ttu-id="4ae37-116">Per ulteriori informazioni, vedere la specifica USB.</span><span class="sxs-lookup"><span data-stu-id="4ae37-116">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="4ae37-117">*RequestIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ae37-117">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae37-118">Specifica il codice dell'identificatore di lingua a 2 byte usato dal dispositivo USB per la restituzione di dati del descrittore di stringa.</span><span class="sxs-lookup"><span data-stu-id="4ae37-118">Specifies the 2-byte language identifier code used by the USB device when returning string descriptor data.</span></span> <span data-ttu-id="4ae37-119">Il parametro è in genere 0 (zero) per i descrittori non di stringa.</span><span class="sxs-lookup"><span data-stu-id="4ae37-119">The parameter is typically 0 (zero) for nonstring descriptors.</span></span> <span data-ttu-id="4ae37-120">Per ulteriori informazioni, vedere la specifica USB.</span><span class="sxs-lookup"><span data-stu-id="4ae37-120">For more information, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="4ae37-121">*RequestLength* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4ae37-121">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae37-122">In input, lunghezza (in ottetti) del descrittore che deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="4ae37-122">On input, length (in octets) of the descriptor that should be returned.</span></span> <span data-ttu-id="4ae37-123">Se questo valore è inferiore alla lunghezza effettiva del descrittore, viene restituita solo la lunghezza richiesta.</span><span class="sxs-lookup"><span data-stu-id="4ae37-123">If this value is less than the actual length of the descriptor, only the requested length is returned.</span></span> <span data-ttu-id="4ae37-124">Se è maggiore della lunghezza effettiva, viene restituita la lunghezza effettiva.</span><span class="sxs-lookup"><span data-stu-id="4ae37-124">If it is more than the actual length, the actual length is returned.</span></span>

<span data-ttu-id="4ae37-125">Nell'output, la lunghezza (in ottetti) del buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="4ae37-125">On output, the length (in octets) of the buffer being returned.</span></span> <span data-ttu-id="4ae37-126">Se il descrittore richiesto non esiste, il contenuto di questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="4ae37-126">If the requested descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="4ae37-127">*Buffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4ae37-127">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ae37-128">Restituisce le informazioni sul descrittore richieste.</span><span class="sxs-lookup"><span data-stu-id="4ae37-128">Returns the requested descriptor information.</span></span> <span data-ttu-id="4ae37-129">Se il descrittore non esiste, il contenuto di questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="4ae37-129">If the descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ae37-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ae37-130">Return value</span></span>

<span data-ttu-id="4ae37-131">Restituisce un valore pari a 0 (zero) se il descrittore USB viene restituito correttamente, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="4ae37-131">Returns a value of 0 (zero) if the USB descriptor is successfully returned, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span> <span data-ttu-id="4ae37-132">In una sottoclasse, il set di possibili codici restituiti può essere specificato utilizzando un qualificatore **ValueMap** nel metodo.</span><span class="sxs-lookup"><span data-stu-id="4ae37-132">In a subclass, the set of possible return codes could be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="4ae37-133">Le stringhe a cui viene convertito il contenuto mofqualifier possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .</span><span class="sxs-lookup"><span data-stu-id="4ae37-133">The strings to which the mofqualifier contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ae37-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ae37-134">Remarks</span></span>

<span data-ttu-id="4ae37-135">Questo metodo non è attualmente implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="4ae37-135">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4ae37-136">Per usare questo metodo, è necessario implementarlo nel proprio provider.</span><span class="sxs-lookup"><span data-stu-id="4ae37-136">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4ae37-137">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4ae37-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4ae37-138">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4ae37-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae37-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ae37-139">Requirements</span></span>



| <span data-ttu-id="4ae37-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae37-140">Requirement</span></span> | <span data-ttu-id="4ae37-141">Valore</span><span class="sxs-lookup"><span data-stu-id="4ae37-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae37-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ae37-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae37-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ae37-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ae37-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ae37-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae37-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ae37-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ae37-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4ae37-146">Namespace</span></span><br/>                | <span data-ttu-id="4ae37-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4ae37-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ae37-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ae37-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ae37-149"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ae37-149"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="4ae37-150">MOF</span><span class="sxs-lookup"><span data-stu-id="4ae37-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ae37-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ae37-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ae37-152">DLL</span><span class="sxs-lookup"><span data-stu-id="4ae37-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ae37-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ae37-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ae37-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ae37-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae37-155">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4ae37-155">**CIM\_USBDevice**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[<span data-ttu-id="4ae37-156">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4ae37-156">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

