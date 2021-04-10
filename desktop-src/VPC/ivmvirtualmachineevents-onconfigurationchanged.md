---
title: Metodo IVMVirtualMachineEvents OnConfigurationChanged (VPCCOMInterfaces. h)
description: Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Metodo OnConfigurationChanged Virtual PC
- Metodo OnConfigurationChanged Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnConfigurationChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963721"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>Metodo IVMVirtualMachineEvents:: OnConfigurationChanged

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configKey* \[ in\]
</dt> <dd>

Valore all'interno della configurazione che è stato modificato.

</dd> <dt>

*configData* \[ in\]
</dt> <dd>

Nuovo valore per la configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando viene modificata la configurazione della macchina virtuale. Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmVirtualMachineEvent ConfigurationChanged originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

