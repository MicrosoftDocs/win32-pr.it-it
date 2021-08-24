---
description: Recupera informazioni sullo stato per un file di disco rigido virtuale.
ms.assetid: 398b098b-dc1a-45e0-abcb-37b4b0a32290
title: Metodo GetVirtualHardDiskState della Msvm_ImageManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b4c696a04ef72075c520694e0983056c74e80e9257d220a9714351664aa841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532341"
---
# <a name="getvirtualharddiskstate-method-of-the-msvm_imagemanagementservice-class"></a>Metodo GetVirtualHardDiskState della classe Msvm \_ ImageManagementService

Recupera informazioni sullo stato per un file di disco rigido virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetVirtualHardDiskState(
  [in]  string              Path,
  [out] string              State,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* \[ Pollici\]
</dt> <dd>

Percorso completo del file di immagine del disco.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, riceve un'istanza incorporata della [**classe Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md) che contiene le informazioni sullo stato per il disco rigido virtuale.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

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
</dt> <dt>

**File non trovato** (32779)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

L'esempio C# seguente illustra come chiamare il **metodo GetVirtualHardDiskState.** Le utilità a cui si fa riferimento sono disponibili in [Utilità comuni per gli esempi di virtualizzazione (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
public static void GetVirtualHardDiskState(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskState");

    inParams["Path"] = vhdPath;
    
    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskState", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskState was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskState was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["State"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

