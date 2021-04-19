---
description: Classe astratta per le sottoclassi che descrivono le funzionalità di un elemento gestito associato e il potenziale delle capacità.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: Classe CIM_Capabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313866"
---
# <a name="cim_capabilities-class"></a><span data-ttu-id="e5bd5-103">\_Classe di funzionalità CIM</span><span class="sxs-lookup"><span data-stu-id="e5bd5-103">CIM\_Capabilities class</span></span>

<span data-ttu-id="e5bd5-104">Classe astratta per le sottoclassi che descrivono le funzionalità di un elemento gestito associato e il potenziale delle capacità.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-104">An abstract class for subclasses that describes the abilities of an associated managed element, and the potential of the abilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5bd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5bd5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="e5bd5-106">Members</span><span class="sxs-lookup"><span data-stu-id="e5bd5-106">Members</span></span>

<span data-ttu-id="e5bd5-107">La classe delle **\_ funzionalità CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e5bd5-107">The **CIM\_Capabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="e5bd5-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e5bd5-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e5bd5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e5bd5-109">Properties</span></span>

<span data-ttu-id="e5bd5-110">La classe delle **\_ funzionalità CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-110">The **CIM\_Capabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e5bd5-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e5bd5-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5bd5-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5bd5-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5bd5-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5bd5-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5bd5-114">Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="e5bd5-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="e5bd5-115">Nome descrittivo dell'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-115">The user friendly name for this class instance.</span></span> <span data-ttu-id="e5bd5-116">Inoltre, è possibile utilizzare il nome descrittivo come proprietà di indice per una query.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-116">In addition, the user friendly name can be used as a index property for a query.</span></span> <span data-ttu-id="e5bd5-117">Non è necessario che questo valore sia univoco all'interno dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-117">This value does not have to be unique within its namespace.</span></span>

</dd> <dt>

<span data-ttu-id="e5bd5-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e5bd5-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e5bd5-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e5bd5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e5bd5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e5bd5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e5bd5-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="e5bd5-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="e5bd5-122">Identifica in modo univoco e opaco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-122">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e5bd5-123">Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="e5bd5-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="e5bd5-124">*OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce **InstanceID**, oppure essere un ID registrato assegnato da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="e5bd5-125">Questo modello è simile alla struttura dei nomi delle classi dello schema.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-125">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="e5bd5-126">Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-126">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="e5bd5-127">Pertanto *OrgID* non deve contenere i due punti (':').</span><span class="sxs-lookup"><span data-stu-id="e5bd5-127">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="e5bd5-128">Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-128">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="e5bd5-129">Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-129">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="e5bd5-130">Per le istanze definite DMTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="e5bd5-130">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e5bd5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5bd5-131">Requirements</span></span>



| <span data-ttu-id="e5bd5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5bd5-132">Requirement</span></span> | <span data-ttu-id="e5bd5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e5bd5-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5bd5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5bd5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e5bd5-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e5bd5-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e5bd5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5bd5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e5bd5-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5bd5-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e5bd5-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e5bd5-138">Namespace</span></span><br/>                | <span data-ttu-id="e5bd5-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e5bd5-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e5bd5-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e5bd5-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5bd5-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5bd5-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5bd5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e5bd5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5bd5-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5bd5-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5bd5-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5bd5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5bd5-145">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="e5bd5-145">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

