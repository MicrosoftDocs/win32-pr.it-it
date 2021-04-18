---
description: Rappresenta le funzionalità di visualizzazione di base di un monitor del computer.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Classe WmiMonitorBasicDisplayParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315744"
---
# <a name="wmimonitorbasicdisplayparams-class"></a><span data-ttu-id="b3369-103">Classe WmiMonitorBasicDisplayParams</span><span class="sxs-lookup"><span data-stu-id="b3369-103">WmiMonitorBasicDisplayParams class</span></span>

<span data-ttu-id="b3369-104">La classe WMI **WmiMonitorBasicDisplayParams** rappresenta le funzionalità di visualizzazione di base di un monitor computer.</span><span class="sxs-lookup"><span data-stu-id="b3369-104">The **WmiMonitorBasicDisplayParams** WMI class represents the basic display features of a computer monitor.</span></span> <span data-ttu-id="b3369-105">Il valore della proprietà **VideoInputType** indica se il monitoraggio è analogico o digitale.</span><span class="sxs-lookup"><span data-stu-id="b3369-105">The value of the **VideoInputType** property indicates whether the monitor is analog or digital.</span></span> <span data-ttu-id="b3369-106">I dati in questa classe corrispondono ai dati nel blocco Basic display Parameters/features di video Electronics Standard Association (VESA) Enhanced Extended Display Data (E-EDID) standard.</span><span class="sxs-lookup"><span data-stu-id="b3369-106">Data in this class corresponds to data in the Basic Display Parameters/Features block of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3369-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3369-107">Syntax</span></span>

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a><span data-ttu-id="b3369-108">Members</span><span class="sxs-lookup"><span data-stu-id="b3369-108">Members</span></span>

<span data-ttu-id="b3369-109">La classe **WmiMonitorBasicDisplayParams** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3369-109">The **WmiMonitorBasicDisplayParams** class has these types of members:</span></span>

