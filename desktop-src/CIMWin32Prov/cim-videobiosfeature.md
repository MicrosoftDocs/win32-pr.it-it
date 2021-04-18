---
description: La \_ classe CIM VideoBIOSFeature rappresenta le funzionalità del software di basso livello utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.
ms.assetid: a12ca387-5b12-487f-84fd-381afe266338
ms.tgt_platform: multiple
title: Classe CIM_VideoBIOSFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeature
- CIM_VideoBIOSFeature.Caption
- CIM_VideoBIOSFeature.CharacteristicDescriptions
- CIM_VideoBIOSFeature.Characteristics
- CIM_VideoBIOSFeature.Description
- CIM_VideoBIOSFeature.IdentifyingNumber
- CIM_VideoBIOSFeature.InstallDate
- CIM_VideoBIOSFeature.Name
- CIM_VideoBIOSFeature.ProductName
- CIM_VideoBIOSFeature.Status
- CIM_VideoBIOSFeature.Vendor
- CIM_VideoBIOSFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 45f9fd2feabdcd1f9e650e7e7a913a394e8ef67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304761"
---
# <a name="cim_videobiosfeature-class"></a><span data-ttu-id="f7726-103">CIM \_ VideoBIOSFeature (classe)</span><span class="sxs-lookup"><span data-stu-id="f7726-103">CIM\_VideoBIOSFeature class</span></span>

<span data-ttu-id="f7726-104">La classe **CIM \_ VideoBIOSFeature** rappresenta le funzionalità del software di basso livello utilizzato per configurare e accedere al controller video e alla visualizzazione di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="f7726-104">The **CIM\_VideoBIOSFeature** class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7726-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f7726-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f7726-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f7726-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f7726-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f7726-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f7726-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f7726-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7726-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7726-109">Syntax</span></span>

