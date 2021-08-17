---
description: Rimuove la macchina virtuale definita in precedenza dall'ambito di gestione del sistema host.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Metodo DestroySystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c41b1f985b55d1f1756d49308ebda4db1beb92264945bd7418bdea4460e4e72b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254151"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo DestroySystem della classe Msvm \_ VirtualSystemManagementService

Rimuove la macchina virtuale definita in precedenza dall'ambito di gestione del sistema host. Verranno rimosse anche eventuali definizioni di risorse associate. La macchina virtuale deve essere spenta o salvata prima di chiamare questo metodo.

## <a name="syntax"></a>Sintassi


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedSystem* \[ Pollici\]
</dt> <dd>

Tipo: **CIM \_ ComputerSystem**

Riferimento a un'istanza del [**\_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta l'istanza della macchina virtuale da eliminare.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Tipo: **CIM \_ ConcreteJob**

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Se questo metodo viene eseguito in modo sincrono, restituisce 0 se ha esito positivo. Se questo metodo viene eseguito in modo asincrono, restituisce 4096 e il parametro di output *Job* può essere usato per tenere traccia dello stato di avanzamento dell'operazione asincrona. Qualsiasi altro valore restituito indica un errore.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

L'esempio C# seguente usa il **metodo DestroySystem** per rimuovere una macchina virtuale pianificata. Questo codice è tratto dall'esempio di macchine virtuali [pianificate Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm). Le utilità a cui si fa riferimento sono disponibili in [Utilità comuni per gli esempi di virtualizzazione (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Per funzionare correttamente, il codice seguente deve essere eseguito nel server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
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
</dt> </dl>

 

