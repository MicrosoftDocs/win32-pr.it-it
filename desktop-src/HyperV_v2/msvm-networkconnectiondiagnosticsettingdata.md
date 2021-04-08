---
description: Rappresenta le impostazioni utilizzate per testare la connettività di rete di una macchina virtuale.
ms.assetid: d719d9c9-7ca9-40a0-ada8-185b8cd44c22
title: Classe Msvm_NetworkConnectionDiagnosticSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_NetworkConnectionDiagnosticSettingData
- Msvm_NetworkConnectionDiagnosticSettingData.IsSender
- Msvm_NetworkConnectionDiagnosticSettingData.SenderIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverIP
- Msvm_NetworkConnectionDiagnosticSettingData.ReceiverMac
- Msvm_NetworkConnectionDiagnosticSettingData.IsolationId
- Msvm_NetworkConnectionDiagnosticSettingData.SequenceNumber
- Msvm_NetworkConnectionDiagnosticSettingData.PayloadSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ec0df1957df6c925cf12ce363c89a0bdad52d3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058242"
---
# <a name="msvm_networkconnectiondiagnosticsettingdata-class"></a><span data-ttu-id="c9a97-103">\_Classe MSVM NetworkConnectionDiagnosticSettingData</span><span class="sxs-lookup"><span data-stu-id="c9a97-103">Msvm\_NetworkConnectionDiagnosticSettingData class</span></span>

<span data-ttu-id="c9a97-104">Rappresenta le impostazioni utilizzate per testare la connettività di rete di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c9a97-104">Represents the settings used to test the network connectivity of a virtual machine.</span></span> <span data-ttu-id="c9a97-105">Utilizzato dal metodo [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c9a97-105">Used by the [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="c9a97-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c9a97-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a97-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9a97-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_NetworkConnectionDiagnosticSettingData : CIM_SettingData
{
  boolean IsSender;
  string  SenderIP;
  string  ReceiverIP;
  string  ReceiverMac;
  uint32  IsolationId;
  uint32  SequenceNumber;
  uint32  PayloadSize;
};
```

## <a name="members"></a><span data-ttu-id="c9a97-108">Members</span><span class="sxs-lookup"><span data-stu-id="c9a97-108">Members</span></span>

<span data-ttu-id="c9a97-109">La **classe \_ NetworkConnectionDiagnosticSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c9a97-109">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="c9a97-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9a97-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9a97-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9a97-111">Properties</span></span>

<span data-ttu-id="c9a97-112">La **classe \_ NetworkConnectionDiagnosticSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c9a97-112">The **Msvm\_NetworkConnectionDiagnosticSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9a97-113">**IsolationId**</span><span class="sxs-lookup"><span data-stu-id="c9a97-113">**IsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a97-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9a97-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9a97-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9a97-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c9a97-116">ID isolamento.</span><span class="sxs-lookup"><span data-stu-id="c9a97-116">The Isolation ID.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-117">**IsSender**</span><span class="sxs-lookup"><span data-stu-id="c9a97-117">**IsSender**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a97-118">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c9a97-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c9a97-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9a97-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c9a97-120">Indica se questo metodo viene richiamato al mittente o al ricevitore.</span><span class="sxs-lookup"><span data-stu-id="c9a97-120">Indicates whether this method is being invoked at the sender or the receiver.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-121">**PayloadSize**</span><span class="sxs-lookup"><span data-stu-id="c9a97-121">**PayloadSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a97-122">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9a97-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9a97-123">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9a97-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c9a97-124">Dimensioni del payload.</span><span class="sxs-lookup"><span data-stu-id="c9a97-124">The payload size.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-125">**ReceiverIP**</span><span class="sxs-lookup"><span data-stu-id="c9a97-125">**ReceiverIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a97-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c9a97-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a97-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9a97-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c9a97-128">Indirizzo IP del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c9a97-128">The receiver IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-129">**ReceiverMac**</span><span class="sxs-lookup"><span data-stu-id="c9a97-129">**ReceiverMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a97-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c9a97-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a97-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9a97-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c9a97-132">Indirizzo MAC del destinatario.</span><span class="sxs-lookup"><span data-stu-id="c9a97-132">The receiver MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-133">**SenderIP**</span><span class="sxs-lookup"><span data-stu-id="c9a97-133">**SenderIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a97-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c9a97-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9a97-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9a97-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c9a97-136">Indirizzo IP del mittente.</span><span class="sxs-lookup"><span data-stu-id="c9a97-136">The sender IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c9a97-137">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="c9a97-137">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9a97-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9a97-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9a97-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="c9a97-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c9a97-140">Numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="c9a97-140">The sequence number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9a97-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9a97-141">Requirements</span></span>



| <span data-ttu-id="c9a97-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a97-142">Requirement</span></span> | <span data-ttu-id="c9a97-143">Valore</span><span class="sxs-lookup"><span data-stu-id="c9a97-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a97-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9a97-144">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a97-145">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9a97-145">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c9a97-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9a97-146">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a97-147">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c9a97-147">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c9a97-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c9a97-148">Namespace</span></span><br/>                | <span data-ttu-id="c9a97-149">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c9a97-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c9a97-150">MOF</span><span class="sxs-lookup"><span data-stu-id="c9a97-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9a97-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9a97-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9a97-152">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a97-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a97-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c9a97-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c9a97-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9a97-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a97-155">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="c9a97-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




