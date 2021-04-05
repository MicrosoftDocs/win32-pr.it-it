---
description: Rappresenta una parte gestibile o distribuibile singolarmente di un \_ SoftwareFeature CIM.
ms.assetid: 96affc55-b001-4122-b883-3610bf95a786
title: Classe CIM_SoftwareElement (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElement
- CIM_SoftwareElement.Name
- CIM_SoftwareElement.Version
- CIM_SoftwareElement.SoftwareElementState
- CIM_SoftwareElement.SoftwareElementID
- CIM_SoftwareElement.TargetOperatingSystem
- CIM_SoftwareElement.OtherTargetOS
- CIM_SoftwareElement.Manufacturer
- CIM_SoftwareElement.BuildNumber
- CIM_SoftwareElement.SerialNumber
- CIM_SoftwareElement.CodeSet
- CIM_SoftwareElement.IdentificationCode
- CIM_SoftwareElement.LanguageEdition
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1d11b428e9a17819f850ce210e6854e4f1d17e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758420"
---
# <a name="cim_softwareelement-class-hyper-v-management"></a><span data-ttu-id="f264d-103">Classe CIM_SoftwareElement (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="f264d-103">CIM_SoftwareElement class (Hyper-V management)</span></span>

<span data-ttu-id="f264d-104">Rappresenta una parte gestibile o distribuibile singolarmente di un **\_ SoftwareFeature CIM**.</span><span class="sxs-lookup"><span data-stu-id="f264d-104">Represents an individually manageable or deployable part of a **CIM\_SoftwareFeature**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f264d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f264d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Application::DeploymentModel"), AMENDMENT]
class CIM_SoftwareElement : CIM_LogicalElement
{
  string Name;
  string Version;
  uint16 SoftwareElementState;
  string SoftwareElementID;
  uint16 TargetOperatingSystem;
  string OtherTargetOS;
  string Manufacturer;
  string BuildNumber;
  string SerialNumber;
  string CodeSet;
  string IdentificationCode;
  string LanguageEdition;
};
```

## <a name="members"></a><span data-ttu-id="f264d-106">Members</span><span class="sxs-lookup"><span data-stu-id="f264d-106">Members</span></span>

<span data-ttu-id="f264d-107">La classe **CIM \_ SoftwareElement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f264d-107">The **CIM\_SoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="f264d-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f264d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f264d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f264d-109">Properties</span></span>

<span data-ttu-id="f264d-110">La classe **CIM \_ SoftwareElement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f264d-110">The **CIM\_SoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f264d-111">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="f264d-111">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-114">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informazioni sul componente software DMTF \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="f264d-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-115">Identificatore interno per la compilazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-115">The internal identifier for the compilation of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-116">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="f264d-116">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f264d-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f264d-120">Codifica dei caratteri utilizzata dall'elemento software, ad esempio UTF-8 e ISO8859-1.</span><span class="sxs-lookup"><span data-stu-id="f264d-120">The character encoding used by the software element, such as UTF-8 and ISO8859-1.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-121">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="f264d-121">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-124">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software sottocomponente DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="f264d-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-125">Identificatore del produttore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-125">The manufacturer identifier for the software element.</span></span> <span data-ttu-id="f264d-126">Si tratta spesso di una SKU (Stock Keeping Unit) o di un numero di parte.</span><span class="sxs-lookup"><span data-stu-id="f264d-126">This is often a stock keeping unit (SKU) or a part number.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-127">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="f264d-127">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-130">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software sottocomponente DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f264d-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-131">Edizione del linguaggio dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-131">The language edition of the software element.</span></span> <span data-ttu-id="f264d-132">È consigliabile utilizzare i codici di lingua definiti nello standard ISO 639.</span><span class="sxs-lookup"><span data-stu-id="f264d-132">The language codes defined in the ISO 639 standard should be used.</span></span> <span data-ttu-id="f264d-133">Se l'elemento rappresenta una versione multilingua o internazionale, è necessario utilizzare la stringa "Multilingual".</span><span class="sxs-lookup"><span data-stu-id="f264d-133">If the element represents a multi-lingual or international version, the string "Multilingual" should be used.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-134">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="f264d-134">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-137">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software sottocomponente DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f264d-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-138">Produttore dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-138">The manufacturer of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f264d-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-142">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f264d-142">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f264d-143">Nome utilizzato per identificare l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-143">The name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-144">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="f264d-144">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-147">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="f264d-147">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-148">Il produttore e il tipo di sistema operativo quando la proprietà **TargetOperatingSystem** è impostata su **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="f264d-148">The manufacturer and operating system type when the **TargetOperatingSystem** property is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="f264d-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="f264d-149">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-152">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="f264d-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-153">Numero di serie assegnato dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-153">The assigned serial number of the software element.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-154">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="f264d-154">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-157">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f264d-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f264d-158">Identificatore per l'elemento software da usare insieme ad altre chiavi per creare un'identificazione univoca dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="f264d-158">An identifier for the software element to use in conjunction with other keys to create a uniquely identify the element.</span></span>

</dd> <dt>

<span data-ttu-id="f264d-159">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="f264d-159">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-160">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f264d-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-162">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f264d-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f264d-163">Stato del ciclo di vita dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-163">The life cycle state of the software element.</span></span>

<span data-ttu-id="f264d-164">\- Un SoftwareElement nello stato distribuibile descrive i dettagli necessari per la distribuzione corretta e i dettagli (verifiche e azioni) necessari per spostarli nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f264d-164">\- A SoftwareElement in the deployable state describes the details necessary to successfully distribute it and the details (Checks and Actions) required to move it to the installable state (i.e, the next state).</span></span>

<span data-ttu-id="f264d-165">\- Un SoftwareElement nello stato installabile descrive i dettagli necessari per l'installazione corretta e i dettagli (verifiche e azioni) necessari per creare un elemento nello stato eseguibile, ad esempio lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="f264d-165">\- A SoftwareElement in the installable state describes the details necessary to successfully install it and the details (Checks and Actions) required to create an element in the executable state (i.e., the next state).</span></span>

<span data-ttu-id="f264d-166">\- Un SoftwareElement nello stato eseguibile descrive i dettagli necessari per avviarlo correttamente e i dettagli (verifiche e azioni) necessari per spostarli nello stato di esecuzione (ad esempio, lo stato successivo).</span><span class="sxs-lookup"><span data-stu-id="f264d-166">\- A SoftwareElement in the executable state describes the details necessary to successfully start it and the details (Checks and Actions) required to move it to the running state (i.e., the next state).</span></span>

<span data-ttu-id="f264d-167">\- Un oggetto SoftwareElement nello stato Running descrive i dettagli necessari per gestire l'elemento avviato.</span><span class="sxs-lookup"><span data-stu-id="f264d-167">\- A SoftwareElement in the running state describes the details necessary to manage the started element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="f264d-168">**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="f264d-168">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="f264d-169">**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="f264d-169">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="f264d-170">**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="f264d-170">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="f264d-171">**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="f264d-171">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f264d-172">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="f264d-172">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-173">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f264d-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-175">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| SubComponent Software \| 001,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="f264d-175">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](/windows/desktop/CIMWin32Prov/cim-operatingsystem).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-176">Sistema operativo dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="f264d-176">The operating system of the software element.</span></span> <span data-ttu-id="f264d-177">Il valore di questa proprietà non garantisce che si tratta di un eseguibile binario.</span><span class="sxs-lookup"><span data-stu-id="f264d-177">The value of this property does not ensure that it is binary executable.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f264d-178">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="f264d-178">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f264d-179">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="f264d-179">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="f264d-180">**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="f264d-180">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="f264d-181">**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="f264d-181">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="f264d-182">**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="f264d-182">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="f264d-183">**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="f264d-183">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Tru64_UNIX"></span><span id="tru64_unix"></span><span id="TRU64_UNIX"></span>

<span data-ttu-id="f264d-184">**Tru64 UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="f264d-184">**Tru64 UNIX** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="f264d-185">**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="f264d-185">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="f264d-186">**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="f264d-186">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="f264d-187">**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="f264d-187">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="f264d-188">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="f264d-188">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="f264d-189">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="f264d-189">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="f264d-190">**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="f264d-190">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="f264d-191">**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="f264d-191">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="f264d-192">**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="f264d-192">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="f264d-193">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="f264d-193">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="f264d-194">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="f264d-194">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="f264d-195">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="f264d-195">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="f264d-196">**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="f264d-196">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="f264d-197">**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="f264d-197">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="f264d-198">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="f264d-198">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="f264d-199">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="f264d-199">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="f264d-200">**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="f264d-200">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="f264d-201">**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="f264d-201">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="f264d-202">**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="f264d-202">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="f264d-203">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="f264d-203">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="f264d-204">**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="f264d-204">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="f264d-205">**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="f264d-205">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="f264d-206">**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="f264d-206">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="f264d-207">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="f264d-207">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="f264d-208">**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="f264d-208">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="f264d-209">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="f264d-209">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="f264d-210">**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="f264d-210">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OS"></span><span id="hp_nonstop_os"></span><span id="HP_NONSTOP_OS"></span>

<span data-ttu-id="f264d-211">**Sistema operativo HP NonStop** (33)</span><span class="sxs-lookup"><span data-stu-id="f264d-211">**HP NonStop OS** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_NonStop_OSS"></span><span id="hp_nonstop_oss"></span><span id="HP_NONSTOP_OSS"></span>

<span data-ttu-id="f264d-212">**Sistemi operativi HP NonStop** (34)</span><span class="sxs-lookup"><span data-stu-id="f264d-212">**HP NonStop OSS** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="f264d-213">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="f264d-213">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="f264d-214">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="f264d-214">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="f264d-215">**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="f264d-215">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="f264d-216">**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="f264d-216">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM"></span><span id="vm"></span>

<span data-ttu-id="f264d-217">**VM** (39)</span><span class="sxs-lookup"><span data-stu-id="f264d-217">**VM** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="f264d-218">**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="f264d-218">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="f264d-219">**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="f264d-219">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="f264d-220">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="f264d-220">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="f264d-221">**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="f264d-221">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="f264d-222">**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="f264d-222">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="f264d-223">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="f264d-223">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="f264d-224">**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="f264d-224">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="f264d-225">**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="f264d-225">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="f264d-226">**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="f264d-226">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="f264d-227">**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="f264d-227">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="f264d-228">**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="f264d-228">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="f264d-229">**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="f264d-229">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="f264d-230">**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="f264d-230">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="f264d-231">**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="f264d-231">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="f264d-232">**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="f264d-232">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="f264d-233">**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="f264d-233">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="f264d-234">**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="f264d-234">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="f264d-235">**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="f264d-235">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="f264d-236">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="f264d-236">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="f264d-237">**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="f264d-237">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="f264d-238">**Sistema operativo/390** (60)</span><span class="sxs-lookup"><span data-stu-id="f264d-238">**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="f264d-239">**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="f264d-239">**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="f264d-240">**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="f264d-240">**TPF** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows__R__Me"></span><span id="windows__r__me"></span><span id="WINDOWS__R__ME"></span>

<span data-ttu-id="f264d-241">**Windows (R) me** (63)</span><span class="sxs-lookup"><span data-stu-id="f264d-241">**Windows (R) Me** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Caldera_Open_UNIX"></span><span id="caldera_open_unix"></span><span id="CALDERA_OPEN_UNIX"></span>

<span data-ttu-id="f264d-242">**Caldera Open UNIX** (64)</span><span class="sxs-lookup"><span data-stu-id="f264d-242">**Caldera Open UNIX** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenBSD"></span><span id="openbsd"></span><span id="OPENBSD"></span>

<span data-ttu-id="f264d-243">**OpenBSD** (65)</span><span class="sxs-lookup"><span data-stu-id="f264d-243">**OpenBSD** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f264d-244">**Non applicabile** (66)</span><span class="sxs-lookup"><span data-stu-id="f264d-244">**Not Applicable** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP"></span><span id="windows_xp"></span><span id="WINDOWS_XP"></span>

<span data-ttu-id="f264d-245">**Windows XP** (67)</span><span class="sxs-lookup"><span data-stu-id="f264d-245">**Windows XP** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="z_OS"></span><span id="z_os"></span><span id="Z_OS"></span>

<span data-ttu-id="f264d-246">**z/OS** (68)</span><span class="sxs-lookup"><span data-stu-id="f264d-246">**z/OS** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003"></span><span id="microsoft_windows_server_2003"></span><span id="MICROSOFT_WINDOWS_SERVER_2003"></span>

<span data-ttu-id="f264d-247">**Microsoft Windows Server 2003** (69)</span><span class="sxs-lookup"><span data-stu-id="f264d-247">**Microsoft Windows Server 2003** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2003_64-Bit"></span><span id="microsoft_windows_server_2003_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2003_64-BIT"></span>

<span data-ttu-id="f264d-248">**Microsoft Windows Server 2003 64 bit** (70)</span><span class="sxs-lookup"><span data-stu-id="f264d-248">**Microsoft Windows Server 2003 64-Bit** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP_64-Bit"></span><span id="windows_xp_64-bit"></span><span id="WINDOWS_XP_64-BIT"></span>

<span data-ttu-id="f264d-249">**Windows XP 64 bit** (71)</span><span class="sxs-lookup"><span data-stu-id="f264d-249">**Windows XP 64-Bit** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_XP_Embedded"></span><span id="windows_xp_embedded"></span><span id="WINDOWS_XP_EMBEDDED"></span>

<span data-ttu-id="f264d-250">**Windows XP Embedded** (72)</span><span class="sxs-lookup"><span data-stu-id="f264d-250">**Windows XP Embedded** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Vista"></span><span id="windows_vista"></span><span id="WINDOWS_VISTA"></span>

<span data-ttu-id="f264d-251">**Windows Vista** (73)</span><span class="sxs-lookup"><span data-stu-id="f264d-251">**Windows Vista** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Vista_64-Bit"></span><span id="windows_vista_64-bit"></span><span id="WINDOWS_VISTA_64-BIT"></span>

<span data-ttu-id="f264d-252">**Windows Vista 64 bit** (74)</span><span class="sxs-lookup"><span data-stu-id="f264d-252">**Windows Vista 64-Bit** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_Embedded_for_Point_of_Service"></span><span id="windows_embedded_for_point_of_service"></span><span id="WINDOWS_EMBEDDED_FOR_POINT_OF_SERVICE"></span>

<span data-ttu-id="f264d-253">**Windows Embedded per punto di servizio** (75)</span><span class="sxs-lookup"><span data-stu-id="f264d-253">**Windows Embedded for Point of Service** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008"></span><span id="microsoft_windows_server_2008"></span><span id="MICROSOFT_WINDOWS_SERVER_2008"></span>

<span data-ttu-id="f264d-254">**Microsoft Windows Server 2008** (76)</span><span class="sxs-lookup"><span data-stu-id="f264d-254">**Microsoft Windows Server 2008** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_64-Bit"></span><span id="microsoft_windows_server_2008_64-bit"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_64-BIT"></span>

<span data-ttu-id="f264d-255">**Microsoft Windows Server 2008 64 bit** (77)</span><span class="sxs-lookup"><span data-stu-id="f264d-255">**Microsoft Windows Server 2008 64-Bit** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD_64-Bit"></span><span id="freebsd_64-bit"></span><span id="FREEBSD_64-BIT"></span>

<span data-ttu-id="f264d-256">**FreeBSD 64 bit** (78)</span><span class="sxs-lookup"><span data-stu-id="f264d-256">**FreeBSD 64-Bit** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux"></span><span id="redhat_enterprise_linux"></span><span id="REDHAT_ENTERPRISE_LINUX"></span>

<span data-ttu-id="f264d-257">**RedHat Enterprise Linux** (79)</span><span class="sxs-lookup"><span data-stu-id="f264d-257">**RedHat Enterprise Linux** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="RedHat_Enterprise_Linux_64-Bit"></span><span id="redhat_enterprise_linux_64-bit"></span><span id="REDHAT_ENTERPRISE_LINUX_64-BIT"></span>

<span data-ttu-id="f264d-258">**RedHat Enterprise Linux 64 bit** (80)</span><span class="sxs-lookup"><span data-stu-id="f264d-258">**RedHat Enterprise Linux 64-Bit** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris_64-Bit"></span><span id="solaris_64-bit"></span><span id="SOLARIS_64-BIT"></span>

<span data-ttu-id="f264d-259">**Solaris 64 bit** (81)</span><span class="sxs-lookup"><span data-stu-id="f264d-259">**Solaris 64-Bit** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="SUSE"></span><span id="suse"></span>

<span data-ttu-id="f264d-260">**SUSE** (82)</span><span class="sxs-lookup"><span data-stu-id="f264d-260">**SUSE** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="SUSE_64-Bit"></span><span id="suse_64-bit"></span><span id="SUSE_64-BIT"></span>

<span data-ttu-id="f264d-261">**SUSE 64 bit** (83)</span><span class="sxs-lookup"><span data-stu-id="f264d-261">**SUSE 64-Bit** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="SLES"></span><span id="sles"></span>

<span data-ttu-id="f264d-262">**SLES** (84)</span><span class="sxs-lookup"><span data-stu-id="f264d-262">**SLES** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="SLES_64-Bit"></span><span id="sles_64-bit"></span><span id="SLES_64-BIT"></span>

<span data-ttu-id="f264d-263">**SLES 64 bit** (85)</span><span class="sxs-lookup"><span data-stu-id="f264d-263">**SLES 64-Bit** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Novell_OES"></span><span id="novell_oes"></span><span id="NOVELL_OES"></span>

<span data-ttu-id="f264d-264">**Novello** (86)</span><span class="sxs-lookup"><span data-stu-id="f264d-264">**Novell OES** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Novell_Linux_Desktop"></span><span id="novell_linux_desktop"></span><span id="NOVELL_LINUX_DESKTOP"></span>

<span data-ttu-id="f264d-265">**Desktop Novell Linux** (87)</span><span class="sxs-lookup"><span data-stu-id="f264d-265">**Novell Linux Desktop** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Sun_Java_Desktop_System"></span><span id="sun_java_desktop_system"></span><span id="SUN_JAVA_DESKTOP_SYSTEM"></span>

<span data-ttu-id="f264d-266">**Sistema desktop Java Sun** (88)</span><span class="sxs-lookup"><span data-stu-id="f264d-266">**Sun Java Desktop System** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Mandriva"></span><span id="mandriva"></span><span id="MANDRIVA"></span>

<span data-ttu-id="f264d-267">**Mandriva** (89)</span><span class="sxs-lookup"><span data-stu-id="f264d-267">**Mandriva** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Mandriva_64-Bit"></span><span id="mandriva_64-bit"></span><span id="MANDRIVA_64-BIT"></span>

<span data-ttu-id="f264d-268">**Mandriva 64 bit** (90)</span><span class="sxs-lookup"><span data-stu-id="f264d-268">**Mandriva 64-Bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboLinux"></span><span id="turbolinux"></span><span id="TURBOLINUX"></span>

<span data-ttu-id="f264d-269">**TurboLinux** (91)</span><span class="sxs-lookup"><span data-stu-id="f264d-269">**TurboLinux** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="TurboLinux_64-Bit"></span><span id="turbolinux_64-bit"></span><span id="TURBOLINUX_64-BIT"></span>

<span data-ttu-id="f264d-270">**TurboLinux 64 bit** (92)</span><span class="sxs-lookup"><span data-stu-id="f264d-270">**TurboLinux 64-Bit** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Ubuntu"></span><span id="ubuntu"></span><span id="UBUNTU"></span>

<span data-ttu-id="f264d-271">**Ubuntu** (93)</span><span class="sxs-lookup"><span data-stu-id="f264d-271">**Ubuntu** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Ubuntu_64-Bit"></span><span id="ubuntu_64-bit"></span><span id="UBUNTU_64-BIT"></span>

<span data-ttu-id="f264d-272">**Ubuntu 64 bit** (94)</span><span class="sxs-lookup"><span data-stu-id="f264d-272">**Ubuntu 64-Bit** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Debian"></span><span id="debian"></span><span id="DEBIAN"></span>

<span data-ttu-id="f264d-273">**Debian** (95)</span><span class="sxs-lookup"><span data-stu-id="f264d-273">**Debian** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Debian_64-Bit"></span><span id="debian_64-bit"></span><span id="DEBIAN_64-BIT"></span>

<span data-ttu-id="f264d-274">**Debian 64 bit** (96)</span><span class="sxs-lookup"><span data-stu-id="f264d-274">**Debian 64-Bit** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x"></span><span id="linux_2.4.x"></span><span id="LINUX_2.4.X"></span>

<span data-ttu-id="f264d-275">**Linux 2.4. x** (97)</span><span class="sxs-lookup"><span data-stu-id="f264d-275">**Linux 2.4.x** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.4.x_64-Bit"></span><span id="linux_2.4.x_64-bit"></span><span id="LINUX_2.4.X_64-BIT"></span>

<span data-ttu-id="f264d-276">**Linux 2.4. x 64 bit** (98)</span><span class="sxs-lookup"><span data-stu-id="f264d-276">**Linux 2.4.x 64-Bit** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x"></span><span id="linux_2.6.x"></span><span id="LINUX_2.6.X"></span>

<span data-ttu-id="f264d-277">**Linux 2.6. x** (99)</span><span class="sxs-lookup"><span data-stu-id="f264d-277">**Linux 2.6.x** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_2.6.x_64-Bit"></span><span id="linux_2.6.x_64-bit"></span><span id="LINUX_2.6.X_64-BIT"></span>

<span data-ttu-id="f264d-278">**Linux 2.6. x 64 bit** (100)</span><span class="sxs-lookup"><span data-stu-id="f264d-278">**Linux 2.6.x 64-Bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Linux_64-Bit"></span><span id="linux_64-bit"></span><span id="LINUX_64-BIT"></span>

<span data-ttu-id="f264d-279">**Linux 64 bit** (101)</span><span class="sxs-lookup"><span data-stu-id="f264d-279">**Linux 64-Bit** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_64-Bit"></span><span id="other_64-bit"></span><span id="OTHER_64-BIT"></span>

<span data-ttu-id="f264d-280">**Altro 64 bit** (102)</span><span class="sxs-lookup"><span data-stu-id="f264d-280">**Other 64-Bit** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_Server_2008_R2"></span><span id="microsoft_windows_server_2008_r2"></span><span id="MICROSOFT_WINDOWS_SERVER_2008_R2"></span>

<span data-ttu-id="f264d-281">**Microsoft Windows Server 2008 R2** (103)</span><span class="sxs-lookup"><span data-stu-id="f264d-281">**Microsoft Windows Server 2008 R2** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="VMware_ESXi"></span><span id="vmware_esxi"></span><span id="VMWARE_ESXI"></span>

<span data-ttu-id="f264d-282">**VMware ESXi** (104)</span><span class="sxs-lookup"><span data-stu-id="f264d-282">**VMware ESXi** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Windows_7"></span><span id="microsoft_windows_7"></span><span id="MICROSOFT_WINDOWS_7"></span>

<span data-ttu-id="f264d-283">**Microsoft Windows 7** (105)</span><span class="sxs-lookup"><span data-stu-id="f264d-283">**Microsoft Windows 7** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="CentOS_32-bit"></span><span id="centos_32-bit"></span><span id="CENTOS_32-BIT"></span>

<span data-ttu-id="f264d-284">**CentOS 32 bit** (106)</span><span class="sxs-lookup"><span data-stu-id="f264d-284">**CentOS 32-bit** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="CentOS_64-bit"></span><span id="centos_64-bit"></span><span id="CENTOS_64-BIT"></span>

<span data-ttu-id="f264d-285">**CentOS 64 bit** (107)</span><span class="sxs-lookup"><span data-stu-id="f264d-285">**CentOS 64-bit** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_32-bit"></span><span id="oracle_enterprise_linux_32-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_32-BIT"></span>

<span data-ttu-id="f264d-286">**Oracle Enterprise Linux 32 bit** (108)</span><span class="sxs-lookup"><span data-stu-id="f264d-286">**Oracle Enterprise Linux 32-bit** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Oracle_Enterprise_Linux_64-bit"></span><span id="oracle_enterprise_linux_64-bit"></span><span id="ORACLE_ENTERPRISE_LINUX_64-BIT"></span>

<span data-ttu-id="f264d-287">**Oracle Enterprise Linux 64 bit** (109)</span><span class="sxs-lookup"><span data-stu-id="f264d-287">**Oracle Enterprise Linux 64-bit** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="eComStation_32-bitx"></span><span id="ecomstation_32-bitx"></span><span id="ECOMSTATION_32-BITX"></span>

<span data-ttu-id="f264d-288">**eComStation 32-BITX** (110)</span><span class="sxs-lookup"><span data-stu-id="f264d-288">**eComStation 32-bitx** (110)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f264d-289">**Versione**</span><span class="sxs-lookup"><span data-stu-id="f264d-289">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f264d-290">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f264d-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f264d-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f264d-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f264d-292">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Software sottocomponente DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="f264d-292">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|SubComponent Software \|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f264d-293">Versione del software nel formato *<Major>* . *<Minor>* .*<Revision>*</span><span class="sxs-lookup"><span data-stu-id="f264d-293">The software version in the format *<Major>*.*<Minor>*.*<Revision>*</span></span> <span data-ttu-id="f264d-294">o *<Major>* . *<Minor><letter><revision>* .</span><span class="sxs-lookup"><span data-stu-id="f264d-294">or *<Major>*.*<Minor><letter><revision>*.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f264d-295">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f264d-295">Requirements</span></span>



| <span data-ttu-id="f264d-296">Requisito</span><span class="sxs-lookup"><span data-stu-id="f264d-296">Requirement</span></span> | <span data-ttu-id="f264d-297">Valore</span><span class="sxs-lookup"><span data-stu-id="f264d-297">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f264d-298">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f264d-298">Minimum supported client</span></span><br/> | <span data-ttu-id="f264d-299">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f264d-299">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f264d-300">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f264d-300">Minimum supported server</span></span><br/> | <span data-ttu-id="f264d-301">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f264d-301">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f264d-302">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f264d-302">Namespace</span></span><br/>                | <span data-ttu-id="f264d-303">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f264d-303">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f264d-304">MOF</span><span class="sxs-lookup"><span data-stu-id="f264d-304">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f264d-305"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f264d-305"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f264d-306">DLL</span><span class="sxs-lookup"><span data-stu-id="f264d-306">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f264d-307"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f264d-307"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f264d-308">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f264d-308">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f264d-309">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="f264d-309">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

