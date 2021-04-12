---
description: Classe di base astratta per le classi che rappresentano le impostazioni per una funzionalità della porta del commutire Ethernet.
ms.assetid: 26c40dd0-fe1e-4432-a177-8a565bf678e6
title: Classe Msvm_EthernetSwitchPortFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortFeatureSettingData
- Msvm_EthernetSwitchPortFeatureSettingData.InstanceID
- Msvm_EthernetSwitchPortFeatureSettingData.Caption
- Msvm_EthernetSwitchPortFeatureSettingData.Description
- Msvm_EthernetSwitchPortFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0734fa89d99d80e26e4d5fc841bdac89cfd8dfe6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346061"
---
# <a name="msvm_ethernetswitchportfeaturesettingdata-class"></a><span data-ttu-id="2f9ba-103">\_Classe MSVM EthernetSwitchPortFeatureSettingData</span><span class="sxs-lookup"><span data-stu-id="2f9ba-103">Msvm\_EthernetSwitchPortFeatureSettingData class</span></span>

<span data-ttu-id="2f9ba-104">Classe di base astratta per le classi che rappresentano le impostazioni per una funzionalità della porta del commutire Ethernet.</span><span class="sxs-lookup"><span data-stu-id="2f9ba-104">Abstract base class for classes that represent settings for an Ethernet switch port feature.</span></span>

<span data-ttu-id="2f9ba-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2f9ba-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9ba-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f9ba-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPortFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="2f9ba-107">Members</span><span class="sxs-lookup"><span data-stu-id="2f9ba-107">Members</span></span>

<span data-ttu-id="2f9ba-108">La **classe \_ EthernetSwitchPortFeatureSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2f9ba-108">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2f9ba-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f9ba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f9ba-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2f9ba-110">Properties</span></span>

<span data-ttu-id="2f9ba-111">La **classe \_ EthernetSwitchPortFeatureSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2f9ba-111">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f9ba-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9ba-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9ba-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f9ba-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9ba-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f9ba-115">A short description of the object.</span></span> <span data-ttu-id="2f9ba-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2f9ba-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f9ba-117">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9ba-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9ba-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f9ba-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9ba-120">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="2f9ba-120">A description of the object.</span></span> <span data-ttu-id="2f9ba-121">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2f9ba-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2f9ba-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9ba-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9ba-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f9ba-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f9ba-125">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2f9ba-125">A display name for the object.</span></span> <span data-ttu-id="2f9ba-126">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f9ba-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2f9ba-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f9ba-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f9ba-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2f9ba-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f9ba-130">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="2f9ba-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2f9ba-131">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2f9ba-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2f9ba-132">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2f9ba-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f9ba-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f9ba-133">Requirements</span></span>



| <span data-ttu-id="2f9ba-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f9ba-134">Requirement</span></span> | <span data-ttu-id="2f9ba-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2f9ba-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9ba-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f9ba-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f9ba-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2f9ba-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f9ba-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f9ba-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f9ba-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2f9ba-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f9ba-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f9ba-140">Namespace</span></span><br/>                | <span data-ttu-id="2f9ba-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f9ba-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f9ba-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2f9ba-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f9ba-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f9ba-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f9ba-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2f9ba-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f9ba-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f9ba-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

