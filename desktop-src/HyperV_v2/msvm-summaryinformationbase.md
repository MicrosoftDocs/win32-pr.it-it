---
description: Usato nel metodo GetSummaryInformation nella \_ classe MSVM VirtualSystemManagementService per recuperare rapidamente informazioni comuni correlate a un sistema virtuale o a uno snapshot.
ms.assetid: f8daa387-d812-4f44-bf5f-e0a0c18c6db8
title: Classe Msvm_SummaryInformationBase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformationBase
- Msvm_SummaryInformationBase.InstanceID
- Msvm_SummaryInformationBase.CreationTime
- Msvm_SummaryInformationBase.ElementName
- Msvm_SummaryInformationBase.EnabledState
- Msvm_SummaryInformationBase.OtherEnabledState
- Msvm_SummaryInformationBase.HealthState
- Msvm_SummaryInformationBase.Name
- Msvm_SummaryInformationBase.Notes
- Msvm_SummaryInformationBase.Version
- Msvm_SummaryInformationBase.NumberOfProcessors
- Msvm_SummaryInformationBase.OperationalStatus
- Msvm_SummaryInformationBase.StatusDescriptions
- Msvm_SummaryInformationBase.UpTime
- Msvm_SummaryInformationBase.EnhancedSessionModeState
- Msvm_SummaryInformationBase.VirtualSwitchNames
- Msvm_SummaryInformationBase.VirtualSystemSubType
- Msvm_SummaryInformationBase.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65c20239673f279babba2581c4300f373f1392bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308909"
---
# <a name="msvm_summaryinformationbase-class"></a><span data-ttu-id="0d34d-103">\_Classe MSVM SummaryInformationBase</span><span class="sxs-lookup"><span data-stu-id="0d34d-103">Msvm\_SummaryInformationBase class</span></span>

<span data-ttu-id="0d34d-104">Usato nel metodo [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) nella classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per recuperare rapidamente informazioni comuni correlate a un sistema virtuale o a uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d34d-104">Used in the [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) method in the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to quickly retrieve common information related to a virtual system or snapshot.</span></span>