``` syntax
[UUID("{BAE20634-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeature : CIM_SoftwareFeature
{
  string   Caption;
  string   CharacteristicDescriptions[];
  uint16   Characteristics[];
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="f7726-110">Members</span><span class="sxs-lookup"><span data-stu-id="f7726-110">Members</span></span>

<span data-ttu-id="f7726-111">La classe **CIM \_ VideoBIOSFeature** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f7726-111">The **CIM\_VideoBIOSFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="f7726-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7726-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7726-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f7726-113">Properties</span></span>

<span data-ttu-id="f7726-114">La classe **CIM \_ VideoBIOSFeature** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f7726-114">The **CIM\_VideoBIOSFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7726-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f7726-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f7726-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-119">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7726-119">Short textual description of the object.</span></span>

<span data-ttu-id="f7726-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7726-121">**CharacteristicDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f7726-121">**CharacteristicDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-122">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="f7726-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f7726-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-124">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| video BIOS caratteristica \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**Caratteristiche**")</span><span class="sxs-lookup"><span data-stu-id="f7726-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**Characteristics**")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-125">Stringhe in formato libero che forniscono descrizioni dettagliate per le funzionalità del BIOS video indicate nella matrice di **caratteristiche** .</span><span class="sxs-lookup"><span data-stu-id="f7726-125">Free-form strings that provide detailed descriptions for the video BIOS features indicated in the **Characteristics** array.</span></span>

> [!Note]  
> <span data-ttu-id="f7726-126">Ogni voce di questa matrice è correlata alla voce nella matrice di **caratteristiche** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="f7726-126">Each entry of this array is related to the entry in the **Characteristics** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="f7726-127">**Caratteristiche**</span><span class="sxs-lookup"><span data-stu-id="f7726-127">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-128">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f7726-128">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f7726-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-130">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| video BIOS caratteristica \| 001,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VideoBIOSFeature**.**CharacteristicDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="f7726-130">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video BIOS Characteristic\|001.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoBIOSFeature**.**CharacteristicDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-131">Funzionalità supportate dal BIOS del video.</span><span class="sxs-lookup"><span data-stu-id="f7726-131">Features supported by the video BIOS.</span></span> <span data-ttu-id="f7726-132">Ad esempio, è possibile indicare il supporto per il risparmio di energia VESA o lo shadowing del BIOS del video.</span><span class="sxs-lookup"><span data-stu-id="f7726-132">For example, support for VESA power management or video BIOS shadowing could be indicated.</span></span> <span data-ttu-id="f7726-133">Il valore 3 ("Unknown") non è valido nello schema CIM perché rappresenta che non sono supportate funzionalità BIOS in DMI.</span><span class="sxs-lookup"><span data-stu-id="f7726-133">The value 3 ("Unknown") is not valid in the CIM schema since it represents that no BIOS features are supported in DMI.</span></span> <span data-ttu-id="f7726-134">In tal caso, non è necessario creare un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7726-134">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f7726-135">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f7726-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7726-136">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="f7726-136">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f7726-137">Non **definito** (3)</span><span class="sxs-lookup"><span data-stu-id="f7726-137">**Undefined** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Standard_Video_BIOS"></span><span id="standard_video_bios"></span><span id="STANDARD_VIDEO_BIOS"></span>

<span data-ttu-id="f7726-138">**BIOS video standard** (4)</span><span class="sxs-lookup"><span data-stu-id="f7726-138">**Standard Video BIOS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_BIOS_Extensions_Supported"></span><span id="vesa_bios_extensions_supported"></span><span id="VESA_BIOS_EXTENSIONS_SUPPORTED"></span>

<span data-ttu-id="f7726-139">**Estensioni BIOS VESA supportate** (5)</span><span class="sxs-lookup"><span data-stu-id="f7726-139">**VESA BIOS Extensions Supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Power_Management_Supported"></span><span id="vesa_power_management_supported"></span><span id="VESA_POWER_MANAGEMENT_SUPPORTED"></span>

<span data-ttu-id="f7726-140">Supporto per il risparmio di **energia VESA** (6)</span><span class="sxs-lookup"><span data-stu-id="f7726-140">**VESA Power Management Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA_Display_Data_Channel_Supported"></span><span id="vesa_display_data_channel_supported"></span><span id="VESA_DISPLAY_DATA_CHANNEL_SUPPORTED"></span>

<span data-ttu-id="f7726-141">**Supporto del canale dati di visualizzazione VESA** (7)</span><span class="sxs-lookup"><span data-stu-id="f7726-141">**VESA Display Data Channel Supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Shadowing_Allowed"></span><span id="video_bios_shadowing_allowed"></span><span id="VIDEO_BIOS_SHADOWING_ALLOWED"></span>

<span data-ttu-id="f7726-142">**Shadowing del BIOS video consentito** (8)</span><span class="sxs-lookup"><span data-stu-id="f7726-142">**Video BIOS Shadowing Allowed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_BIOS_Upgradeable"></span><span id="video_bios_upgradeable"></span><span id="VIDEO_BIOS_UPGRADEABLE"></span>

<span data-ttu-id="f7726-143">**Aggiornamento del BIOS video** (9)</span><span class="sxs-lookup"><span data-stu-id="f7726-143">**Video BIOS Upgradeable** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7726-144">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f7726-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-147">Qualificatori: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="f7726-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-148">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7726-148">Textual description of the object.</span></span>

<span data-ttu-id="f7726-149">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7726-150">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="f7726-150">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-153">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="f7726-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-154">Identificazione del prodotto, ad esempio un numero di serie del software o un numero di dado su un chip hardware.</span><span class="sxs-lookup"><span data-stu-id="f7726-154">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span> <span data-ttu-id="f7726-155">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-155">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7726-156">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f7726-156">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-157">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7726-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-159">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="f7726-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-160">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7726-160">Date and time the object was installed.</span></span> <span data-ttu-id="f7726-161">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="f7726-161">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f7726-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7726-163">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f7726-163">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-166">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f7726-166">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7726-167">Etichetta con cui l'oggetto è noto all'esterno del sistema di elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="f7726-167">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="f7726-168">Questa etichetta è un nome che identifica in modo univoco l'elemento nel contesto dello spazio dei nomi dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f7726-168">This label is a name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="f7726-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7726-170">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="f7726-170">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-173">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="f7726-173">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-174">Nome del prodotto comunemente usato.</span><span class="sxs-lookup"><span data-stu-id="f7726-174">Commonly used product name.</span></span>

<span data-ttu-id="f7726-175">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-175">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7726-176">**Status**</span><span class="sxs-lookup"><span data-stu-id="f7726-176">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-179">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f7726-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-180">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f7726-180">Current status of the object.</span></span> <span data-ttu-id="f7726-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f7726-182">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="f7726-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f7726-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f7726-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f7726-184">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="f7726-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f7726-185">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="f7726-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7726-186">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f7726-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f7726-187">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="f7726-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f7726-188">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="f7726-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f7726-189">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="f7726-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f7726-190">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="f7726-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f7726-191">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="f7726-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f7726-192">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="f7726-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f7726-193">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="f7726-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f7726-194">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="f7726-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7726-195">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="f7726-195">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-196">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-198">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Vendor**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="f7726-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-199">Nome del fornitore del prodotto, che corrisponde alla proprietà del **Fornitore** nell'oggetto prodotto di DMTF Solution Exchange standard (SES).</span><span class="sxs-lookup"><span data-stu-id="f7726-199">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard (SES).</span></span>

<span data-ttu-id="f7726-200">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-200">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7726-201">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f7726-201">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7726-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f7726-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7726-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f7726-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7726-204">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ prodotto CIM**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f7726-204">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f7726-205">Informazioni sulla versione del prodotto, che corrisponde alla proprietà **Version** nell'oggetto Product di DMTF ses.</span><span class="sxs-lookup"><span data-stu-id="f7726-205">Product version information, which corresponds to the **Version** property in the product object of the DMTF SES.</span></span>

<span data-ttu-id="f7726-206">Questa proprietà viene ereditata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-206">This property is inherited from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7726-207">Commenti</span><span class="sxs-lookup"><span data-stu-id="f7726-207">Remarks</span></span>

<span data-ttu-id="f7726-208">La classe **CIM \_ VideoBIOSFeature** è derivata da [**CIM \_ SoftwareFeature**](cim-softwarefeature.md).</span><span class="sxs-lookup"><span data-stu-id="f7726-208">The **CIM\_VideoBIOSFeature** class is derived from [**CIM\_SoftwareFeature**](cim-softwarefeature.md).</span></span>

<span data-ttu-id="f7726-209">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f7726-209">WMI does not implement this class.</span></span>

<span data-ttu-id="f7726-210">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f7726-210">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f7726-211">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f7726-211">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7726-212">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7726-212">Requirements</span></span>



| <span data-ttu-id="f7726-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7726-213">Requirement</span></span> | <span data-ttu-id="f7726-214">Valore</span><span class="sxs-lookup"><span data-stu-id="f7726-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7726-215">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7726-215">Minimum supported client</span></span><br/> | <span data-ttu-id="f7726-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7726-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7726-217">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7726-217">Minimum supported server</span></span><br/> | <span data-ttu-id="f7726-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7726-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7726-219">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f7726-219">Namespace</span></span><br/>                | <span data-ttu-id="f7726-220">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f7726-220">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7726-221">MOF</span><span class="sxs-lookup"><span data-stu-id="f7726-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7726-222"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7726-222"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7726-223">DLL</span><span class="sxs-lookup"><span data-stu-id="f7726-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7726-224"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7726-224"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7726-225">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7726-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7726-226">**\_SoftwareFeature CIM**</span><span class="sxs-lookup"><span data-stu-id="f7726-226">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> </dl>

 

