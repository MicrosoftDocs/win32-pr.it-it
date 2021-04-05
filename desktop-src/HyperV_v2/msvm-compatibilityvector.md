---
description: Fa riferimento alle informazioni di compatibilità per una macchina virtuale (VM) (quando viene eseguita in un computer VM) o in un host (se eseguita in un computer host).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Classe Msvm_CompatibilityVector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883057"
---
# <a name="msvm_compatibilityvector-class"></a><span data-ttu-id="c08d5-103">\_Classe MSVM CompatibilityVector</span><span class="sxs-lookup"><span data-stu-id="c08d5-103">Msvm\_CompatibilityVector class</span></span>

<span data-ttu-id="c08d5-104">Fa riferimento alle informazioni di compatibilità per una macchina virtuale (VM) (quando viene eseguita in un computer VM) o in un host (se eseguita in un computer host).</span><span class="sxs-lookup"><span data-stu-id="c08d5-104">References the compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span>

<span data-ttu-id="c08d5-105">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c08d5-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c08d5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c08d5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a><span data-ttu-id="c08d5-107">Members</span><span class="sxs-lookup"><span data-stu-id="c08d5-107">Members</span></span>

<span data-ttu-id="c08d5-108">La **classe \_ CompatibilityVector di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c08d5-108">The **Msvm\_CompatibilityVector** class has these types of members:</span></span>

