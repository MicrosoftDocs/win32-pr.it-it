---
title: Metodo IVMVirtualMachineEvents OnConfigurationChanged (VPCCOMInterfaces.h)
description: Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Metodo OnConfigurationChanged Virtual PC
- Metodo OnConfigurationChanged Virtual PC , interfaccia IVMVirtualMachineEvents
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
ms.openlocfilehash: 36ca4d3b72d9cd2b06db2ca7b7b65e0c63795a4db0e52ccd9b76a62ff8b192e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056639"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a>Metodo IVMVirtualMachineEvents::OnConfigurationChanged

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*configKey* \[ Pollici\]
</dt> <dd>

Valore all'interno della configurazione modificata.

</dd> <dt>

*configData* \[ Pollici\]
</dt> <dd>

Nuovo valore per la configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando la configurazione viene modificata per questa macchina virtuale. Il programma client deve implementare questo metodo di interfaccia per ricevere la notifica dell'evento vmVirtualMachineEvent \_ ConfigurationChanged proveniente da [**IVMVirtualMachine.**](ivmvirtualmachine.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

