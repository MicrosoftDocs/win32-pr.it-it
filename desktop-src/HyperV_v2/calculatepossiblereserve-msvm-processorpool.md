---
description: Questo metodo viene utilizzato per trovare la riserva effettiva con il parametro di input corrispondente al numero di processori di macchine virtuali per cui viene calcolata la riserva.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Metodo CalculatePossibleReserve della classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756623"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Metodo CalculatePossibleReserve della classe MSVM \_ ProcessorPool

Questo metodo viene utilizzato per trovare la riserva effettiva con il parametro di input corrispondente al numero di processori di macchine virtuali per cui viene calcolata la riserva. Questo metodo è necessario perché la prenotazione delle risorse del processore dipende molto dal numero di processori che devono essere pianificati in parallelo.

## <a name="syntax"></a>Sintassi


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProcessorCount* \[ in\]
</dt> <dd>

Tipo: **UInt16**

Il numero di processori di macchine virtuali per cui viene calcolata la riserva. Il valore massimo per questa proprietà è il numero di processori logici per il computer host.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Quantità di risorse della CPU che possono essere riservate per una macchina virtuale.

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ ProcessorPool di MSVM**](msvm-processorpool.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ProcessorPool MSVM**](msvm-processorpool.md)
</dt> </dl>

 