-   [<span data-ttu-id="c08d5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c08d5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c08d5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c08d5-110">Properties</span></span>

<span data-ttu-id="c08d5-111">La **classe \_ CompatibilityVector di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c08d5-111">The **Msvm\_CompatibilityVector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c08d5-112">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="c08d5-112">**CompareOperation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08d5-113">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c08d5-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c08d5-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08d5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08d5-115">Identifica l'operazione di confronto che restituirà true solo se due vettori sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="c08d5-115">Identifies the comparison operation that will return true if and only if two vectors are compatible.</span></span> <span data-ttu-id="c08d5-116">I dati della macchina virtuale si trovano sul lato sinistro del confronto e i dati dell'host si trovano sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="c08d5-116">The VM's data is on the left hand side of the comparison, and the host's data is on the right hand side.</span></span>

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

<span data-ttu-id="c08d5-117">**Uguale** a (0)</span><span class="sxs-lookup"><span data-stu-id="c08d5-117">**Equal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

<span data-ttu-id="c08d5-118">**Superset** (1)</span><span class="sxs-lookup"><span data-stu-id="c08d5-118">**Superset** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

<span data-ttu-id="c08d5-119">**Subset** (2)</span><span class="sxs-lookup"><span data-stu-id="c08d5-119">**Subset** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

<span data-ttu-id="c08d5-120">Non **contiguo** (3)</span><span class="sxs-lookup"><span data-stu-id="c08d5-120">**Disjoint** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

<span data-ttu-id="c08d5-121">**GreaterThan** (4)</span><span class="sxs-lookup"><span data-stu-id="c08d5-121">**GreaterThan** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

<span data-ttu-id="c08d5-122">**GreaterThanOrEqual** (5)</span><span class="sxs-lookup"><span data-stu-id="c08d5-122">**GreaterThanOrEqual** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

<span data-ttu-id="c08d5-123">**LessThan** (6)</span><span class="sxs-lookup"><span data-stu-id="c08d5-123">**LessThan** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

<span data-ttu-id="c08d5-124">**LessThanOrEqual** (7)</span><span class="sxs-lookup"><span data-stu-id="c08d5-124">**LessThanOrEqual** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

<span data-ttu-id="c08d5-125">**Multiple** (8)</span><span class="sxs-lookup"><span data-stu-id="c08d5-125">**Multiple** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

<span data-ttu-id="c08d5-126">**Divisibile** (9)</span><span class="sxs-lookup"><span data-stu-id="c08d5-126">**Divisible** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c08d5-127">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="c08d5-127">**CompatibilityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08d5-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c08d5-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c08d5-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08d5-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08d5-130">Dati effettivi sugli attributi di compatibilità utilizzati per il confronto.</span><span class="sxs-lookup"><span data-stu-id="c08d5-130">The actual compatibility attribute data that is used for comparison.</span></span>

</dd> <dt>

<span data-ttu-id="c08d5-131">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="c08d5-131">**VectorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c08d5-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c08d5-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c08d5-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c08d5-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c08d5-134">Identifica un vettore di compatibilità che rappresenta un attributo specifico.</span><span class="sxs-lookup"><span data-stu-id="c08d5-134">Identifies a compatibility vector that represents a specific attribute.</span></span> <span data-ttu-id="c08d5-135">Questa proprietà viene usata per trovare la corrispondenza con i vettori corrispondenti tra un host e una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c08d5-135">This property is used to match corresponding vectors between a host and a VM.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c08d5-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="c08d5-136">Remarks</span></span>

<span data-ttu-id="c08d5-137">Il metodo [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) della classe [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) restituisce una matrice di istanze di **MSVM \_ CompatibilityVector** per l'host (se eseguita nell'host) o una macchina virtuale (se eseguita nella macchina virtuale).</span><span class="sxs-lookup"><span data-stu-id="c08d5-137">The [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class returns an array of **Msvm\_CompatibilityVector** instances for the host (if run on the host) or a VM (if run on the VM).</span></span> <span data-ttu-id="c08d5-138">Ogni voce **MSVM \_ CompatibilityVector** nell'elenco descrive un vettore di attributi di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="c08d5-138">Each **Msvm\_CompatibilityVector** entry in the list describes a compatibility attribute vector.</span></span> <span data-ttu-id="c08d5-139">Affinché una macchina virtuale sia compatibile con un host, è necessario che tutti gli attributi di compatibilità siano compatibili con gli attributi dell'host.</span><span class="sxs-lookup"><span data-stu-id="c08d5-139">For a VM to be compatible with a host, all of its compatibility attributes must be compatible with the host s attributes.</span></span>

<span data-ttu-id="c08d5-140">Ogni voce **MSVM \_ CompatibilityVector** presenta le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="c08d5-140">Each **Msvm\_CompatibilityVector** entry has these properties:</span></span>

<dl> <dt>

<span data-ttu-id="c08d5-141">**VectorId**</span><span class="sxs-lookup"><span data-stu-id="c08d5-141">**VectorId**</span></span>
</dt> <dd>

<span data-ttu-id="c08d5-142">Identifica in modo univoco il vettore di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="c08d5-142">Uniquely identifies the compatibility vector.</span></span> <span data-ttu-id="c08d5-143">Viene usato per trovare la corrispondenza con i vettori da confrontare tra un host e una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c08d5-143">This is used to match the vectors to compare between a host and a VM.</span></span>

</dd> <dt>

<span data-ttu-id="c08d5-144">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="c08d5-144">**CompareOperation**</span></span>
</dt> <dd>

<span data-ttu-id="c08d5-145">Identifica l'operazione di confronto che determina se i vettori sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="c08d5-145">Identifies the comparison operation that determines whether the vectors are compatible.</span></span>

</dd> <dt>

<span data-ttu-id="c08d5-146">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="c08d5-146">**CompatibilityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c08d5-147">Contiene l'attributo di compatibilità effettivo. Si tratta in effetti del payload dell'attributo, ad esempio maschera della funzionalità del processore, dimensioni di scaricamento della riga della cache e così via.</span><span class="sxs-lookup"><span data-stu-id="c08d5-147">Contains the actual compatibility attribute; This is effectively the attribute payload (e.g. processor feature mask, cache line flush size, etc.)</span></span>

</dd> </dl>

<span data-ttu-id="c08d5-148">Il set di operazioni definito per **CompareOperation** implica solo il confronto di base di interi e la logica bit per bit.</span><span class="sxs-lookup"><span data-stu-id="c08d5-148">The set of operations defined for **CompareOperation** just involve basic integer comparison and bitwise logic.</span></span> <span data-ttu-id="c08d5-149">Ciò consente al contenuto effettivo di **CompatibilityInfo** di rimanere opaco.</span><span class="sxs-lookup"><span data-stu-id="c08d5-149">This enables the actual contents of **CompatibilityInfo** to remain opaque.</span></span> <span data-ttu-id="c08d5-150">Il set di operazioni include:</span><span class="sxs-lookup"><span data-stu-id="c08d5-150">The set of operations include:</span></span>



| <span data-ttu-id="c08d5-151">CompareOperation</span><span class="sxs-lookup"><span data-stu-id="c08d5-151">CompareOperation</span></span> | <span data-ttu-id="c08d5-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c08d5-152">Description</span></span>                                      | <span data-ttu-id="c08d5-153">Confronto di pseudocodice</span><span class="sxs-lookup"><span data-stu-id="c08d5-153">Pseudocode Comparison</span></span>                |
|------------------|--------------------------------------------------|--------------------------------------|
| <span data-ttu-id="c08d5-154">VmCcEqual</span><span class="sxs-lookup"><span data-stu-id="c08d5-154">VmCcEqual</span></span>        | <span data-ttu-id="c08d5-155">VmAttr deve essere uguale a HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-155">VmAttr must equal HostAttr</span></span>                       | <span data-ttu-id="c08d5-156">If (VmAttr = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="c08d5-156">If (VmAttr == HostAttr)</span></span>              |
| <span data-ttu-id="c08d5-157">VmCcSuperSet</span><span class="sxs-lookup"><span data-stu-id="c08d5-157">VmCcSuperSet</span></span>     | <span data-ttu-id="c08d5-158">VmAttr deve essere un superset di HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-158">VmAttr must be a superset of HostAttr</span></span>            | <span data-ttu-id="c08d5-159">If ((VmAttr & HostAttr) = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="c08d5-159">If ((VmAttr & HostAttr) == HostAttr)</span></span> |
| <span data-ttu-id="c08d5-160">VmCcSubSet</span><span class="sxs-lookup"><span data-stu-id="c08d5-160">VmCcSubSet</span></span>       | <span data-ttu-id="c08d5-161">VmAttr deve essere un subset di HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-161">VmAttr must be a subset of HostAttr</span></span>              | <span data-ttu-id="c08d5-162">If ((VmAttr & HostAttr) = = VmAttr)</span><span class="sxs-lookup"><span data-stu-id="c08d5-162">If ((VmAttr & HostAttr) == VmAttr)</span></span>   |
| <span data-ttu-id="c08d5-163">VmCcDisjointSet</span><span class="sxs-lookup"><span data-stu-id="c08d5-163">VmCcDisjointSet</span></span>  | <span data-ttu-id="c08d5-164">VmAttr deve essere un set non contiguo da HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-164">VmAttr must be a disjoint set from HostAttr</span></span>      | <span data-ttu-id="c08d5-165">If ((VmAttr & HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="c08d5-165">If ((VmAttr & HostAttr) == 0)</span></span>        |
| <span data-ttu-id="c08d5-166">VmCcGreater</span><span class="sxs-lookup"><span data-stu-id="c08d5-166">VmCcGreater</span></span>      | <span data-ttu-id="c08d5-167">VmAttr deve essere maggiore di HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-167">VmAttr must be greater than HostAttr</span></span>             | <span data-ttu-id="c08d5-168">If (VmAttr > HostAttr)</span><span class="sxs-lookup"><span data-stu-id="c08d5-168">If (VmAttr > HostAttr)</span></span>            |
| <span data-ttu-id="c08d5-169">VmCcGreaterEqual</span><span class="sxs-lookup"><span data-stu-id="c08d5-169">VmCcGreaterEqual</span></span> | <span data-ttu-id="c08d5-170">VmAttr deve essere maggiore o uguale a HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-170">VmAttr must be greater than or equal to HostAttr</span></span> | <span data-ttu-id="c08d5-171">If (VmAttr >= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="c08d5-171">If (VmAttr >= HostAttr)</span></span>           |
| <span data-ttu-id="c08d5-172">VmCcLess</span><span class="sxs-lookup"><span data-stu-id="c08d5-172">VmCcLess</span></span>         | <span data-ttu-id="c08d5-173">VmAttr deve essere minore di HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-173">VmAttr must be less than HostAttr</span></span>                | <span data-ttu-id="c08d5-174">If (VmAttr < HostAttr)</span><span class="sxs-lookup"><span data-stu-id="c08d5-174">If (VmAttr < HostAttr)</span></span>            |
| <span data-ttu-id="c08d5-175">VmCcLessEqual</span><span class="sxs-lookup"><span data-stu-id="c08d5-175">VmCcLessEqual</span></span>    | <span data-ttu-id="c08d5-176">VmAttr deve essere minore o uguale a HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-176">VmAttr must be less than or equal to HostAttr</span></span>    | <span data-ttu-id="c08d5-177">If (VmAttr <= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="c08d5-177">If (VmAttr <= HostAttr)</span></span>           |
| <span data-ttu-id="c08d5-178">VmCcMultiple</span><span class="sxs-lookup"><span data-stu-id="c08d5-178">VmCcMultiple</span></span>     | <span data-ttu-id="c08d5-179">VmAttr deve essere un multiplo di HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-179">VmAttr must be a multiple of HostAttr</span></span>            | <span data-ttu-id="c08d5-180">If ((VmAttr% HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="c08d5-180">If ((VmAttr % HostAttr) == 0)</span></span>        |
| <span data-ttu-id="c08d5-181">VmCcDivisor</span><span class="sxs-lookup"><span data-stu-id="c08d5-181">VmCcDivisor</span></span>      | <span data-ttu-id="c08d5-182">VmAttr deve essere un divisore di HostAttr</span><span class="sxs-lookup"><span data-stu-id="c08d5-182">VmAttr must be a divisor of HostAttr</span></span>             | <span data-ttu-id="c08d5-183">If ((HostAttr% VmAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="c08d5-183">If ((HostAttr % VmAttr) == 0)</span></span>        |



 

<span data-ttu-id="c08d5-184">SCVMM deve eseguire questi passaggi per determinare se una macchina virtuale è compatibile con un host.</span><span class="sxs-lookup"><span data-stu-id="c08d5-184">SCVMM needs to do these steps to determine whether a VM is compatible with a host.</span></span>

<span data-ttu-id="c08d5-185">**Per determinare se una macchina virtuale è compatibile con un host**</span><span class="sxs-lookup"><span data-stu-id="c08d5-185">**To determine whether a VM is compatible with a host**</span></span>

1.  <span data-ttu-id="c08d5-186">Scorrere tutti gli elementi **\_ CompatibilityVector di MSVM** per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c08d5-186">Iterate through all of the **Msvm\_CompatibilityVector** elements for the VM.</span></span>
2.  <span data-ttu-id="c08d5-187">Per ogni **elemento \_ CompatibilityVector di MSVM** , usare l'operazione di compatibilità specificata in **CompareOperation** per confrontare il vettore di compatibilità hardware della VM con il vettore di compatibilità corrispondente per l'host.</span><span class="sxs-lookup"><span data-stu-id="c08d5-187">For each **Msvm\_CompatibilityVector** element, use the compatibility operation specified in **CompareOperation** to compare the VM s hardware compatibility vector with the corresponding compatibility vector for the host.</span></span>
3.  <span data-ttu-id="c08d5-188">Se tutti gli elementi **\_ CompatibilityVector di MSVM** della macchina virtuale sono considerati compatibili, la macchina virtuale è compatibile con l'host (dal punto di vista della funzionalità del processore).</span><span class="sxs-lookup"><span data-stu-id="c08d5-188">If the all of the **Msvm\_CompatibilityVector** elements from the VM are deemed compatible, the VM is compatible with the host (from a processor feature perspective).</span></span>

## <a name="requirements"></a><span data-ttu-id="c08d5-189">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c08d5-189">Requirements</span></span>



| <span data-ttu-id="c08d5-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="c08d5-190">Requirement</span></span> | <span data-ttu-id="c08d5-191">Valore</span><span class="sxs-lookup"><span data-stu-id="c08d5-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c08d5-192">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08d5-192">Minimum supported client</span></span><br/> | <span data-ttu-id="c08d5-193">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c08d5-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c08d5-194">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c08d5-194">Minimum supported server</span></span><br/> | <span data-ttu-id="c08d5-195">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c08d5-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c08d5-196">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c08d5-196">Namespace</span></span><br/>                | <span data-ttu-id="c08d5-197">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c08d5-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c08d5-198">MOF</span><span class="sxs-lookup"><span data-stu-id="c08d5-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c08d5-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c08d5-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c08d5-200">DLL</span><span class="sxs-lookup"><span data-stu-id="c08d5-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c08d5-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c08d5-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c08d5-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c08d5-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c08d5-203">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="c08d5-203">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="c08d5-204">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c08d5-204">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




