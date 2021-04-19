---
description: Classe astratta che rappresenta le impostazioni per un'istanza specifica di una funzionalità di comcambio Ethernet.
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Classe Msvm_EthernetSwitchFeatureSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a71d9b4a78ffedb6ffc0a0c1e01562ce7638ef65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320034"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a><span data-ttu-id="2fb8e-103">\_Classe MSVM EthernetSwitchFeatureSettingData</span><span class="sxs-lookup"><span data-stu-id="2fb8e-103">Msvm\_EthernetSwitchFeatureSettingData class</span></span>

<span data-ttu-id="2fb8e-104">Classe astratta che rappresenta le impostazioni per un'istanza specifica di una funzionalità di comcambio Ethernet.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-104">An abstract class that represents settings for a given instance of an Ethernet switch feature.</span></span> <span data-ttu-id="2fb8e-105">La classe di gestione delle impostazioni delle funzionalità del commutere Ethernet deve derivare da questa classe astratta.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-105">Ethernet Switch Features settings management class must derive from this abstract class.</span></span>

<span data-ttu-id="2fb8e-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fb8e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fb8e-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="2fb8e-108">Members</span><span class="sxs-lookup"><span data-stu-id="2fb8e-108">Members</span></span>

<span data-ttu-id="2fb8e-109">La **classe \_ EthernetSwitchFeatureSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2fb8e-109">The **Msvm\_EthernetSwitchFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2fb8e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fb8e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fb8e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fb8e-111">Properties</span></span>

<span data-ttu-id="2fb8e-112">La **classe \_ EthernetSwitchFeatureSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-112">The **Msvm\_EthernetSwitchFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fb8e-113">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fb8e-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fb8e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fb8e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fb8e-116">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-116">A short description of the object.</span></span> <span data-ttu-id="2fb8e-117">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2fb8e-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2fb8e-118">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-118">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fb8e-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fb8e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fb8e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fb8e-121">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="2fb8e-121">A description of the object.</span></span> <span data-ttu-id="2fb8e-122">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2fb8e-122">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2fb8e-123">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-123">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fb8e-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fb8e-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fb8e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fb8e-126">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-126">A display name for the object.</span></span> <span data-ttu-id="2fb8e-127">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fb8e-127">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2fb8e-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fb8e-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fb8e-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2fb8e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fb8e-131">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="2fb8e-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2fb8e-132">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2fb8e-132">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2fb8e-133">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2fb8e-133">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fb8e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fb8e-134">Requirements</span></span>



| <span data-ttu-id="2fb8e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fb8e-135">Requirement</span></span> | <span data-ttu-id="2fb8e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="2fb8e-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fb8e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb8e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2fb8e-138">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2fb8e-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2fb8e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fb8e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2fb8e-140">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2fb8e-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2fb8e-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fb8e-141">Namespace</span></span><br/>                | <span data-ttu-id="2fb8e-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2fb8e-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2fb8e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2fb8e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fb8e-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fb8e-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fb8e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2fb8e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fb8e-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2fb8e-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

