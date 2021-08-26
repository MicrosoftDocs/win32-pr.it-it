---
description: Questo metodo viene usato per trovare la riserva effettiva con il parametro di input corrispondente al numero di processori di macchine virtuali per cui viene calcolata la riserva.
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
ms.openlocfilehash: 06cfa01dd89392c05f460462d8bda5898b47d90b6e027fa885bf039f62488cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042071"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Metodo CalculatePossibleReserve della classe Msvm \_ ProcessorPool

Questo metodo viene usato per trovare la riserva effettiva con il parametro di input corrispondente al numero di processori di macchine virtuali per cui viene calcolata la riserva. Questo metodo è necessario perché la prenotazione delle risorse del processore dipende in modo elevato dal numero di processori che devono essere pianificati in parallelo.

## <a name="syntax"></a>Sintassi


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProcessorCount* \[ Pollici\]
</dt> <dd>

Tipo: **uint16**

Numero di processori di macchine virtuali per cui viene calcolata la riserva. Il valore massimo per questa proprietà è il numero di processori logici per il computer host.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Quantità di risorse della CPU che possono essere riservate per una macchina virtuale.

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ ProcessorPool**](msvm-processorpool.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

