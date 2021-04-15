---
title: Metodo IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Imposta un canale di comunicazione tra l'host e il sistema operativo guest.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Metodo StartCommunicationChannel Virtual PC
- Metodo StartCommunicationChannel Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478323"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a>Metodo IVMVirtualMachine:: StartCommunicationChannel

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Imposta un canale di comunicazione tra l'host e il sistema operativo guest.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inHostEndpointType* \[ in\]
</dt> <dd>

Questo parametro deve essere **vmEndpoint \_ NamedPipe** (0).

</dd> <dt>

*inHostEndPointName* \[ in\]
</dt> <dd>

Nome univoco della pipe. Questa stringa deve avere il formato seguente: " \\ \\ . \\ pipe \\ *pipeName*". La parte *pipeName* del nome può includere qualsiasi carattere diverso da una barra rovesciata, inclusi i numeri e i caratteri speciali. La lunghezza totale della stringa del nome della pipe può essere di 256 caratteri. Per i nomi di pipe non viene fatta distinzione tra maiuscole

</dd> <dt>

*inGuestEndpointType* \[ in\]
</dt> <dd>

Questo parametro deve essere **vmEndpoint \_ Tcpip** (1).

</dd> <dt>

*inGuestEndpointName* \[ in\]
</dt> <dd>

Numero di porta su cui il server TCP nel Guest è in ascolto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                                  | Descrizione                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                        | L'operazione è stata completata.<br/>                                                                                                                    |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                                       | Il parametro *inHostEndpointType* non è **vmEndpoint \_ NamedPipe** (0) o il parametro *inGuestEndpointType* non è **vmEndpoint \_ Tcpip** (1).<br/> |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                          | Il parametro *inHostEndPointName* o *inGuestEndpointName* è **null** o non è un valore valido.<br/>                                                    |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                                  | Si è verificato un errore imprevisto.<br/>                                                                                                                |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ handle non valido \_ )**</dt> <dt>0x80070006</dt> </dl>        | Handle non valido.<br/>                                                                                                                           |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt> </dl>            | La memoria disponibile non è sufficiente per completare la richiesta.<br/>                                                                                   |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ non \_ pronto)**</dt> <dt>0x80070015</dt> </dl>             | Il sistema sottostante usato per fornire servizi di rete è attualmente in fase di inizializzazione.<br/>                                                        |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt> </dl>        | Il nome della pipe è già in uso.<br/>                                                                                                                 |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (pipe di errore \_ \_ occupata)**</dt> <dt>0x800700e7</dt> </dl>             | Uno o più canali sono in esecuzione e potrebbero essere disponibili a breve.<br/>                                                                          |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ Max \_ sessioni \_ raggiunte)**</dt> <dt>0x80070161</dt> </dl> | Il numero massimo di canali di comunicazione disponibili è in uso. Non è possibile avviare un altro canale in questo momento.<br/>                              |
| <dl> <dt>**HRESULT \_ DA \_ Win32 ( \_ \_ mancata corrispondenza Revisione errore)**</dt> <dt>0x8007051a</dt> </dl>     | Mancata corrispondenza tra la versione dei sottosistemi host e Guest. Per ulteriori informazioni, vedere il registro eventi di Windows.<br/>                             |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>                             | La macchina virtuale non è in esecuzione.<br/>                                                                                                                           |



 

## <a name="remarks"></a>Commenti

L'implementazione corrente supporta solo named pipe interfaccia sull'host e sull'interfaccia TCP/IP nel sistema operativo guest.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMEndpointType**](vmendpointtype.md)
</dt> </dl>

 

