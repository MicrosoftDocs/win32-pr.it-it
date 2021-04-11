---
description: Rappresenta i parametri di configurazione e operativi per le \_ istanze CIM gestiteelement.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: Classe CIM_SettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232084"
---
# <a name="cim_settingdata-class"></a><span data-ttu-id="81056-103">CIM \_ SettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="81056-103">CIM\_SettingData class</span></span>

<span data-ttu-id="81056-104">Rappresenta i parametri di configurazione e operativi per le istanze [**CIM \_ gestiteelement**](cim-managedelement.md) .</span><span class="sxs-lookup"><span data-stu-id="81056-104">Represents configuration and operational parameters for [**CIM\_ManagedElement**](cim-managedelement.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="81056-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81056-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="81056-106">Members</span><span class="sxs-lookup"><span data-stu-id="81056-106">Members</span></span>

<span data-ttu-id="81056-107">La classe **CIM \_ SettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="81056-107">The **CIM\_SettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="81056-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81056-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81056-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81056-109">Properties</span></span>

<span data-ttu-id="81056-110">La classe **CIM \_ SettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="81056-110">The **CIM\_SettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81056-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="81056-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81056-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81056-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81056-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81056-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81056-114">Qualificatori: [**obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="81056-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="81056-115">Nome descrittivo per un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="81056-115">The user-friendly name for an instance of this class.</span></span> <span data-ttu-id="81056-116">Inoltre, il nome descrittivo può essere utilizzato come indice per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="81056-116">In addition, the user-friendly name can be used as an index for a search or query.</span></span> <span data-ttu-id="81056-117">Non è necessario che il nome sia univoco all'interno di uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="81056-117">The name does not have to be unique within a namespace.</span></span>

</dd> <dt>

<span data-ttu-id="81056-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="81056-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81056-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="81056-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="81056-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81056-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81056-121">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="81056-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="81056-122">Identifica in modo univoco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="81056-122">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="81056-123">Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="81056-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="81056-124">*OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce la proprietà **InstanceID** , oppure essere un ID registrato assegnato da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="81056-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="81056-125">*OrgID* non deve contenere i due punti.</span><span class="sxs-lookup"><span data-stu-id="81056-125">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="81056-126">I primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="81056-126">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="81056-127">Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.</span><span class="sxs-lookup"><span data-stu-id="81056-127">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="81056-128">Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="81056-128">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="81056-129">Per le istanze definite da DMTF, il modello deve essere usato con *OrgID* impostato su "CIM".</span><span class="sxs-lookup"><span data-stu-id="81056-129">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81056-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81056-130">Requirements</span></span>



| <span data-ttu-id="81056-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="81056-131">Requirement</span></span> | <span data-ttu-id="81056-132">Valore</span><span class="sxs-lookup"><span data-stu-id="81056-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81056-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81056-133">Minimum supported client</span></span><br/> | <span data-ttu-id="81056-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="81056-134">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="81056-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81056-135">Minimum supported server</span></span><br/> | <span data-ttu-id="81056-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81056-136">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="81056-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81056-137">Namespace</span></span><br/>                | <span data-ttu-id="81056-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="81056-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81056-139">MOF</span><span class="sxs-lookup"><span data-stu-id="81056-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81056-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81056-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81056-141">DLL</span><span class="sxs-lookup"><span data-stu-id="81056-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81056-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81056-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81056-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81056-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81056-144">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="81056-144">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

