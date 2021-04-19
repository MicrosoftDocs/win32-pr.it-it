---
description: Ridimensiona un disco rigido virtuale esistente.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Metodo ResizeVirtualHardDisk della classe Msvm_ImageManagementService
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
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307864"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Metodo ResizeVirtualHardDisk della classe MSVM \_ servizio

Ridimensiona un disco rigido virtuale esistente. Il disco rigido virtuale deve essere offline. Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.

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

*Percorso* \[ in\]
</dt> <dd>

Tipo: **stringa**

Percorso completo del file del disco rigido virtuale.

</dd> <dt>

*MaxInternalSize* \[ in\]
</dt> <dd>

Tipo: **UInt64**

Dimensione massima del disco rigido virtuale, in byte, visualizzabile dalla macchina virtuale. Il valore minimo di *MaxInternalSize* è *fissoDimensione* + 512-(*fissoDimensione* mod 512). *FissoDimensione* è la dimensione in byte del file del disco rigido virtuale. Se il valore *MaxInternalSize* specificato è minore del valore minimo, viene restituito l'errore InvalidParameter (32773).

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

Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti quando è in corso l'aumento delle dimensioni del disco rigido virtuale:

-   VHD fisso
-   Correzione di VHDX
-   VHD dinamico
-   VHDX dinamico
-   VHDX differenze

Con questo metodo è possibile utilizzare solo i tipi di dischi rigidi virtuali seguenti quando si riduce la dimensione del disco rigido virtuale:

-   Correzione di VHDX
-   VHDX dinamico
-   VHDX differenze

L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Esempio

Nell'esempio C# seguente viene espanso un file di disco rigido virtuale. Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**\_Servizio MSVM**](msvm-imagemanagementservice.md)
</dt> </dl>

 

