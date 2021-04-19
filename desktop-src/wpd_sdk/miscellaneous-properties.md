---
description: I dispositivi portatili Windows supportano le proprietà varie seguenti.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Proprietà varie (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326292"
---
# <a name="miscellaneous-properties"></a><span data-ttu-id="f122b-103">Proprietà varie</span><span class="sxs-lookup"><span data-stu-id="f122b-103">Miscellaneous Properties</span></span>

<span data-ttu-id="f122b-104">I dispositivi portatili Windows supportano le proprietà varie seguenti.</span><span class="sxs-lookup"><span data-stu-id="f122b-104">Windows Portable Devices supports the following miscellaneous properties.</span></span>



| <span data-ttu-id="f122b-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f122b-105">Property</span></span>                                       | <span data-ttu-id="f122b-106">VarType</span><span class="sxs-lookup"><span data-stu-id="f122b-106">VarType</span></span>         | <span data-ttu-id="f122b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f122b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f122b-108">**\_opzione dell'API WPD usare un \_ \_ \_ \_ flusso di dati chiaro \_**</span><span class="sxs-lookup"><span data-stu-id="f122b-108">**WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM**</span></span> | <span data-ttu-id="f122b-109">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="f122b-109">**VT\_BOOL**</span></span>    | <span data-ttu-id="f122b-110">Valore booleano che specifica se il flusso di dati creato per il trasferimento dei dati sarà chiaro, ovvero se il DRM non è necessario. I client possono impostare questa opzione aggiungendola alle proprietà dell'oggetto passate a [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="f122b-110">A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="f122b-111">**\_versione del servizio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f122b-111">**WPD\_SERVICE\_VERSION**</span></span>                      | <span data-ttu-id="f122b-112">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="f122b-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="f122b-113">Stringa che specifica la versione di implementazione di un determinato servizio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f122b-113">A string that specifies the implementation version of a given device service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f122b-114">**\_tipi di contenuto della cartella WPD \_ \_ \_ consentiti**</span><span class="sxs-lookup"><span data-stu-id="f122b-114">**WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED**</span></span>       | <span data-ttu-id="f122b-115">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f122b-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="f122b-116">Valore che specifica i tipi di oggetto che possono essere elementi figlio diretti di questa cartella.</span><span class="sxs-lookup"><span data-stu-id="f122b-116">A value that specifies the object types that can be direct children of this folder.</span></span> <span data-ttu-id="f122b-117">Le cartelle figlio possono avere diverse funzionalità. Questa proprietà è un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che contiene \_ i valori CLSID del VT che specificano i tipi di oggetto consentiti.</span><span class="sxs-lookup"><span data-stu-id="f122b-117">Child folders can have different capabilities.This property is an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) holding VT\_CLSID values that specify permitted object types.</span></span><br/> <span data-ttu-id="f122b-118">Per un elenco di tipi di oggetto definiti da dispositivi portatili Windows, vedere [requisiti per gli oggetti](requirements-for-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f122b-118">For a list of object types defined by Windows Portable Devices, see [Requirements for Objects](requirements-for-objects.md).</span></span><br/>                                         |
| <span data-ttu-id="f122b-119">**\_ \_ categoria oggetto funzionale \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f122b-119">**WPD\_FUNCTIONAL\_OBJECT\_CATEGORY**</span></span>          | <span data-ttu-id="f122b-120">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="f122b-120">**VT\_CLSID**</span></span>   | <span data-ttu-id="f122b-121">Valore che specifica la categoria funzionale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f122b-121">A value that specifies the object's functional category.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f122b-122">**\_ \_ profili informazioni di rendering WPD \_**</span><span class="sxs-lookup"><span data-stu-id="f122b-122">**WPD\_RENDERING\_INFORMATION\_PROFILES**</span></span>      | <span data-ttu-id="f122b-123">**VT \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f122b-123">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="f122b-124">Un [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) che contiene più interfacce [**IPortableDeviceValues**](iportabledevicevalues.md) , ognuna delle quali contiene le impostazioni delle proprietà per un profilo supportato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f122b-124">An [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) that holds multiple [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces, each of which contains the property settings for a profile that the object supports.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="f122b-125">**\_ \_ \_ \_ nome visualizzato posizione hint oggetto \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="f122b-125">**WPD\_OBJECT\_HINT\_LOCATION\_DISPLAY\_NAME**</span></span> | <span data-ttu-id="f122b-126">**\_LPWSTR VT**</span><span class="sxs-lookup"><span data-stu-id="f122b-126">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="f122b-127">Se un oggetto è un percorso di hint, questa proprietà indica il nome specifico dell'hint da visualizzare all'utente anziché il nome dell'oggetto. I driver possono specificare hint di posizione per diversi tipi di oggetto.</span><span class="sxs-lookup"><span data-stu-id="f122b-127">If an object is a hint location, this property indicates the hint-specific name to display to the user instead of the object name.Drivers can specify location hints for various object types.</span></span> <span data-ttu-id="f122b-128">Si tratta delle posizioni di archiviazione preferite per le cartelle che contengono un particolare tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="f122b-128">These are preferred storage locations for folders that hold a particular object type.</span></span> <span data-ttu-id="f122b-129">Un equivalente è la cartella immagini personali per i file di immagine in Windows.</span><span class="sxs-lookup"><span data-stu-id="f122b-129">An equivalent would be the My Pictures folder for image files in Windows.</span></span> <span data-ttu-id="f122b-130">Se questa proprietà non esiste, viene in genere usato il [ \_ \_ nome dell'oggetto WPD](object-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="f122b-130">If this property does not exist, typically the [WPD\_OBJECT\_NAME](object-properties.md) is used instead.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f122b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f122b-131">Requirements</span></span>



| <span data-ttu-id="f122b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f122b-132">Requirement</span></span> | <span data-ttu-id="f122b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f122b-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f122b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f122b-134">Header</span></span><br/> | <dl> <span data-ttu-id="f122b-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="f122b-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f122b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f122b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f122b-137">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="f122b-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




