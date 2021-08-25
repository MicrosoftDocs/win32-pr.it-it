---
description: Aggiorna l'elemento padre per i file del disco rigido virtuale foglia e figlio specificati.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Metodo SetParentVirtualHardDisk della classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47be9f3f383da237a3679633ac1d663bbc81ef078a7529662b8f21d10246761f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050541"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Metodo SetParentVirtualHardDisk della classe Msvm \_ ImageManagementService

Aggiorna l'elemento padre per i file del disco rigido virtuale foglia e figlio specificati. Per informazioni sulle restrizioni di utilizzo per questo metodo, vedere Note.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ChildPath* \[ Pollici\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale figlio.

</dd> <dt>

*ParentPath* \[ Pollici\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale padre.

</dd> <dt>

*LeafPath* \[ Pollici\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale foglia. Il parametro può essere **Null** se il disco rigido virtuale è offline, ma deve essere specificato se il disco rigido virtuale è in uso.

</dd> <dt>

*IgnoreIDMismatch* \[ Pollici\]
</dt> <dd>

Indica se l'elemento padre deve essere impostato forzatamente quando gli identificatori del disco virtuale non corrispondono. Questo parametro deve essere usato con cautela perché se il nuovo disco rigido virtuale padre non è identico al disco padre originale, può verificarsi un danneggiamento dei dati.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
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

**Sistema in uso** (32774)
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

Con questo metodo è possibile usare solo i tipi seguenti di dischi rigidi virtuali:

-   Disco rigido virtuale differenze
-   Disco rigido virtuale differenze

L'accesso alla [**classe Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

