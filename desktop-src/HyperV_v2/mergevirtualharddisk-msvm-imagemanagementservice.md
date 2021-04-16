---
description: Unisce un disco rigido virtuale figlio in una catena di differenze con uno o più dischi rigidi virtuali padre nella catena.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Metodo MergeVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529664"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Metodo MergeVirtualHardDisk della classe MSVM \_ servizio

Unisce un disco rigido virtuale figlio in una catena di differenze con uno o più dischi rigidi virtuali padre nella catena. Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.

Se l'utente che esegue questa funzione non dispone dell'autorizzazione per aggiornare le macchine virtuali, la funzione avrà esito negativo.

## <a name="syntax"></a>Sintassi


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SourcePath* \[ in\]
</dt> <dd>

Tipo: **stringa**

Percorso completo che specifica il percorso del file del disco rigido virtuale da unire.

</dd> <dt>

*DestinationPath* \[ in\]
</dt> <dd>

Tipo: **stringa**

Percorso completo che specifica il percorso del file del disco rigido virtuale padre in cui deve essere eseguito il merge dei dati. Potrebbe trattarsi del disco rigido virtuale padre diretto del file di Unione o dell'immagine del disco padre, in modo da aumentare la catena di differenziazione.

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

Il disco rigido virtuale figlio deve essere offline.

Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti:

-   Disco rigido virtuale differenze
-   VHDX differenze

L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Esempio

Nell'esempio C# seguente viene espanso un file di disco rigido virtuale. Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
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

 

