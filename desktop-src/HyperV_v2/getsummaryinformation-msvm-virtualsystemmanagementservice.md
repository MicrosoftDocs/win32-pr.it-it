---
description: Restituisce informazioni di riepilogo sulla macchina virtuale.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Metodo GetSummaryInformation della classe Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342801"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo GetSummaryInformation della classe MSVM \_ VirtualSystemManagementService

Restituisce informazioni di riepilogo sulla macchina virtuale.

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

*SettingData* \[ in\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData \[ \]**

Matrice di istanze [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) che specificano le macchine virtuali o gli snapshot per cui è necessario recuperare le informazioni. Se questo parametro è **null**, vengono recuperate le informazioni per tutte le macchine virtuali.

</dd> <dt>

*RequestedInformation* \[ in\]
</dt> <dd>

Tipo: **UInt32 \[ \]**

Matrice di valori di enumerazione, che corrisponde alle proprietà della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) , che specificano i dati da recuperare per le macchine virtuali e gli snapshot specificati nella matrice *SettingData* .

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome** (0)


</dt> <dd>

Corrisponde alla proprietà **Name** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nome elemento** (1)


</dt> <dd>

Corrisponde alla proprietà **ElementName** della classe SummaryInformation di [**MSVM \_**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Ora creazione** (2)


</dt> <dd>

Corrisponde alla proprietà **creationTime** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Note** (3)


</dt> <dd>

Corrisponde alla proprietà **Notes** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Numero di processori** (4)


</dt> <dd>

Corrisponde alla proprietà **NumberOfProcessors** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Piccola immagine di anteprima (80x60)** (5)


</dt> <dd>

Corrisponde alla proprietà **ThumbnailImage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) . Verrà recuperata un'immagine di anteprima con dimensioni pari a 80 60.

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Immagine di anteprima media (160x120)** (6)


</dt> <dd>

Corrisponde alla proprietà **ThumbnailImage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) . Verrà recuperata un'immagine di anteprima con dimensioni pari a 160 120.

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Immagine di anteprima grande (320x240)** (7)


</dt> <dd>

Corrisponde alla proprietà **ThumbnailImage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) . Verrà recuperata un'immagine di anteprima con dimensioni pari a 320 240.

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)


</dt> <dd>

Corrisponde alla proprietà **AllocatedGPU** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

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

Corrisponde alla proprietà **EnabledState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)


</dt> <dd>

Corrisponde alla proprietà **ProcessorLoad** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)


</dt> <dd>

Corrisponde alla proprietà **ProcessorLoadHistory** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)


</dt> <dd>

Corrisponde alla proprietà **MemoryUsage** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)


</dt> <dd>

Corrisponde alla proprietà **heartbeat** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Tempo di esecuzione** (105)


</dt> <dd>

Corrisponde alla proprietà di **tempo di esecuzione** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)


</dt> <dd>

Corrisponde alla proprietà **GuestOperatingSystem** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshot** (107)


</dt> <dd>

Corrisponde alla proprietà **Snapshots** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)


</dt> <dd>

Corrisponde alla proprietà **AsynchronousTasks** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)


</dt> <dd>

Corrisponde alla proprietà **HealthState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)


</dt> <dd>

Corrisponde alla proprietà **OperationalStatus** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)


</dt> <dd>

Corrisponde alla proprietà **StatusDescriptions** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)


</dt> <dd>

Corrisponde alla proprietà **MemoryAvailable** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)


</dt> <dd>

Corrisponde alla proprietà **AvailableMemoryBuffer** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Modalità di replica** (114)


</dt> <dd>

Corrisponde alla proprietà **ReplicationMode** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Stato di replica** (115)


</dt> <dd>

Corrisponde alla proprietà **ReplicationState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Sistema di replica HealthTest di replica** (116)


</dt> <dd>

Corrisponde alla proprietà **ReplicationHealth** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Integrità dell'applicazione** (117)


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)


</dt> <dd>

Corrisponde alla proprietà **ReplicationState** della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) . Si tratta di una matrice per tutti i valori dello stato di replica tra relazioni primarie ed estese. il valore di indice 0 è sempre per la relazione primaria e, se la replica estesa è abilitata, viene restituita nell'indice 1.

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)


</dt> <dd>

Corrisponde alla proprietà **ReplicationHealth** della classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) . Si tratta di una matrice per tutti i valori di integrità della replica tra relazioni primarie ed estese. il valore di indice 0 è sempre per la relazione primaria e, se la replica estesa è abilitata, viene restituita nell'indice 1.

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)


</dt> <dd>

Corrisponde alla proprietà **SwapFilesInUse** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)


</dt> <dd>

Corrisponde alla proprietà **Name** della classe [**MSVM \_ ReplicationProvider**](msvm-replicationprovider.md) .

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)


</dt> <dd>

Corrisponde alla proprietà **IntegrationServicesVersionState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)


</dt> <dd>

Corrisponde alla proprietà **OtherEnabledState** della classe [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>



 (133)


</dt> <dd></dd> </dl> </dd> <dt>

*SummaryInformation* \[ out\]
</dt> <dd>

Tipo: **[ **MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**

Matrice di istanze di [**MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md) contenenti le informazioni richieste per le macchine virtuali e/o gli snapshot specificati nella matrice *SettingData* . Questa matrice avrà lo stesso numero di elementi della matrice *SettingData* . Ognuna di queste voci conterrà la proprietà **Name** , anche se questa proprietà non è stata richiesta. Se la macchina virtuale o lo snapshot non è stato trovato o non è disponibile, la proprietà **Name** della voce di informazioni di riepilogo corrispondente sarà vuota.

Le proprietà non specificate nel parametro *RequestedInformation* avranno un valore **null** .

> [!Note]  
> DataType aggiornato da in Windows 10, versione 1703 da [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Esempio

Nell'esempio C# seguente vengono visualizzate le informazioni di riepilogo. Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.

 


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**\_SummaryInformation MSVM**](msvm-summaryinformation.md)
</dt> </dl>

 

