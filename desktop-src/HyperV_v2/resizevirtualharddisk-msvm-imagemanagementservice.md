---
description: Ridimensiona un disco rigido virtuale esistente.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Metodo ResizeVirtualHardDisk della Msvm_ImageManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b582a79757fdf5f27a3f71d260ec6ce7cb594c434422215fb898a2575691da39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754881"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Metodo ResizeVirtualHardDisk della classe Msvm \_ ImageManagementService

Ridimensiona un disco rigido virtuale esistente. Il disco rigido virtuale deve essere offline. Per informazioni sulle restrizioni di utilizzo per questo metodo, vedere La sezione Osservazioni.

## <a name="syntax"></a>Sintassi


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Percorso completo del file del disco rigido virtuale.

</dd> <dt>

*MaxInternalSize* \[ Pollici\]
</dt> <dd>

Tipo: **uint64**

Dimensioni massime del disco rigido virtuale visualizzabili dalla macchina virtuale, in byte. *Il valore minimo di MaxInternalSize* è *DiskSize* + 512 - (*DiskSize* mod 512). *DiskSize* è la dimensione in byte del file del disco rigido virtuale. L'errore InvalidParameter (32773) viene restituito se il *valore MaxInternalSize* specificato è minore del valore minimo.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Questo metodo può restituire uno dei valori seguenti.

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
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="remarks"></a>Commenti

Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti quando le dimensioni del disco rigido virtuale vengono aumentate:

-   Disco rigido virtuale fisso
-   VHDX fisso
-   Disco rigido virtuale dinamico
-   VHDX dinamico
-   VHDX differenze

Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti quando le dimensioni del disco rigido virtuale vengono ridotte:

-   VHDX fisso
-   VHDX dinamico
-   VHDX differenze

L'accesso alla [**classe Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

L'esempio C# seguente espande un file di disco rigido virtuale. Le utilità a cui si fa riferimento sono disponibili in [Utilità comuni per gli esempi di virtualizzazione (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
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

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

