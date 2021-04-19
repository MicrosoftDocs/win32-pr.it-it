---
description: Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi di parametro per i metodi e gli eventi di un servizio dispositivo.
ms.assetid: a7708c60-758a-4fb6-8ef9-074ecdc9cf60
title: Attributi parametro (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Parameter
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 113b2b35a5b6e61cd2cc1d3666d1a13fbade5ec7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324044"
---
# <a name="parameter-attributes"></a><span data-ttu-id="04175-103">Attributi del parametro</span><span class="sxs-lookup"><span data-stu-id="04175-103">Parameter Attributes</span></span>

<span data-ttu-id="04175-104">Per Windows 7, i dispositivi portatili Windows supportano i seguenti attributi di parametro per i metodi e gli eventi di un servizio dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04175-104">For Windows 7, Windows Portable Devices supports the following parameter attributes for methods and events of a device service.</span></span> <span data-ttu-id="04175-105">Questi attributi vengono restituiti dai metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="04175-105">These attributes are returned by the these methods:</span></span>

-   [<span data-ttu-id="04175-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="04175-106">**IPortableDeviceServiceCapabilities::GetMethodParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes)
-   [<span data-ttu-id="04175-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span><span class="sxs-lookup"><span data-stu-id="04175-107">**IPortableDeviceServiceCapabilities::GetEventParameterAttributes**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-geteventparameterattributes)




| <span data-ttu-id="04175-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="04175-108">Attribute</span></span>                                            | <span data-ttu-id="04175-109">VarType</span><span class="sxs-lookup"><span data-stu-id="04175-109">VarType</span></span>         | <span data-ttu-id="04175-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04175-110">Description</span></span>                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04175-111">**\_ \_ valore predefinito dell'attributo del parametro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04175-111">**WPD\_PARAMETER\_ATTRIBUTE\_DEFAULT\_VALUE**</span></span>        | <span data-ttu-id="04175-112">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="04175-112">VT\_*XXXX*</span></span>      | <span data-ttu-id="04175-113">Valore predefinito del parametro.</span><span class="sxs-lookup"><span data-stu-id="04175-113">The default value of the parameter.</span></span>                                                                                                                                                         |
| <span data-ttu-id="04175-114">**\_elementi di \_ \_ enumerazione \_ degli attributi di parametro WPD**</span><span class="sxs-lookup"><span data-stu-id="04175-114">**WPD\_PARAMETER\_ATTRIBUTE\_ENUMERATION\_ELEMENTS**</span></span> | <span data-ttu-id="04175-115">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="04175-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="04175-116">Interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene i valori di enumerazione per il parametro.</span><span class="sxs-lookup"><span data-stu-id="04175-116">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface that contains the enumeration values for the parameter.</span></span>                                   |
| <span data-ttu-id="04175-117">**\_ \_ form attributo parametro \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="04175-117">**WPD\_PARAMETER\_ATTRIBUTE\_FORM**</span></span>                  | <span data-ttu-id="04175-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="04175-118">**VT\_UI4**</span></span>     | <span data-ttu-id="04175-119">Formato dei valori di parametro validi consentiti.</span><span class="sxs-lookup"><span data-stu-id="04175-119">The form of valid parameter values allowed.</span></span>                                                                                                                                                 |
| <span data-ttu-id="04175-120">**\_ \_ \_ dimensioni massime attributo parametro WPD \_**</span><span class="sxs-lookup"><span data-stu-id="04175-120">**WPD\_PARAMETER\_ATTRIBUTE\_MAX\_SIZE**</span></span>             | <span data-ttu-id="04175-121">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="04175-121">**VT\_UI8**</span></span>     | <span data-ttu-id="04175-122">Dimensione massima, in byte, del parametro.</span><span class="sxs-lookup"><span data-stu-id="04175-122">The maximum size of the parameter, in bytes .</span></span>                                                                                                                                               |
| <span data-ttu-id="04175-123">**\_ \_ nome attributo parametro \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="04175-123">**WPD\_PARAMETER\_ATTRIBUTE\_NAME**</span></span>                  | <span data-ttu-id="04175-124">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="04175-124">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="04175-125">Stringa che specifica il nome descrittivo di un evento o un parametro di metodo.</span><span class="sxs-lookup"><span data-stu-id="04175-125">A string that specifies the script-friendly name of an event or method parameter.</span></span> <span data-ttu-id="04175-126">I caratteri validi sono alfanumerici \[ a-Za-z0-9 \] è \_ '.</span><span class="sxs-lookup"><span data-stu-id="04175-126">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span>                                                 |
| <span data-ttu-id="04175-127">**\_ \_ ordine attributo parametro \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="04175-127">**WPD\_PARAMETER\_ATTRIBUTE\_ORDER**</span></span>                 | <span data-ttu-id="04175-128">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="04175-128">**VT\_UI4**</span></span>     | <span data-ttu-id="04175-129">Indice dell'ordine dei parametri in base zero, in modo che un valore di ordine pari a 0 corrisponda al primo parametro.</span><span class="sxs-lookup"><span data-stu-id="04175-129">The zero-based parameter-order index, so that an order value of 0 corresponds to the first parameter.</span></span>                                                                                       |
| <span data-ttu-id="04175-130">**\_ \_ intervallo attributi parametro \_ WPD \_ min**</span><span class="sxs-lookup"><span data-stu-id="04175-130">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MIN**</span></span>            | <span data-ttu-id="04175-131">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="04175-131">VT\_*XXXX*</span></span>      | <span data-ttu-id="04175-132">Il valore massimo per un parametro nell'intervallo del form dell'attributo del parametro del modulo WPD \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04175-132">The maximum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="04175-133">**\_ \_ intervallo attributi parametro \_ WPD \_ Max**</span><span class="sxs-lookup"><span data-stu-id="04175-133">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_MAX**</span></span>            | <span data-ttu-id="04175-134">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="04175-134">VT\_*XXXX*</span></span>      | <span data-ttu-id="04175-135">Il valore minimo per un parametro nell'intervallo del form dell'attributo del parametro del modulo WPD \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04175-135">The minimum value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                       |
| <span data-ttu-id="04175-136">**\_passaggio dell' \_ intervallo di attributi del parametro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04175-136">**WPD\_PARAMETER\_ATTRIBUTE\_RANGE\_STEP**</span></span>           | <span data-ttu-id="04175-137">VT \_ *xxxx*</span><span class="sxs-lookup"><span data-stu-id="04175-137">VT\_*XXXX*</span></span>      | <span data-ttu-id="04175-138">Valore del passaggio per un parametro nell'intervallo del form dell'attributo del parametro del modulo WPD \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04175-138">The step value for a parameter of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE.</span></span>                                                                                                          |
| <span data-ttu-id="04175-139">**\_ \_ \_ espressione regolare attributo parametro \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="04175-139">**WPD\_PARAMETER\_ATTRIBUTE\_REGULAR\_EXPRESSION**</span></span>   | <span data-ttu-id="04175-140">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="04175-140">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="04175-141">Espressione regolare che specifica i valori accettabili per i parametri dell' \_ espressione regolare dell'attributo del parametro form WPD \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04175-141">A regular expression that specifies acceptable values for parameters of the form WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION.</span></span>                                                      |
| <span data-ttu-id="04175-142">**\_tipo di \_ utilizzo dell'attributo del parametro WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04175-142">**WPD\_PARAMETER\_ATTRIBUTE\_USAGE\_TYPE**</span></span>           | <span data-ttu-id="04175-143">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="04175-143">**VT\_UI4**</span></span>     | <span data-ttu-id="04175-144">Integer che specifica l'utilizzo di un parametro di metodo, ad esempio in/out. I valori validi sono del tipo di enumerazione dei [**\_ tipi di \_ utilizzo \_ del parametro WPD**](wpd-parameter-usage-types.md) .</span><span class="sxs-lookup"><span data-stu-id="04175-144">An integer that specifies the usage of a method parameter, for example, in/out. Valid values are of the [**WPD\_PARAMETER\_USAGE\_TYPES**](wpd-parameter-usage-types.md) enumeration type.</span></span> |
| <span data-ttu-id="04175-145">**WPD \_ \_ attributo parametro \_ VarType**</span><span class="sxs-lookup"><span data-stu-id="04175-145">**WPD\_PARAMETER\_ATTRIBUTE\_VARTYPE**</span></span>               | <span data-ttu-id="04175-146">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="04175-146">**VT\_UI4**</span></span>     | <span data-ttu-id="04175-147">Il parametro VarType.</span><span class="sxs-lookup"><span data-stu-id="04175-147">The parameter VarType.</span></span>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="04175-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04175-148">Requirements</span></span>



| <span data-ttu-id="04175-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="04175-149">Requirement</span></span> | <span data-ttu-id="04175-150">Valore</span><span class="sxs-lookup"><span data-stu-id="04175-150">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="04175-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04175-151">Header</span></span><br/> | <dl> <span data-ttu-id="04175-152"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="04175-152"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04175-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04175-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04175-154">**Proprietà e attributi**</span><span class="sxs-lookup"><span data-stu-id="04175-154">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




