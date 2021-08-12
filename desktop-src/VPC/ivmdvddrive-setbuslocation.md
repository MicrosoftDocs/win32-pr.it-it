---
title: Metodo IVMDVDDrive SetBusLocation (VPCCOMInterfaces.h)
description: Collega l'unità DVD al percorso del bus specificato nella macchina virtuale.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Metodo SetBusLocation Virtual PC
- Metodo SetBusLocation Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo SetBusLocation
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 593a42c21d1ed688185a7fe7123e972998859c010775a2cf4efd5f3bbbbaa98f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595844"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>Metodo IVMDVDDrive::SetBusLocation

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Collega l'unità DVD al percorso del bus specificato nella macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*busNumber* \[ Pollici\]
</dt> <dd>

Numero del bus a cui deve essere collegata l'unità. Ad esempio, in un bus IDE, questo numero rappresenta se usare il numero di bus primario o secondario.

</dd> <dt>

*deviceNumber* \[ Pollici\]
</dt> <dd>

Numero del dispositivo a cui deve essere collegata l'unità. Ad esempio, in un bus IDE, questo numero rappresenta se usare la posizione del dispositivo primario o secondario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                                                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                 | La posizione del bus specificata non è valida.<br/>                                                                                     |
| <dl> <dt>**E \_ FAIL**</dt> <dt>0x80004005</dt> </dl>                       | Si è verificato un errore imprevisto.<br/>                                                                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ VM RUNNING OR \_ \_ \_ SAVED**</dt> <dt>0xA004020B</dt> </dl> | Non è possibile impostare la posizione del bus mentre la macchina virtuale è in esecuzione o in uno stato salvato.<br/>                                     |
| <dl> <dt>**VM \_ E \_ BUS \_ LOC IN \_ \_ USO**</dt> </dl>                                                                      | Un altro dispositivo è già collegato alla posizione del bus specificata.<br/>                                                            |
| <dl> <dt>**Macchina virtuale \_ E \_ UNITÀ \_ NON VALIDA**</dt> <dt>0xA0040502</dt> </dl>         | Impossibile inizializzare l'unità corrente.<br/>                                                                                  |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>            | Impossibile scrivere le modifiche nel file delle preferenze perché non è stato possibile determinare la macchina virtuale per questa unità.<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>            | Si è verificato un errore imprevisto.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive è definito come b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

