---
description: Converte un disco rigido virtuale esistente in un tipo o formato diverso.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Metodo ConvertVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314355"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Metodo ConvertVirtualHardDisk della classe MSVM \_ servizio

Converte un disco rigido virtuale esistente in un tipo o formato diverso. Questo metodo crea un nuovo disco rigido virtuale e non converte il disco rigido virtuale di origine sul posto. Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SourcePath* \[ in\]
</dt> <dd>

Tipo: **stringa**

Percorso completo del file di disco rigido virtuale di origine da convertire. Il file non verrà modificato in seguito a questa operazione.

</dd> <dt>

*VirtualDiskSettingData* \[ in\]
</dt> <dd>

Tipo: **stringa**

Rappresentazione di stringa della classe [**\_ VirtualHardDiskSettingData di MSVM**](msvm-virtualharddisksettingdata.md) che specifica gli attributi del nuovo disco rigido virtuale. È necessario impostare le proprietà **path**, **Type**, **Format**, **ParentPath**, **blockSize** e **LogicalSectorSize** . Se non è necessario, la proprietà **ParentPath** può essere **null** . Impostare le proprietà **blockSize** e **LogicalSectorSize** su 0 per usare i valori predefiniti.

Per specificare il formato (VHD o VHDX) del nuovo disco rigido virtuale, impostare l'estensione del **percorso** sul valore appropriato (". VHD" o ". vhdx"). La proprietà **Format** deve corrispondere all'estensione del nome di file nel **percorso**.

La proprietà **LogicalSectorSize** verrà ignorata.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo può restituire uno dei valori seguenti.

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
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="remarks"></a>Commenti

Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti:

-   VHD fisso
-   Correzione di VHDX
-   VHD dinamico
-   VHDX dinamico
-   Disco rigido virtuale differenze
-   VHDX differenze

L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Esempio

Nell'esempio C# seguente viene convertito un disco rigido virtuale. Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
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

[**ConvertVirtualHardDisk (V1)**](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**\_Servizio MSVM**](msvm-imagemanagementservice.md)
</dt> </dl>

 

