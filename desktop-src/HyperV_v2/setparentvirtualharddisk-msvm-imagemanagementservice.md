---
description: Aggiorna l'elemento padre per i file di disco rigido virtuale foglia e figlio specificati.
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
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311767"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Metodo SetParentVirtualHardDisk della classe MSVM \_ servizio

Aggiorna l'elemento padre per i file di disco rigido virtuale foglia e figlio specificati. Per informazioni sulle restrizioni di utilizzo di questo metodo, vedere la sezione Osservazioni.

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

*Childpath* \[ in\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale figlio.

</dd> <dt>

*ParentPath* \[ in\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale padre.

</dd> <dt>

*LeafPath* \[ in\]
</dt> <dd>

Percorso completo che specifica il percorso del file del disco rigido virtuale foglia. Il parametro può essere **null** se il disco rigido virtuale è offline, ma deve essere specificato se il disco rigido virtuale è in uso.

</dd> <dt>

*IgnoreIDMismatch* \[ in\]
</dt> <dd>

Indica se l'elemento padre deve essere impostato forzatamente quando gli identificatori del disco virtuale non corrispondono. Questo parametro deve essere utilizzato con cautela perché se il nuovo disco rigido virtuale padre non è identico all'elemento padre originale, è possibile che si verifichi un danneggiamento dei dati.

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

**File non trovato** (32779)
</dt> </dl>

## <a name="remarks"></a>Commenti

Con questo metodo è possibile usare solo i tipi di dischi rigidi virtuali seguenti:

-   Disco rigido virtuale differenze
-   VHDX differenze

L'accesso alla [**classe \_ servizio di MSVM**](msvm-imagemanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Servizio MSVM**](msvm-imagemanagementservice.md)
</dt> </dl>

 

