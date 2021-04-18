---
description: Restituisce il descrittore USBDevice come specificato dai parametri di input.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Metodo GetDescriptor della classe CIM_USBDevice (gestione di Hyper-V)
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
- vmms.exe
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310567"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="24828-103">Metodo GetDescriptor della classe CIM_USBDevice (gestione di Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="24828-103">GetDescriptor method of the CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="24828-104">Restituisce il descrittore USBDevice come specificato dai parametri di input.</span><span class="sxs-lookup"><span data-stu-id="24828-104">Returns the USBDevice descriptor as specified by the input parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="24828-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24828-105">Syntax</span></span>


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a><span data-ttu-id="24828-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24828-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24828-107">*RequestType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24828-107">*RequestType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24828-108">Mappa di bit che identifica il tipo di richiesta del descrittore e il destinatario.</span><span class="sxs-lookup"><span data-stu-id="24828-108">Bit-map that identifies the type of Descriptor request and the recipient.</span></span> <span data-ttu-id="24828-109">Il tipo di richiesta può essere ' standard ',' Class ' o ' specifico del fornitore '.</span><span class="sxs-lookup"><span data-stu-id="24828-109">The type of request may be 'standard', 'class' or 'vendor-specific'.</span></span> <span data-ttu-id="24828-110">Il destinatario può essere ' Device ',' Interface ',' endpoint ' o ' other '.</span><span class="sxs-lookup"><span data-stu-id="24828-110">The recipient may be 'device', 'interface', 'endpoint' or 'other'.</span></span> <span data-ttu-id="24828-111">Vedere la specifica USB per i valori appropriati per ogni bit.</span><span class="sxs-lookup"><span data-stu-id="24828-111">Refer to the USB Specification for the appropriate values for each bit.</span></span>

</dd> <dt>

<span data-ttu-id="24828-112">*RequestValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24828-112">*RequestValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24828-113">Contiene il tipo di descrittore nel byte elevato e l'indice del descrittore, ad esempio indice o offset nella matrice di descrittori, nel byte minimo.</span><span class="sxs-lookup"><span data-stu-id="24828-113">Contains the Descriptor Type in the high byte and the Descriptor Index (for example, index or offset into the Descriptor array) in the low byte.</span></span> <span data-ttu-id="24828-114">Per ulteriori informazioni, fare riferimento alla specifica USB.</span><span class="sxs-lookup"><span data-stu-id="24828-114">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="24828-115">*RequestIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24828-115">*RequestIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24828-116">Definisce il codice ID lingua a 2 byte utilizzato da USBDevice quando vengono restituiti i dati del descrittore di stringa.</span><span class="sxs-lookup"><span data-stu-id="24828-116">Defines the 2 byte Language ID code used by the USBDevice when returning string Descriptor data.</span></span> <span data-ttu-id="24828-117">Il parametro è in genere 0 per i descrittori non di stringa.</span><span class="sxs-lookup"><span data-stu-id="24828-117">The parameter is typically 0 for non-string Descriptors.</span></span> <span data-ttu-id="24828-118">Per ulteriori informazioni, fare riferimento alla specifica USB.</span><span class="sxs-lookup"><span data-stu-id="24828-118">Refer to the USB Specification for more information.</span></span>

</dd> <dt>

<span data-ttu-id="24828-119">*RequestLength* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="24828-119">*RequestLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="24828-120">In input, contiene la lunghezza (in ottetti) del descrittore che deve essere restituito.</span><span class="sxs-lookup"><span data-stu-id="24828-120">On input, contains the length (in octets) of the Descriptor that should be returned.</span></span> <span data-ttu-id="24828-121">Se questo valore è inferiore alla lunghezza effettiva del descrittore, verrà restituita solo la lunghezza richiesta.</span><span class="sxs-lookup"><span data-stu-id="24828-121">If this value is less than the actual length of the Descriptor, only the requested length will be returned.</span></span> <span data-ttu-id="24828-122">Se è maggiore della lunghezza effettiva, viene restituita la lunghezza effettiva.</span><span class="sxs-lookup"><span data-stu-id="24828-122">If it is more than the actual length, the actual length is returned.</span></span> <span data-ttu-id="24828-123">Nell'output, questo parametro è la lunghezza, in ottetti, del buffer restituito.</span><span class="sxs-lookup"><span data-stu-id="24828-123">On output, this parameter is the length, in octets, of the Buffer being returned.</span></span> <span data-ttu-id="24828-124">Se il descrittore richiesto non esiste, il contenuto di questo parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="24828-124">If the requested Descriptor does not exist, the contents of this parameter are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="24828-125">*Buffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24828-125">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24828-126">Restituisce le informazioni sul descrittore richieste.</span><span class="sxs-lookup"><span data-stu-id="24828-126">Returns the requested Descriptor information.</span></span> <span data-ttu-id="24828-127">Se il descrittore non esiste, il contenuto del parametro non è definito.</span><span class="sxs-lookup"><span data-stu-id="24828-127">If the Descriptor does not exist, the contents of the parameter are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24828-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24828-128">Return value</span></span>

<span data-ttu-id="24828-129">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="24828-129">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="24828-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24828-130">Requirements</span></span>



| <span data-ttu-id="24828-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="24828-131">Requirement</span></span> | <span data-ttu-id="24828-132">Valore</span><span class="sxs-lookup"><span data-stu-id="24828-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24828-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24828-133">Minimum supported client</span></span><br/> | <span data-ttu-id="24828-134">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="24828-134">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="24828-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24828-135">Minimum supported server</span></span><br/> | <span data-ttu-id="24828-136">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="24828-136">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="24828-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="24828-137">Namespace</span></span><br/>                | <span data-ttu-id="24828-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="24828-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="24828-139">MOF</span><span class="sxs-lookup"><span data-stu-id="24828-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24828-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24828-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="24828-141">DLL</span><span class="sxs-lookup"><span data-stu-id="24828-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24828-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="24828-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="24828-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24828-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24828-144">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="24828-144">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> </dl>

 

 




