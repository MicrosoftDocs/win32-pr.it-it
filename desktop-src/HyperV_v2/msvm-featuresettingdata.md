---
description: Classe astratta che rappresenta le impostazioni per una funzionalità specifica di un sistema o di un componente.
ms.assetid: f55eacdd-a802-4374-8756-a59733af6d2c
title: Classe Msvm_FeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingData
- Msvm_FeatureSettingData.InstanceID
- Msvm_FeatureSettingData.Caption
- Msvm_FeatureSettingData.Description
- Msvm_FeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98f022515ac877c0dd598cb9a962bc3133f76eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525236"
---
# <a name="msvm_featuresettingdata-class"></a><span data-ttu-id="7b9f2-103">\_Classe MSVM FeatureSettingData</span><span class="sxs-lookup"><span data-stu-id="7b9f2-103">Msvm\_FeatureSettingData class</span></span>

<span data-ttu-id="7b9f2-104">Classe astratta che rappresenta le impostazioni per una funzionalità specifica di un sistema o di un componente.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-104">An abstract class that represents settings for a specific feature of a system or component.</span></span>

<span data-ttu-id="7b9f2-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b9f2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b9f2-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="7b9f2-107">Members</span><span class="sxs-lookup"><span data-stu-id="7b9f2-107">Members</span></span>

<span data-ttu-id="7b9f2-108">La **classe \_ FeatureSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7b9f2-108">The **Msvm\_FeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7b9f2-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b9f2-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b9f2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b9f2-110">Properties</span></span>

<span data-ttu-id="7b9f2-111">La **classe \_ FeatureSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-111">The **Msvm\_FeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b9f2-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9f2-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b9f2-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b9f2-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b9f2-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-115">A short description of the object.</span></span> <span data-ttu-id="7b9f2-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7b9f2-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7b9f2-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9f2-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b9f2-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b9f2-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b9f2-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7b9f2-120">A description of the object.</span></span> <span data-ttu-id="7b9f2-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7b9f2-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7b9f2-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9f2-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b9f2-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b9f2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b9f2-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-125">A display name for the object.</span></span> <span data-ttu-id="7b9f2-126">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b9f2-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7b9f2-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b9f2-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b9f2-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b9f2-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b9f2-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7b9f2-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7b9f2-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7b9f2-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7b9f2-132">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b9f2-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b9f2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b9f2-133">Requirements</span></span>



| <span data-ttu-id="7b9f2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b9f2-134">Requirement</span></span> | <span data-ttu-id="7b9f2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="7b9f2-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b9f2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b9f2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7b9f2-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7b9f2-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7b9f2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b9f2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7b9f2-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7b9f2-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b9f2-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b9f2-140">Namespace</span></span><br/>                | <span data-ttu-id="7b9f2-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7b9f2-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7b9f2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7b9f2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b9f2-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b9f2-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b9f2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="7b9f2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b9f2-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7b9f2-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

