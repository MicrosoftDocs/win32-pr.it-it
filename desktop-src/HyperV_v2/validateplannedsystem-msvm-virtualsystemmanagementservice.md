---
description: Convalida il sistema pianificato specificato.
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Metodo ValidatePlannedSystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759047"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ValidatePlannedSystem della classe MSVM \_ VirtualSystemManagementService

Convalida il sistema pianificato specificato. Ciò comporta controlli della configurazione della macchina virtuale, dei dispositivi, della configurazione dello snapshot, dei dispositivi snapshot, dei file di stato salvati e dei file di archiviazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PlannedSystem* \[ in\]
</dt> <dd>

Riferimento a un oggetto [**\_ PlannedComputerSystem MSVM**](msvm-plannedcomputersystem.md) che rappresenta il sistema pianificato da convalidare.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

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
</dt> <dt>

**File in uso** (32779)
</dt> </dl>

## <a name="examples"></a>Esempio

Nell'esempio C# seguente viene usato il metodo **ValidatePlannedSystem** per convalidare una macchina virtuale pianificata. Questo codice è tratto dall' [esempio di macchine virtuali pianificate Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm). Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
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
</dt> </dl>

 

