---
description: Restituisce informazioni di riepilogo sulle macchine virtuali.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Metodo GetSummaryInformation della Msvm_VirtualSystemManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: efa879cd3da0f5e8a4cc8cf1e9873390c94a94bae0eef3dd8d36c59c9e1680e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253651"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo GetSummaryInformation della classe Msvm \_ VirtualSystemManagementService

Restituisce informazioni di riepilogo sulle macchine virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazione dei dati* \[ Pollici\]
</dt> <dd>

Tipo: **CIM \_ \[ \] VirtualSystemSettingData**

Matrice di [**istanze CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che specificano le macchine virtuali o gli snapshot per cui devono essere recuperate le informazioni. Se questo parametro è **Null,** vengono recuperate le informazioni per tutte le macchine virtuali.

</dd> <dt>

*RequestedInformation* \[ Pollici\]
</dt> <dd>

Tipo: **uint32 \[ \]**

Matrice di valori di enumerazione, che corrispondono alle proprietà nella classe [**Msvm \_ SummaryInformation,**](msvm-summaryinformation.md) che specificano i dati da recuperare per le macchine virtuali e gli snapshot specificati nella matrice *SettingData.*

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome** (0)


</dt> <dd>

Corrisponde alla proprietà **Name** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nome elemento** (1)


</dt> <dd>

Corrisponde alla proprietà **ElementName** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Ora creazione** (2)


</dt> <dd>

Corrisponde alla proprietà **CreationTime** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Note** (3)


</dt> <dd>

Corrisponde alla proprietà **Notes** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Numero di processori** (4)


</dt> <dd>

Corrisponde alla proprietà **NumberOfProcessors** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Immagine di anteprima piccola (80x60)** (5)


</dt> <dd>

Corrisponde alla proprietà **ThumbnailImage** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Verrà recuperata un'immagine di anteprima con dimensioni di 80 60.

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Immagine di anteprima media (160x120)** (6)


</dt> <dd>

Corrisponde alla proprietà **ThumbnailImage** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Verrà recuperata un'immagine di anteprima con dimensioni di 160 120.

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Immagine di anteprima grande (320x240)** (7)


</dt> <dd>

Corrisponde alla proprietà **ThumbnailImage** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Verrà recuperata un'immagine di anteprima con dimensioni di 320 240.

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)


</dt> <dd>

Corrisponde alla proprietà **AllocatedGPU** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versione** (10)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Schermato** (11)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)


</dt> <dd>

Corrisponde alla proprietà **EnabledState** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)


</dt> <dd>

Corrisponde alla proprietà **ProcessorLoad** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)


</dt> <dd>

Corrisponde alla proprietà **ProcessorLoadHistory** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)


</dt> <dd>

Corrisponde alla proprietà **MemoryUsage** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)


</dt> <dd>

Corrisponde alla proprietà **Heartbeat** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Tempo di attività** (105)


</dt> <dd>

Corrisponde alla proprietà **UpTime** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)


</dt> <dd>

Corrisponde alla proprietà **GuestOperatingSystem** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshot** (107)


</dt> <dd>

Corrisponde alla proprietà **Snapshots** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)


</dt> <dd>

Corrisponde alla proprietà **AsynchronousTasks** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)


</dt> <dd>

Corrisponde alla proprietà **HealthState** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)


</dt> <dd>

Corrisponde alla proprietà **OperationalStatus** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)


</dt> <dd>

Corrisponde alla proprietà **StatusDescriptions** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)


</dt> <dd>

Corrisponde alla proprietà **MemoryAvailable** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)


</dt> <dd>

Corrisponde alla proprietà **AvailableMemoryBuffer** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Modalità di** replica (114)


</dt> <dd>

Corrisponde alla proprietà **ReplicationMode** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Stato replica** (115)


</dt> <dd>

Corrisponde alla proprietà **ReplicationState** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Integrità replicaTest Replica System** (116)


</dt> <dd>

Corrisponde alla proprietà **ReplicationHealth** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Integrità applicazione** (117)


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)


</dt> <dd>

Corrisponde alla proprietà **ReplicationState** della [**classe Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md) Si tratta di una matrice per tutti i valori dello stato di replica nella relazione primaria ed estesa. Il valore di indice 0 è sempre per la relazione primaria e, se la replica estesa è abilitata, viene restituito nell'indice 1.

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)


</dt> <dd>

Corrisponde alla proprietà **ReplicationHealth** della [**classe Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md) Matrice per tutti i valori di integrità della replica nella relazione primaria ed estesa. Il valore di indice 0 è sempre per la relazione primaria e, se la replica estesa è abilitata, viene restituito nell'indice 1.

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)


</dt> <dd>

Corrisponde alla proprietà **SwapFilesInUse** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)


</dt> <dd>

Corrisponde alla proprietà **Name** della [**classe Msvm \_ ReplicationProvider.**](msvm-replicationprovider.md)

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)


</dt> <dd>

Corrisponde alla proprietà **IntegrationServicesVersionState** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)


</dt> <dd>

Corrisponde alla proprietà **OtherEnabledState** della [**classe Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>



 (133)


</dt> <dd></dd> </dl> </dd> <dt>

*Informazioni di riepilogo* \[ Cambio\]
</dt> <dd>

Tipo: **[ **Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**

Matrice di istanze [**di Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md) contenente le informazioni richieste per le macchine virtuali e/o gli snapshot specificati nella *matrice SettingData.* Questa matrice avrà lo stesso numero di elementi della *matrice SettingData.* Ognuna di queste voci conterrà la **proprietà Name,** anche se questa proprietà non è stata richiesta. Se non è possibile trovare la macchina virtuale o lo snapshot o non è disponibile, la **proprietà Name** della voce di informazioni di riepilogo corrispondente sarà vuota.

Le proprietà non specificate nel *parametro RequestedInformation* avranno un **valore** Null.

> [!Note]  
> Tipo di dati aggiornato da in Windows 10 versione 1703 da [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Il sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

L'esempio C# seguente visualizza informazioni di riepilogo. Le utilità a cui si fa riferimento sono disponibili in [Utilità comuni per gli esempi di virtualizzazione (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Per funzionare correttamente, il codice seguente deve essere eseguito nel server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)
</dt> </dl>

 

