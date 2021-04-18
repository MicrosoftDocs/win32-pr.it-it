---
description: La \_ classe CIM Managed è una classe astratta che fornisce una superclasse comune (o parte superiore dell'albero di ereditarietà) per le classi non di associazione nello schema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: Classe CIM_ManagedElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305661"
---
# <a name="cim_managedelement-class"></a><span data-ttu-id="cd0e7-103">CIM \_ managementelement (classe)</span><span class="sxs-lookup"><span data-stu-id="cd0e7-103">CIM\_ManagedElement class</span></span>

<span data-ttu-id="cd0e7-104">La classe **CIM \_ Managed** è una classe astratta che fornisce una superclasse comune (o parte superiore dell'albero di ereditarietà) per le classi non di associazione nello schema CIM.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-104">The **CIM\_ManagedElement** class is an abstract class that provides a common superclass (or top of the inheritance tree) for the non-association classes in the CIM Schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd0e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd0e7-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="cd0e7-106">Members</span><span class="sxs-lookup"><span data-stu-id="cd0e7-106">Members</span></span>

<span data-ttu-id="cd0e7-107">La classe **CIM \_ Managed** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd0e7-107">The **CIM\_ManagedElement** class has these types of members:</span></span>

-   [<span data-ttu-id="cd0e7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd0e7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd0e7-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd0e7-109">Properties</span></span>

<span data-ttu-id="cd0e7-110">La classe **CIM \_ Managed** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-110">The **CIM\_ManagedElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd0e7-111">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-111">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e7-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e7-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e7-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd0e7-114">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="cd0e7-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cd0e7-115">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-115">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="cd0e7-116">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-116">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e7-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e7-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e7-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd0e7-119">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-119">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="cd0e7-120">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-120">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e7-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e7-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd0e7-123">Nome descrittivo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-123">A user-friendly name for the object.</span></span> <span data-ttu-id="cd0e7-124">Questa proprietà consente a ogni istanza di definire un nome descrittivo in aggiunta alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-124">This property allows each instance to define a user-friendly name in addition to its key properties, identity data, and description information.</span></span>

</dd> <dt>

<span data-ttu-id="cd0e7-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd0e7-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd0e7-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd0e7-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd0e7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd0e7-128">Identifica in modo univoco e opaco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-128">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="cd0e7-129">Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="cd0e7-129">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="cd0e7-130">*OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce **InstanceID**, oppure essere un ID registrato assegnato da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-130">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="cd0e7-131">Questo modello è simile alla struttura dei nomi delle classi dello schema.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-131">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="cd0e7-132">Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-132">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="cd0e7-133">Pertanto *OrgID* non deve contenere i due punti (':').</span><span class="sxs-lookup"><span data-stu-id="cd0e7-133">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="cd0e7-134">Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-134">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="cd0e7-135">Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-135">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="cd0e7-136">Per le istanze definite DMTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="cd0e7-136">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd0e7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd0e7-137">Requirements</span></span>



| <span data-ttu-id="cd0e7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd0e7-138">Requirement</span></span> | <span data-ttu-id="cd0e7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="cd0e7-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd0e7-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd0e7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cd0e7-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd0e7-141">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="cd0e7-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd0e7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cd0e7-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd0e7-143">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="cd0e7-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd0e7-144">Namespace</span></span><br/>                | <span data-ttu-id="cd0e7-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd0e7-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cd0e7-146">MOF</span><span class="sxs-lookup"><span data-stu-id="cd0e7-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd0e7-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd0e7-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd0e7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="cd0e7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd0e7-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd0e7-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

