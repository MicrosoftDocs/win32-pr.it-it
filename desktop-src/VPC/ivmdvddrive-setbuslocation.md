---
title: Metodo IVMDVDDrive SetBusLocation (VPCCOMInterfaces. h)
description: Connette l'unità DVD al percorso del bus specificato nella macchina virtuale.
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
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301736"
---
# <a name="ivmdvddrivesetbuslocation-method"></a>Metodo IVMDVDDrive:: SetBusLocation

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Connette l'unità DVD al percorso del bus specificato nella macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*busNumber* \[ in\]
</dt> <dd>

Numero del bus a cui deve essere collegata l'unità. Ad esempio, in un bus IDE, questo numero indicherà se usare il numero di bus primario o secondario.

</dd> <dt>

*deviceNumber* \[ in\]
</dt> <dd>

Numero del dispositivo a cui deve essere collegata l'unità. Ad esempio, in un bus IDE, questo numero indicherà se usare il percorso del dispositivo primario o secondario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                            | Descrizione                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                  | L'operazione è stata completata.<br/>                                                                                                |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                 | Il percorso del bus specificato non è valido.<br/>                                                                                     |
| <dl> <dt>**E \_ ERRORE**</dt> <dt>0x80004005</dt> </dl>                       | Si è verificato un errore imprevisto.<br/>                                                                                            |
| <dl> <dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt> </dl> | Non è possibile impostare il percorso del bus mentre la macchina virtuale è in esecuzione o è in uno stato salvato.<br/>                                     |
| <dl> <dt>**\_loc VM \_ E \_ bus \_ in \_ uso**</dt> </dl>                                                                      | Un altro dispositivo è già collegato al percorso del bus specificato.<br/>                                                            |
| <dl> <dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt> </dl>         | Non è stato possibile inizializzare l'unità corrente.<br/>                                                                                  |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>            | Non è stato possibile scrivere le modifiche nel file delle preferenze perché non è stato possibile determinare la macchina virtuale per questa unità.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>            | Si è verificato un errore imprevisto.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