<span data-ttu-id="0d34d-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0d34d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d34d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d34d-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformationBase : CIM_View
{
  string   InstanceID;
  DateTime CreationTime;
  string   ElementName;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   HealthState;
  string   Name;
  string   Notes;
  string   Version;
  uint16   NumberOfProcessors;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  uint64   UpTime;
  uint16   EnhancedSessionModeState;
  string   VirtualSwitchNames[];
  string   VirtualSystemSubType;
  string   HostComputerSystemName;
};
```

## <a name="members"></a><span data-ttu-id="0d34d-107">Members</span><span class="sxs-lookup"><span data-stu-id="0d34d-107">Members</span></span>

<span data-ttu-id="0d34d-108">La **classe \_ SummaryInformationBase di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0d34d-108">The **Msvm\_SummaryInformationBase** class has these types of members:</span></span>

-   [<span data-ttu-id="0d34d-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d34d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d34d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d34d-110">Properties</span></span>

<span data-ttu-id="0d34d-111">La **classe \_ SummaryInformationBase di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d34d-111">The **Msvm\_SummaryInformationBase** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d34d-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="0d34d-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-113">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d34d-113">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-115">Ora in cui è stato creato il sistema virtuale o lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d34d-115">The time at which the virtual system or snapshot was created.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-116">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0d34d-116">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managed. ElementName")</span><span class="sxs-lookup"><span data-stu-id="0d34d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-120">Nome descrittivo per il sistema virtuale o lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d34d-120">The friendly name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-121">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="0d34d-121">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d34d-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-124">Stato corrente del sistema virtuale o dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d34d-124">The current state of the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-125">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="0d34d-125">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-126">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d34d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-128">Indica se le connessioni in modalità avanzata sono consentite dall'host e se sono consentite, indipendentemente dal fatto che siano disponibili o meno per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-128">Indicates whether or not enhanced mode connections are allowed by the host and if allowed, whether or not they are available to the virtual machine.</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="0d34d-129">**Consentito e disponibile** (2)</span><span class="sxs-lookup"><span data-stu-id="0d34d-129">**Allowed and available** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="0d34d-130">**Non consentito** (3)</span><span class="sxs-lookup"><span data-stu-id="0d34d-130">**Not allowed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="0d34d-131">**Consentito ma non disponibile** (6)</span><span class="sxs-lookup"><span data-stu-id="0d34d-131">**Allowed but not available** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d34d-132">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="0d34d-132">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d34d-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-135">Stato di integrità corrente per il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-135">The current health state for the virtual system.</span></span> <span data-ttu-id="0d34d-136">Questa proprietà non è valida per le istanze di [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) che rappresentano uno snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-136">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-137">**HostComputerSystemName**</span><span class="sxs-lookup"><span data-stu-id="0d34d-137">**HostComputerSystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-140">Nome del computer che ospita la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-140">The name of the computer hosting this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-141">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0d34d-141">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-144">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managed. InstanceId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0d34d-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-145">InstanceID è una proprietà facoltativa che può essere utilizzata per identificare in modo opaco e univoco un'istanza di questa classe nell'ambito dello spazio dei nomi di creazione di istanze.</span><span class="sxs-lookup"><span data-stu-id="0d34d-145">InstanceID is an optional property that may be used to opaquely and uniquely identify an instance of this class within the scope of the instantiating Namespace.</span></span> <span data-ttu-id="0d34d-146">Varie sottoclassi di questa classe possono eseguire l'override di questa proprietà per renderla obbligatoria o una chiave.</span><span class="sxs-lookup"><span data-stu-id="0d34d-146">Various subclasses of this class may override this property to make it required, or a key.</span></span> <span data-ttu-id="0d34d-147">Tali sottoclassi possono anche modificare gli algoritmi preferiti per garantire l'univocità definita di seguito.</span><span class="sxs-lookup"><span data-stu-id="0d34d-147">Such subclasses may also modify the preferred algorithms for ensuring uniqueness that are defined below.</span></span>

<span data-ttu-id="0d34d-148">Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente:</span><span class="sxs-lookup"><span data-stu-id="0d34d-148">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm:</span></span>

<span data-ttu-id="0d34d-149"><OrgID>:<LocalID></span><span class="sxs-lookup"><span data-stu-id="0d34d-149"><OrgID>:<LocalID></span></span>

<span data-ttu-id="0d34d-150">Dove <OrgID> e <LocalID> sono separati da due punti (:) e dove <OrgID> devono includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità business da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="0d34d-150">Where <OrgID> and <LocalID> are separated by a colon (:), and where <OrgID> must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="0d34d-151">(Questo requisito è simile al <Schema Name> \_ <Class Name> struttura dei nomi delle classi dello schema. Per garantire l'univocità, inoltre, <OrgID> non deve contenere i due punti (:).</span><span class="sxs-lookup"><span data-stu-id="0d34d-151">(This requirement is similar to the <Schema Name>\_<Class Name> structure of Schema class names.) In addition, to ensure uniqueness, <OrgID> must not contain a colon (:).</span></span> <span data-ttu-id="0d34d-152">Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono essere compresi tra <OrgID> e <LocalID> .</span><span class="sxs-lookup"><span data-stu-id="0d34d-152">When using this algorithm, the first colon to appear in InstanceID must appear between <OrgID> and <LocalID>.</span></span>

<span data-ttu-id="0d34d-153"><LocalID> viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti.</span><span class="sxs-lookup"><span data-stu-id="0d34d-153"><LocalID> is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="0d34d-154">Se non è null e l'algoritmo "preferito" precedente non viene utilizzato, l'entità di definizione deve garantire che l'ID istanza risultante non venga riutilizzato tra le InstanceID prodotte da questo o da altri provider per lo spazio dei nomi di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="0d34d-154">If not null and the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span>

<span data-ttu-id="0d34d-155">Se non è impostato su null per le istanze definite da DMTF, è necessario usare l'algoritmo "preferito" con <OrgID> impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="0d34d-155">If not set to null for DMTF-defined instances, the "preferred" algorithm must be used with the <OrgID> set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0d34d-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-159">Nome univoco per il sistema virtuale o lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d34d-159">The unique name for the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-160">**Note**</span><span class="sxs-lookup"><span data-stu-id="0d34d-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-163">Note associate al sistema virtuale o allo snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d34d-163">The notes associated with the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-164">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="0d34d-164">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d34d-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-167">Numero totale di processori virtuali allocati al sistema virtuale o allo snapshot.</span><span class="sxs-lookup"><span data-stu-id="0d34d-167">The total number of virtual processors allocated to the virtual system or snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-168">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="0d34d-168">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-169">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d34d-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-171">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="0d34d-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-172">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0d34d-172">The current status of the element.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-173">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="0d34d-173">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-176">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="0d34d-176">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="0d34d-177">Questa proprietà deve essere impostata su null quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="0d34d-177">This property must be set to null when **EnabledState** is any value other than 1.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-178">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0d34d-178">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-179">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0d34d-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-181">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="0d34d-181">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-182">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="0d34d-182">Strings that describe the various **OperationalStatus** array values.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-183">**Tempo**</span><span class="sxs-lookup"><span data-stu-id="0d34d-183">**UpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-184">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d34d-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-186">Quantità di tempo trascorsa dall'ultimo avvio del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-186">The amount of time since the virtual system was last booted.</span></span> <span data-ttu-id="0d34d-187">Questa proprietà non è valida per le istanze di [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) che rappresentano uno snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-187">This property is not valid for instances of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) representing a virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-188">**Versione**</span><span class="sxs-lookup"><span data-stu-id="0d34d-188">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-191">Versione del sistema virtuale in formato "Major. minor"; ad esempio, "2,0".</span><span class="sxs-lookup"><span data-stu-id="0d34d-191">The version of the virtual system in a format of "major.minor"; for example, "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-192">**VirtualSwitchNames**</span><span class="sxs-lookup"><span data-stu-id="0d34d-192">**VirtualSwitchNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-193">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="0d34d-193">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-195">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="0d34d-195">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-196">Stringhe che elencano i nomi descrittivi dei commutatori virtuali a cui è connessa la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-196">Strings that list the friendly names of the virtual switches the VM is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="0d34d-197">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="0d34d-197">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d34d-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d34d-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d34d-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0d34d-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d34d-200">Sottotipo del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d34d-200">The subtype of the virtual system.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="0d34d-201">**Microsoft: Hyper-v: sottotipo: 1** ("Microsoft: Hyper-v: sottotipo: 1")</span><span class="sxs-lookup"><span data-stu-id="0d34d-201">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="0d34d-202">**Microsoft: Hyper-v: sottotipo: 2** ("Microsoft: Hyper-v: sottotipo: 2")</span><span class="sxs-lookup"><span data-stu-id="0d34d-202">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


<span data-ttu-id="0d34d-203"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0d34d-203"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0d34d-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d34d-204">Requirements</span></span>



| <span data-ttu-id="0d34d-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d34d-205">Requirement</span></span> | <span data-ttu-id="0d34d-206">Valore</span><span class="sxs-lookup"><span data-stu-id="0d34d-206">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d34d-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d34d-207">Minimum supported client</span></span><br/> | <span data-ttu-id="0d34d-208">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d34d-208">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0d34d-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d34d-209">Minimum supported server</span></span><br/> | <span data-ttu-id="0d34d-210">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0d34d-210">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0d34d-211">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d34d-211">Namespace</span></span><br/>                | <span data-ttu-id="0d34d-212">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0d34d-212">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0d34d-213">MOF</span><span class="sxs-lookup"><span data-stu-id="0d34d-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d34d-214"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d34d-214"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d34d-215">DLL</span><span class="sxs-lookup"><span data-stu-id="0d34d-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d34d-216"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d34d-216"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d34d-217">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d34d-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d34d-218">**\_Visualizzazione CIM**</span><span class="sxs-lookup"><span data-stu-id="0d34d-218">**CIM\_View**</span></span>](cim-view.md)
</dt> </dl>

 

