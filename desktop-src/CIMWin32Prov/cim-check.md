---
description: La \_ classe CIM check rappresenta una condizione o una caratteristica che dovrebbe essere true in un ambiente definito o con ambito da un'istanza di una classe CIM \_ ComputerSystem.
ms.assetid: f7862fe5-4412-4d57-b5fa-03c939ddba02
ms.tgt_platform: multiple
title: Classe CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check
- CIM_Check.CheckID
- CIM_Check.Caption
- CIM_Check.Description
- CIM_Check.CheckMode
- CIM_Check.Name
- CIM_Check.TargetOperatingSystem
- CIM_Check.Version
- CIM_Check.SoftwareElementID
- CIM_Check.SoftwareElementState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cbe742fb4cd2510ec4c502f89b3b3b1eb79bc47
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877993"
---
# <a name="cim_check-class"></a><span data-ttu-id="a4a5b-103">\_Classe di controllo CIM</span><span class="sxs-lookup"><span data-stu-id="a4a5b-103">CIM\_Check class</span></span>

<span data-ttu-id="a4a5b-104">La classe **CIM \_ Check** rappresenta una condizione o una caratteristica che dovrebbe essere true in un ambiente definito o con ambito da un'istanza di una classe [**CIM \_ ComputerSystem**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a5b-104">The **CIM\_Check** class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="a4a5b-105">I controlli associati a un particolare elemento software sono organizzati in uno dei due gruppi usando la proprietà **Phase** dell'associazione [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a5b-105">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

<span data-ttu-id="a4a5b-106">Le condizioni che devono essere soddisfatte quando un elemento software si trova in un determinato ambiente sono note come condizioni in stato.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-106">Conditions that are expected to be satisfied when a software element is in a particular environment are known as in-state conditions.</span></span> <span data-ttu-id="a4a5b-107">Le condizioni che devono essere soddisfatte per la transizione dell'elemento software corrente allo stato successivo sono note come condizioni di stato successivo.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-107">Conditions that must be satisfied to transition the current software element to its next state are known as next-state conditions.</span></span>

<span data-ttu-id="a4a5b-108">Un [**oggetto \_ ComputerSystem CIM**](cim-computersystem.md) rappresenta l'ambiente in cui è già installato un [**CIM \_ SoftwareElement**](cim-softwareelement.md) o in cui verrà installato **un \_ software CIM** .</span><span class="sxs-lookup"><span data-stu-id="a4a5b-108">A [**CIM\_ComputerSystem**](cim-computersystem.md) object represents the environment in which a [**CIM\_SoftwareElement**](cim-softwareelement.md) is already installed, or in which a **CIM\_SoftwareElement** will be installed.</span></span> <span data-ttu-id="a4a5b-109">Per il caso in cui un elemento software è già installato, l'associazione [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) viene utilizzata per identificare l'oggetto **CIM \_ ComputerSystem** che rappresenta l'"ambiente".</span><span class="sxs-lookup"><span data-stu-id="a4a5b-109">For the case in which a software element is already installed, the [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) association is used to identify the **CIM\_ComputerSystem** object that represents the "environment."</span></span> <span data-ttu-id="a4a5b-110">Quando un elemento software viene distribuito e installato in un computer diverso, l'oggetto **\_ ComputerSystem CIM** per il sistema di destinazione è l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-110">When a software element is being distributed and installed on a different computer, the **CIM\_ComputerSystem** object for the targeted system is the environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4a5b-111">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a4a5b-112">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a4a5b-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a4a5b-113">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a4a5b-114">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4a5b-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4a5b-115">Syntax</span></span>

``` syntax
[UUID("{7A9135CA-DB21-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
};
```

## <a name="members"></a><span data-ttu-id="a4a5b-116">Members</span><span class="sxs-lookup"><span data-stu-id="a4a5b-116">Members</span></span>

<span data-ttu-id="a4a5b-117">La classe **CIM \_ Check** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a4a5b-117">The **CIM\_Check** class has these types of members:</span></span>

-   [<span data-ttu-id="a4a5b-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4a5b-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="a4a5b-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4a5b-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a4a5b-120">Metodi</span><span class="sxs-lookup"><span data-stu-id="a4a5b-120">Methods</span></span>

<span data-ttu-id="a4a5b-121">La classe **CIM \_ Check** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-121">The **CIM\_Check** class has these methods.</span></span>



| <span data-ttu-id="a4a5b-122">Metodo</span><span class="sxs-lookup"><span data-stu-id="a4a5b-122">Method</span></span>                                             | <span data-ttu-id="a4a5b-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4a5b-123">Description</span></span>                                                   |
|:---------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="a4a5b-124">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-124">**Invoke**</span></span>](invoke-method-in-class-cim-check.md) | <span data-ttu-id="a4a5b-125">Esegue una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-125">Takes a particular action.</span></span> <span data-ttu-id="a4a5b-126">Non implementato da WMI.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a4a5b-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a4a5b-127">Properties</span></span>

<span data-ttu-id="a4a5b-128">La classe **CIM \_ Check** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-128">The **CIM\_Check** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4a5b-129">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-129">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-132">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-132">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-133">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-133">A short textual description of the subject.</span></span>

</dd> <dt>

<span data-ttu-id="a4a5b-134">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-134">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-137">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-138">Identificatore utilizzato insieme ad altre chiavi per identificare in modo univoco il controllo.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-138">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

</dd> <dt>

<span data-ttu-id="a4a5b-139">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-139">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-140">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-142">Se **true**, la condizione dovrebbe esistere nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-142">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="a4a5b-143">Un file, ad esempio, dovrebbe trovarsi in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-143">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="a4a5b-144">Se **false**, la condizione non è prevista.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-144">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="a4a5b-145">Un file, ad esempio, non si trova in un sistema, quindi il metodo [**Invoke**](invoke-method-in-class-cim-check.md) deve restituire **false**.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-145">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a4a5b-146">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-149">Descrizione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-149">A description of the objects.</span></span>

</dd> <dt>

<span data-ttu-id="a4a5b-150">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-153">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Nome**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-153">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-154">Nome utilizzato per identificare l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-154">Name used to identify the software element.</span></span>

</dd> <dt>

<span data-ttu-id="a4a5b-155">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-155">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-158">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-158">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-159">Si tratta di un identificatore per questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-159">This is an identifier for this software element.</span></span>

</dd> <dt>

<span data-ttu-id="a4a5b-160">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-160">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-163">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-163">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-164">Stato dell'elemento software di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-164">The software element state of a software element.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="a4a5b-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Distribuibile** (0)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-165"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-166">Vengono descritti i dettagli necessari per la corretta distribuzione e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato installabile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-166">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="a4a5b-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installabile** (1)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-167"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-168">Vengono descritti i dettagli necessari per l'installazione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato eseguibile, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-168">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="a4a5b-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Eseguibile** (2)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-169"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-170">Vengono descritti i dettagli necessari per l'esecuzione corretta e i dettagli (condizioni e azioni) necessari per creare un elemento software nello stato di esecuzione, ovvero lo stato successivo.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-170">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="a4a5b-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**In esecuzione** (3)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-171"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-172">Vengono descritti i dettagli necessari per il monitoraggio e l'utilizzo di un elemento iniziale.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-172">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a4a5b-173">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-173">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-174">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-176">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chiave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informazioni sul componente software DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="a4a5b-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-177">Sistema operativo di destinazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-177">Target operating system of the software element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a4a5b-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a4a5b-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="a4a5b-180"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-180"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-181">Mac OS</span><span class="sxs-lookup"><span data-stu-id="a4a5b-181">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="a4a5b-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-182"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-183">UNIX ATT</span><span class="sxs-lookup"><span data-stu-id="a4a5b-183">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="a4a5b-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-184"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="a4a5b-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-185"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="a4a5b-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-186"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="a4a5b-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-187"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-188">Apri VM</span><span class="sxs-lookup"><span data-stu-id="a4a5b-188">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="a4a5b-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-189"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-190">HP-UX</span><span class="sxs-lookup"><span data-stu-id="a4a5b-190">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="a4a5b-191"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-191"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="a4a5b-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-192"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="a4a5b-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-193"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="a4a5b-194"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-194"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="a4a5b-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-195"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-196">Macchina virtuale Microsoft (VM) per Java</span><span class="sxs-lookup"><span data-stu-id="a4a5b-196">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="a4a5b-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-197"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="a4a5b-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-198"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-199">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="a4a5b-199">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="a4a5b-200"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-200"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-201">Windows 95</span><span class="sxs-lookup"><span data-stu-id="a4a5b-201">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="a4a5b-202"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-202"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-203">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a4a5b-203">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="a4a5b-204"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-204"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-205">Windows NT</span><span class="sxs-lookup"><span data-stu-id="a4a5b-205">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="a4a5b-206"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-206"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-207">Windows CE</span><span class="sxs-lookup"><span data-stu-id="a4a5b-207">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="a4a5b-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-208"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-209">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="a4a5b-209">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="a4a5b-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-210"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="a4a5b-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-211"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="a4a5b-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-212"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="a4a5b-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-213"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="a4a5b-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-214"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="a4a5b-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-215"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="a4a5b-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-216"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="a4a5b-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-217"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="a4a5b-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-218"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="a4a5b-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-219"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="a4a5b-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-220"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="a4a5b-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-221"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-222">Serie A</span><span class="sxs-lookup"><span data-stu-id="a4a5b-222">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="a4a5b-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-223"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-224">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="a4a5b-224">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="a4a5b-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-225"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-226">NT tandem</span><span class="sxs-lookup"><span data-stu-id="a4a5b-226">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="a4a5b-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-227"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-228">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="a4a5b-228">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="a4a5b-229"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-229"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="a4a5b-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-230"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="a4a5b-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-231"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="a4a5b-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-232"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="a4a5b-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-233"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="a4a5b-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-234"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-235">UNIX BSD</span><span class="sxs-lookup"><span data-stu-id="a4a5b-235">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="a4a5b-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-236"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="a4a5b-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-237"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="a4a5b-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-238"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="a4a5b-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-239"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-240">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="a4a5b-240">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="a4a5b-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-241"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="a4a5b-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-242"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="a4a5b-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-243"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="a4a5b-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-244"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="a4a5b-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-245"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="a4a5b-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-246"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="a4a5b-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-247"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="a4a5b-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-248"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="a4a5b-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-249"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="a4a5b-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-250"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="a4a5b-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-251"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="a4a5b-252">Sistema operativo Palm</span><span class="sxs-lookup"><span data-stu-id="a4a5b-252">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="a4a5b-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-253"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="a4a5b-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-254"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="a4a5b-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-255"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="a4a5b-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-256"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="a4a5b-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-257"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a4a5b-258">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-258">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4a5b-259">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a4a5b-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a4a5b-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4a5b-261">Qualificatori: [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="a4a5b-261">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a4a5b-262">Versione dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-262">Version of the operation.</span></span>

<span data-ttu-id="a4a5b-263">La versione dell'operazione deve essere in uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="a4a5b-263">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="a4a5b-264"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="a4a5b-264"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="a4a5b-265"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="a4a5b-265"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4a5b-266">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4a5b-266">Remarks</span></span>

<span data-ttu-id="a4a5b-267">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-267">WMI does not implement this class.</span></span> <span data-ttu-id="a4a5b-268">Per ulteriori informazioni sulle classi derivate dal **\_ controllo CIM**, vedere [classi Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a4a5b-268">For more information about classes derived from **CIM\_Check**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a4a5b-269">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-269">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a4a5b-270">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-270">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4a5b-271">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4a5b-271">Requirements</span></span>



| <span data-ttu-id="a4a5b-272">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4a5b-272">Requirement</span></span> | <span data-ttu-id="a4a5b-273">Valore</span><span class="sxs-lookup"><span data-stu-id="a4a5b-273">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a5b-274">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4a5b-274">Minimum supported client</span></span><br/> | <span data-ttu-id="a4a5b-275">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4a5b-275">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4a5b-276">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4a5b-276">Minimum supported server</span></span><br/> | <span data-ttu-id="a4a5b-277">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4a5b-277">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4a5b-278">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a4a5b-278">Namespace</span></span><br/>                | <span data-ttu-id="a4a5b-279">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a4a5b-279">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4a5b-280">MOF</span><span class="sxs-lookup"><span data-stu-id="a4a5b-280">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4a5b-281"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4a5b-281"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4a5b-282">DLL</span><span class="sxs-lookup"><span data-stu-id="a4a5b-282">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4a5b-283"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4a5b-283"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

