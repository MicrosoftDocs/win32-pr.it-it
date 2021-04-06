---
description: Rappresenta le impostazioni per il servizio di replica in un host di ripristino. Non è possibile modificare direttamente le proprietà di questa classe. Il client deve chiamare il \_ Metodo MSVM ReplicationService. ModifyServiceSettings per modificare una di queste proprietà.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Classe Msvm_ReplicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882765"
---
# <a name="msvm_replicationservicesettingdata-class"></a><span data-ttu-id="1acc8-105">\_Classe MSVM ReplicationServiceSettingData</span><span class="sxs-lookup"><span data-stu-id="1acc8-105">Msvm\_ReplicationServiceSettingData class</span></span>

<span data-ttu-id="1acc8-106">Rappresenta le impostazioni per il servizio di replica in un host di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1acc8-106">Represents the settings for the replication service on a recovery host.</span></span> <span data-ttu-id="1acc8-107">Non è possibile modificare direttamente le proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1acc8-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="1acc8-108">Il client deve chiamare il metodo [**MSVM \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) per modificare una di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1acc8-108">The client must call the [**Msvm\_ReplicationService.ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="1acc8-109">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1acc8-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1acc8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1acc8-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a><span data-ttu-id="1acc8-111">Members</span><span class="sxs-lookup"><span data-stu-id="1acc8-111">Members</span></span>

<span data-ttu-id="1acc8-112">La **classe \_ ReplicationServiceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1acc8-112">The **Msvm\_ReplicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1acc8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1acc8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1acc8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1acc8-114">Properties</span></span>

<span data-ttu-id="1acc8-115">La **classe \_ ReplicationServiceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1acc8-115">The **Msvm\_ReplicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1acc8-116">**AllowedAuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="1acc8-116">**AllowedAuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-117">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1acc8-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-119">Definire le modalità di autenticazione consentite per la connessione al server host di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1acc8-119">Define authentication modes allowed for connecting to recovery host server.</span></span>

<dt>

<span data-ttu-id="1acc8-120">0</span><span class="sxs-lookup"><span data-stu-id="1acc8-120">0</span></span>
</dt> <dd>

<span data-ttu-id="1acc8-121">Non definito.</span><span class="sxs-lookup"><span data-stu-id="1acc8-121">Not defined.</span></span>

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="1acc8-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticazione Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="1acc8-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="1acc8-123">Autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="1acc8-123">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="1acc8-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticazione basata su certificati** (2)</span><span class="sxs-lookup"><span data-stu-id="1acc8-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1acc8-125">Autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="1acc8-125">Certificate based authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="1acc8-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Autenticazione basata su certificati e autenticazione Kerberos** (3)</span><span class="sxs-lookup"><span data-stu-id="1acc8-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Certificate based authentication and kerberos authentication** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1acc8-127">Autenticazione basata su certificati e autenticazione integrata.</span><span class="sxs-lookup"><span data-stu-id="1acc8-127">Both certificate based authentication and integrated authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1acc8-128">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1acc8-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acc8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-131">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1acc8-131">A short description of the object.</span></span> <span data-ttu-id="1acc8-132">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Replication Service Settings".</span><span class="sxs-lookup"><span data-stu-id="1acc8-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-133">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="1acc8-133">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acc8-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-136">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="1acc8-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-137">Identificazione personale del certificato da usare quando **AuthenticationType** è l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="1acc8-137">Certificate thumbprint to use when **AuthenticationType** is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-138">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1acc8-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acc8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-141">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="1acc8-141">A description of the object.</span></span> <span data-ttu-id="1acc8-142">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "dati delle impostazioni di replica della macchina virtuale".</span><span class="sxs-lookup"><span data-stu-id="1acc8-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1acc8-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acc8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-146">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1acc8-146">A display name for the object.</span></span> <span data-ttu-id="1acc8-147">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Replication Service Settings".</span><span class="sxs-lookup"><span data-stu-id="1acc8-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-148">**HttpPort**</span><span class="sxs-lookup"><span data-stu-id="1acc8-148">**HttpPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1acc8-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-151">Numero di porta del server di ripristino da utilizzare quando si accetta una connessione non protetta per la replica.</span><span class="sxs-lookup"><span data-stu-id="1acc8-151">Recovery server port number to use when accepting a nonsecure connection for replication.</span></span> <span data-ttu-id="1acc8-152">Il valore predefinito è 80.</span><span class="sxs-lookup"><span data-stu-id="1acc8-152">The default value is 80.</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-153">**HttpsPort**</span><span class="sxs-lookup"><span data-stu-id="1acc8-153">**HttpsPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-154">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1acc8-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-156">Numero di porta del server di ripristino da utilizzare quando si accetta una connessione protetta per la replica.</span><span class="sxs-lookup"><span data-stu-id="1acc8-156">Recovery server port number to use when accepting secure connection for replication.</span></span> <span data-ttu-id="1acc8-157">Il valore predefinito è 443.</span><span class="sxs-lookup"><span data-stu-id="1acc8-157">The default value is 443.</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1acc8-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1acc8-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-161">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="1acc8-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-162">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1acc8-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1acc8-163">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1acc8-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-164">**MonitoringInterval**</span><span class="sxs-lookup"><span data-stu-id="1acc8-164">**MonitoringInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-165">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1acc8-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-167">Intervallo, in secondi, in cui devono essere reimpostate le statistiche di replica.</span><span class="sxs-lookup"><span data-stu-id="1acc8-167">The interval, in seconds, at which replication statistics should be reset.</span></span> <span data-ttu-id="1acc8-168">L'intervallo predefinito è 12 ore (43200 secondi).</span><span class="sxs-lookup"><span data-stu-id="1acc8-168">The default interval is 12 hours (43200 seconds).</span></span> <span data-ttu-id="1acc8-169">Il valore minimo valido è 60 minuti (3600 secondi) e il valore massimo valido è 7 giorni (604800 secondi).</span><span class="sxs-lookup"><span data-stu-id="1acc8-169">The minimum valid value is 60 minutes (3600 seconds), and the maximum valid value is 7 days (604800 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-170">**MonitoringStartTime**</span><span class="sxs-lookup"><span data-stu-id="1acc8-170">**MonitoringStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-171">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1acc8-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-173">Ora di inizio per il monitoraggio della replica, in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="1acc8-173">The start time for replication monitoring, in UTC.</span></span> <span data-ttu-id="1acc8-174">Il valore predefinito è 9:00 A.M., ora locale, rappresentato in formato UTC.</span><span class="sxs-lookup"><span data-stu-id="1acc8-174">The default value is 9:00 A.M., local time, represented in UTC.</span></span> <span data-ttu-id="1acc8-175">Gli elementi date dell'oggetto **DateTime** devono essere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="1acc8-175">The date elements of the **datetime** object must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1acc8-176">**RecoveryServerEnabled**</span><span class="sxs-lookup"><span data-stu-id="1acc8-176">**RecoveryServerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1acc8-177">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1acc8-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1acc8-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1acc8-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1acc8-179">Specifica se l'host Hyper-V è abilitato come server di ripristino.</span><span class="sxs-lookup"><span data-stu-id="1acc8-179">Specifies whether the Hyper-V host is enabled as a recovery server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1acc8-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1acc8-180">Requirements</span></span>



| <span data-ttu-id="1acc8-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="1acc8-181">Requirement</span></span> | <span data-ttu-id="1acc8-182">Valore</span><span class="sxs-lookup"><span data-stu-id="1acc8-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acc8-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acc8-183">Minimum supported client</span></span><br/> | <span data-ttu-id="1acc8-184">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1acc8-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1acc8-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1acc8-185">Minimum supported server</span></span><br/> | <span data-ttu-id="1acc8-186">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1acc8-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1acc8-187">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1acc8-187">Namespace</span></span><br/>                | <span data-ttu-id="1acc8-188">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1acc8-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1acc8-189">MOF</span><span class="sxs-lookup"><span data-stu-id="1acc8-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1acc8-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1acc8-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1acc8-191">DLL</span><span class="sxs-lookup"><span data-stu-id="1acc8-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1acc8-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1acc8-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1acc8-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1acc8-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acc8-194">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="1acc8-194">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="1acc8-195">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="1acc8-195">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

