---
description: Rappresenta la configurazione di un'opzione di Fibre Channel virtuale.
ms.assetid: da2918a9-6e7f-4fee-9c13-7e75bbc6821f
title: Classe Msvm_VirtualFcSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitchSettingData
- Msvm_VirtualFcSwitchSettingData.InstanceID
- Msvm_VirtualFcSwitchSettingData.Caption
- Msvm_VirtualFcSwitchSettingData.Description
- Msvm_VirtualFcSwitchSettingData.ElementName
- Msvm_VirtualFcSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualFcSwitchSettingData.VirtualSystemType
- Msvm_VirtualFcSwitchSettingData.Notes
- Msvm_VirtualFcSwitchSettingData.CreationTime
- Msvm_VirtualFcSwitchSettingData.ConfigurationID
- Msvm_VirtualFcSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualFcSwitchSettingData.ConfigurationFile
- Msvm_VirtualFcSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualFcSwitchSettingData.SuspendDataRoot
- Msvm_VirtualFcSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualFcSwitchSettingData.LogDataRoot
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualFcSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualFcSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualFcSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualFcSwitchSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67b6008ba1f5ba9849d6fcd9127c1a55c1da8290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525218"
---
# <a name="msvm_virtualfcswitchsettingdata-class"></a><span data-ttu-id="3b258-103">\_Classe MSVM VirtualFcSwitchSettingData</span><span class="sxs-lookup"><span data-stu-id="3b258-103">Msvm\_VirtualFcSwitchSettingData class</span></span>

<span data-ttu-id="3b258-104">Rappresenta la configurazione di un'opzione di Fibre Channel virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-104">Represents the configuration of a virtual Fibre Channel switch.</span></span>

<span data-ttu-id="3b258-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3b258-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b258-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b258-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitchSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a><span data-ttu-id="3b258-107">Members</span><span class="sxs-lookup"><span data-stu-id="3b258-107">Members</span></span>

<span data-ttu-id="3b258-108">La **classe \_ VirtualFcSwitchSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3b258-108">The **Msvm\_VirtualFcSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3b258-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b258-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b258-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b258-110">Properties</span></span>

<span data-ttu-id="3b258-111">La **classe \_ VirtualFcSwitchSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3b258-111">The **Msvm\_VirtualFcSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b258-112">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="3b258-112">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b258-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-115">Azione da eseguire per la macchina virtuale quando il software eseguito dalla macchina virtuale ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3b258-115">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="3b258-116">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-116">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-117">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="3b258-117">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-118">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b258-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-120">Azione da eseguire per la macchina virtuale quando l'host viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="3b258-120">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="3b258-121">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-121">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-122">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="3b258-122">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b258-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-125">Azione da eseguire per la macchina virtuale all'avvio dell'host.</span><span class="sxs-lookup"><span data-stu-id="3b258-125">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="3b258-126">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-126">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-127">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="3b258-127">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-128">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b258-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-130">Tempo di ritardo prima che la macchina virtuale venga avviata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3b258-130">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="3b258-131">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-131">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-132">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="3b258-132">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-133">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3b258-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-135">Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host.</span><span class="sxs-lookup"><span data-stu-id="3b258-135">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="3b258-136">Un numero inferiore indica l'attivazione precedente.</span><span class="sxs-lookup"><span data-stu-id="3b258-136">A lower number indicates earlier activation.</span></span> <span data-ttu-id="3b258-137">Se una o più configurazioni mostrano lo stesso valore, la sequenza è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="3b258-137">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="3b258-138">Il valore 0 indica che la sequenza è dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="3b258-138">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="3b258-139">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-139">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-140">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="3b258-140">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-141">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-143">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b258-143">A short description of the object.</span></span> <span data-ttu-id="3b258-144">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3b258-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-145">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b258-145">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-148">Percorso di una directory in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-148">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="3b258-149">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-149">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-150">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="3b258-150">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-153">Il percorso relativo e il nome file di un file in cui vengono archiviate le informazioni sulla configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-153">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="3b258-154">Questo percorso è relativo alla proprietà **ConfigurationDataRoot** .</span><span class="sxs-lookup"><span data-stu-id="3b258-154">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3b258-155">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-155">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-156">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="3b258-156">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-159">Identificatore univoco della configurazione.</span><span class="sxs-lookup"><span data-stu-id="3b258-159">The unique identifier of the configuration.</span></span> <span data-ttu-id="3b258-160">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-160">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-161">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="3b258-161">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-162">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b258-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-164">Data e ora in cui sono state create le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="3b258-164">The date and time at which the settings were created.</span></span> <span data-ttu-id="3b258-165">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-165">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="3b258-166">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-166">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-167">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="3b258-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-170">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="3b258-170">A description of the object.</span></span> <span data-ttu-id="3b258-171">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3b258-171">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-172">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3b258-172">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-175">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3b258-175">A display name for the object.</span></span> <span data-ttu-id="3b258-176">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-176">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-177">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b258-177">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b258-180">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="3b258-180">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3b258-181">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="3b258-181">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3b258-182">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-183">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b258-183">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-186">Percorso di una directory in cui vengono archiviate le informazioni di log per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-186">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="3b258-187">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-187">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-188">**Note**</span><span class="sxs-lookup"><span data-stu-id="3b258-188">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-189">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="3b258-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b258-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-191">Note fornite dall'utente correlate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-191">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="3b258-192">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-192">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-193">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="3b258-193">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-196">Percorso completo di un file in cui sono archiviate le informazioni relative al ripristino per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-196">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="3b258-197">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-197">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-198">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b258-198">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-201">Percorso di una directory in cui vengono archiviate le informazioni sugli snapshot della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-201">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="3b258-202">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-203">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b258-203">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-206">Percorso di una directory in cui vengono archiviate informazioni sulle informazioni relative alla sospensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-206">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="3b258-207">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-208">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b258-208">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-211">Percorso di una directory in cui vengono archiviati i file di scambio per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3b258-211">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="3b258-212">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="3b258-212">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b258-213">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="3b258-213">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-216">Nome dell'oggetto [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) a cui appartengono i dati dell'impostazione.</span><span class="sxs-lookup"><span data-stu-id="3b258-216">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="3b258-217">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b258-218">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="3b258-218">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b258-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b258-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b258-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b258-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b258-221">Specifica il tipo di macchina virtuale rappresentata dai dati di impostazione.</span><span class="sxs-lookup"><span data-stu-id="3b258-221">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="3b258-222">Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3b258-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b258-223">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b258-223">Requirements</span></span>



| <span data-ttu-id="3b258-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b258-224">Requirement</span></span> | <span data-ttu-id="3b258-225">Valore</span><span class="sxs-lookup"><span data-stu-id="3b258-225">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b258-226">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b258-226">Minimum supported client</span></span><br/> | <span data-ttu-id="3b258-227">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3b258-227">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3b258-228">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b258-228">Minimum supported server</span></span><br/> | <span data-ttu-id="3b258-229">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3b258-229">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b258-230">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3b258-230">Namespace</span></span><br/>                | <span data-ttu-id="3b258-231">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3b258-231">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3b258-232">MOF</span><span class="sxs-lookup"><span data-stu-id="3b258-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b258-233"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b258-233"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b258-234">DLL</span><span class="sxs-lookup"><span data-stu-id="3b258-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b258-235"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b258-235"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