-   [<span data-ttu-id="b3369-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3369-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3369-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3369-111">Properties</span></span>

<span data-ttu-id="b3369-112">La classe **WmiMonitorBasicDisplayParams** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3369-112">The **WmiMonitorBasicDisplayParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3369-113">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="b3369-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3369-114">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b3369-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3369-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3369-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3369-116">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="b3369-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b3369-117">**DisplayTransferCharacteristic**</span><span class="sxs-lookup"><span data-stu-id="b3369-117">**DisplayTransferCharacteristic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3369-118">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b3369-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3369-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3369-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3369-120">Caratteristica di trasferimento di visualizzazione (100 \* gamma-100).</span><span class="sxs-lookup"><span data-stu-id="b3369-120">Display transfer characteristic (100\*Gamma-100).</span></span>

</dd> <dt>

<span data-ttu-id="b3369-121">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="b3369-121">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3369-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3369-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3369-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3369-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3369-124">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b3369-124">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b3369-125">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="b3369-125">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="b3369-126">**MaxHorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="b3369-126">**MaxHorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3369-127">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b3369-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3369-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3369-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3369-129">Dimensioni massime dell'immagine orizzontale in centimetri.</span><span class="sxs-lookup"><span data-stu-id="b3369-129">Maximum horizontal image size in centimeters.</span></span> <span data-ttu-id="b3369-130">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b3369-130">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3369-131">**MaxVerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="b3369-131">**MaxVerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3369-132">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b3369-132">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3369-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3369-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3369-134">Dimensioni massime dell'immagine verticale in centimetri.</span><span class="sxs-lookup"><span data-stu-id="b3369-134">Maximum vertical image size in centimeters.</span></span> <span data-ttu-id="b3369-135">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b3369-135">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3369-136">**SupportedDisplayFeatures**</span><span class="sxs-lookup"><span data-stu-id="b3369-136">**SupportedDisplayFeatures**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3369-137">Tipo di dati: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span><span class="sxs-lookup"><span data-stu-id="b3369-137">Data type: **[**SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**</span></span>
</dt> <dt>

<span data-ttu-id="b3369-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3369-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3369-139">Visualizza le funzionalità supportate dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b3369-139">Display features supported by the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="b3369-140">**VideoInputType**</span><span class="sxs-lookup"><span data-stu-id="b3369-140">**VideoInputType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3369-141">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b3369-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b3369-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3369-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3369-143">Tipo di input video.</span><span class="sxs-lookup"><span data-stu-id="b3369-143">Video input type.</span></span>



| <span data-ttu-id="b3369-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b3369-144">Value</span></span>                                                                              | <span data-ttu-id="b3369-145">Significato</span><span class="sxs-lookup"><span data-stu-id="b3369-145">Meaning</span></span>            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="b3369-146"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b3369-146"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="b3369-147">Analogico</span><span class="sxs-lookup"><span data-stu-id="b3369-147">Analog</span></span><br/>  |
| <dl> <span data-ttu-id="b3369-148"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="b3369-148"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="b3369-149">Digitale</span><span class="sxs-lookup"><span data-stu-id="b3369-149">Digital</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3369-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3369-150">Remarks</span></span>

<span data-ttu-id="b3369-151">**MaxHorizontalImageSize** e **MaxVerticalImageSize** rappresentano le dimensioni massime dell'immagine che il monitoraggio è in grado di visualizzare correttamente per l'intero set di combinazioni di formato e temporizzazione supportate.</span><span class="sxs-lookup"><span data-stu-id="b3369-151">**MaxHorizontalImageSize** and **MaxVerticalImageSize** represent the maximum image dimensions that the monitor can correctly display for the entire set of supported timing and format combinations.</span></span> <span data-ttu-id="b3369-152">La dimensione massima dell'immagine è definita dallo standard VIAD (video image area Definition) VESA ed è arrotondata al centimetro più vicino.</span><span class="sxs-lookup"><span data-stu-id="b3369-152">The maximum image dimension is defined by VESA Video Image Area Definition (VIAD) Standard and is rounded to the nearest centimeter.</span></span> <span data-ttu-id="b3369-153">Il computer host può usare questi dati per selezionare le dimensioni e le proporzioni dell'immagine che consentiranno il testo ridimensionato correttamente.</span><span class="sxs-lookup"><span data-stu-id="b3369-153">The host computer system can use this data to select the image size and aspect ratio that will allow properly scaled text.</span></span> <span data-ttu-id="b3369-154">Tenere presente che, se uno o entrambi i campi sono pari a zero, il sistema non prevede alcuna supposizione sulle dimensioni di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b3369-154">Be aware that, if either or both of these fields are zero, then the system makes no assumptions about the display size.</span></span> <span data-ttu-id="b3369-155">Ad esempio, le dimensioni di una visualizzazione di proiezione potrebbero non essere determinate.</span><span class="sxs-lookup"><span data-stu-id="b3369-155">For example, the size of a projection display may be undetermined.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3369-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3369-156">Requirements</span></span>



| <span data-ttu-id="b3369-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3369-157">Requirement</span></span> | <span data-ttu-id="b3369-158">Valore</span><span class="sxs-lookup"><span data-stu-id="b3369-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3369-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3369-159">Minimum supported client</span></span><br/> | <span data-ttu-id="b3369-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3369-160">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b3369-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3369-161">Minimum supported server</span></span><br/> | <span data-ttu-id="b3369-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3369-162">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b3369-163">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3369-163">Namespace</span></span><br/>                | <span data-ttu-id="b3369-164">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="b3369-164">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b3369-165">MOF</span><span class="sxs-lookup"><span data-stu-id="b3369-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3369-166"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3369-166"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3369-167">DLL</span><span class="sxs-lookup"><span data-stu-id="b3369-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3369-168"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3369-168"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3369-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3369-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3369-170">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="b3369-170">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




