---
description: Rappresenta le impostazioni per il servizio sintetico 3D presente in un singolo sistema host.
ms.assetid: ed5d9bba-faad-40a6-8f08-258a94272a11
title: Classe Msvm_Synthetic3DServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DServiceSettingData
- Msvm_Synthetic3DServiceSettingData.InstanceID
- Msvm_Synthetic3DServiceSettingData.Caption
- Msvm_Synthetic3DServiceSettingData.Description
- Msvm_Synthetic3DServiceSettingData.ElementName
- Msvm_Synthetic3DServiceSettingData.GPUOvercommitEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b625064f90ef4c0241dfa48bea9900110f37a4d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131074"
---
# <a name="msvm_synthetic3dservicesettingdata-class"></a><span data-ttu-id="5ceb6-103">\_Classe MSVM Synthetic3DServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="5ceb6-103">Msvm\_Synthetic3DServiceSettingData class</span></span>

<span data-ttu-id="5ceb6-104">Rappresenta le impostazioni per il servizio sintetico 3D presente in un singolo sistema host.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-104">Represents the settings for the synthetic 3-D service present on a single host system.</span></span> <span data-ttu-id="5ceb6-105">Non è possibile modificare direttamente le proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="5ceb6-106">Il client deve chiamare il metodo [**MSVM \_ Synthetic3DService. ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) per modificare una di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-106">The client must call the [**Msvm\_Synthetic3DService.ModifyServiceSettings**](modifyservicesettings-msvm-synthetic3dservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="5ceb6-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ceb6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ceb6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Synthetic3DServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Synthetic3D Service Settings";
  string  Description = "Configuration Settings for Synthetic3D Service.";
  string  ElementName = "Synthetic3D Service Settings";
  boolean GPUOvercommitEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="5ceb6-109">Members</span><span class="sxs-lookup"><span data-stu-id="5ceb6-109">Members</span></span>

<span data-ttu-id="5ceb6-110">La **classe \_ Synthetic3DServiceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ceb6-110">The **Msvm\_Synthetic3DServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5ceb6-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ceb6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ceb6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ceb6-112">Properties</span></span>

<span data-ttu-id="5ceb6-113">La **classe \_ Synthetic3DServiceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-113">The **Msvm\_Synthetic3DServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ceb6-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ceb6-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ceb6-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ceb6-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ceb6-117">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-117">A short description of the object.</span></span> <span data-ttu-id="5ceb6-118">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5ceb6-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5ceb6-119">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ceb6-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ceb6-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ceb6-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ceb6-122">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="5ceb6-122">A description of the object.</span></span> <span data-ttu-id="5ceb6-123">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5ceb6-123">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5ceb6-124">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-124">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ceb6-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ceb6-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ceb6-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ceb6-127">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-127">A display name for the object.</span></span> <span data-ttu-id="5ceb6-128">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5ceb6-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5ceb6-129">**GPUOvercommitEnabled**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-129">**GPUOvercommitEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ceb6-130">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-130">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ceb6-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ceb6-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ceb6-132">Controlla se l'assegnazione della macchina virtuale prende in considerazione le limitazioni della memoria della GPU.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-132">Controls whether virtual machine assignment takes GPU memory limitations into account.</span></span>

</dd> <dt>

<span data-ttu-id="5ceb6-133">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-133">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ceb6-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ceb6-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ceb6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ceb6-136">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="5ceb6-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5ceb6-137">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="5ceb6-137">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5ceb6-138">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5ceb6-138">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ceb6-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ceb6-139">Requirements</span></span>



| <span data-ttu-id="5ceb6-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ceb6-140">Requirement</span></span> | <span data-ttu-id="5ceb6-141">Valore</span><span class="sxs-lookup"><span data-stu-id="5ceb6-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ceb6-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ceb6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5ceb6-143">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5ceb6-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5ceb6-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ceb6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5ceb6-145">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5ceb6-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ceb6-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ceb6-146">Namespace</span></span><br/>                | <span data-ttu-id="5ceb6-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5ceb6-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5ceb6-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5ceb6-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ceb6-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ceb6-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ceb6-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5ceb6-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ceb6-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ceb6-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

