---
title: Metodo IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Elimina la configurazione di una macchina virtuale.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Metodo DeleteVirtualMachine Virtual PC
- Metodo DeleteVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302162"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a>IVMVirtualPC::D Metodo eleteVirtualMachine

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Elimina la configurazione di una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*virtualmachine* \[ in\]
</dt> <dd>

Puntatore a un oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la configurazione della macchina virtuale da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1</dt> </dl>                                           | Impossibile trovare la configurazione specificata.<br/>                                      |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                | Il parametro *virtualmachine* è **null**.<br/>                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt> </dl>                        | La macchina virtuale è in esecuzione.<br/>                                                      |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

È possibile eliminare solo le macchine virtuali arrestate. Si noti che tutti i dati dello stato salvato o dell'unità di annullamento esistenti per questa configurazione verranno eliminati oltre al file di configurazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

