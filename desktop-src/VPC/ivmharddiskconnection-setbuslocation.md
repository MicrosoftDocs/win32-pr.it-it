---
title: Metodo IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces.h)
description: Imposta la posizione del bus a cui è collegato il disco rigido.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Metodo SetBusLocation Virtual PC
- Metodo SetBusLocation Virtual PC, interfaccia IVMHardDiskConnection
- Interfaccia IVMHardDiskConnection Virtual PC, metodo SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f2ff59b0318c321d1fb5ce75bac8c5604c5e96474c52565732ec3794b4aab0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974351"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a>Metodo IVMHardDiskConnection::SetBusLocation

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Imposta la posizione del bus a cui è collegato il disco rigido.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vmBusNumber* \[ Pollici\]
</dt> <dd>

Numero del bus da usare.

</dd> <dt>

*vmDeviceNumber* \[ Pollici\]
</dt> <dd>

Numero di dispositivo da usare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                               | Descrizione                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                     | L'operazione è stata completata.<br/>                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                    | La posizione del bus specificata non è valida.<br/>                                                         |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE IN ESECUZIONE O SALVATA \_ \_ \_ 0XA004020B**</dt> <dt></dt> </dl>    | Non è stato possibile impostare la posizione del bus perché la macchina virtuale è in esecuzione o è in stato salvato.<br/>    |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ BUS \_ LOC IN USO \_ \_ 0XA00400503**</dt> <dt></dt> </dl> | Non è stato possibile impostare la posizione del bus perché un altro dispositivo è attualmente collegato a questa posizione.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON VALIDA**</dt> <dt>0xA0040502</dt> </dl>            | L'unità corrente non è valida.<br/>                                                                  |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>               | La macchina virtuale corrente non è valida.<br/>                                                        |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>               | Si è verificato un errore imprevisto.<br/>                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection è definito come aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

