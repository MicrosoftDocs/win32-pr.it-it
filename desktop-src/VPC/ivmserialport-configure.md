---
title: Metodo Configure IVMSerialPort (VPCCOMInterfaces. h)
description: Configura la porta seriale.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Configurare il metodo Virtual PC
- Configurare il metodo Virtual PC, interfaccia IVMSerialPort
- Interfaccia IVMSerialPort Virtual PC, metodo Configure
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048434"
---
# <a name="ivmserialportconfigure-method"></a>Metodo IVMSerialPort:: Configure

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Configura la porta seriale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*portType* \[ in\]
</dt> <dd>

Tipo di porta seriale. Per un elenco di valori, vedere [**VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*portaname* \[ in\]
</dt> <dd>

Nome della porta seriale. Ad esempio, "COM1" per **vmSerialPort \_ portahost**, "C: \\SerialPort.txt" per **vmSerialPort \_ TextFile** o " \\ \\ *ServerName* \\ pipe \\ *pipeName*" per **vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ in\]
</dt> <dd>

**True** se la porta seriale dell'host deve essere aperta immediatamente quando la macchina virtuale viene avviata e **false** in caso contrario. Viene ignorato se *portType* non è **vmSerialPort \_ portahost**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                          |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                                 | Il parametro *portType* non è valido.<br/>                                                                                 |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                      |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                    | Il parametro *PortName* è **null**.<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt> </dl>      | La memoria disponibile non è sufficiente per completare la richiesta.<br/>                                                         |
| <dl> <dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal parametro *PortName* è troppo lungo. Il percorso deve essere minore di **Max \_ path** (260) caratteri.<br/> |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt> </dl>    | Il parametro *PortName* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt> </dl>    | Il parametro *PortName* specifica un percorso vuoto o relativo. È necessario specificare un percorso assoluto.<br/>                            |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>                            | La configurazione per questa macchina virtuale non è valida.<br/>                                                               |
| <dl> <dt>**Macchina virtuale \_ 0xA0040301 \_ \_ \_ valore non valido E pref**</dt> <dt></dt> </dl>                   | La porta specificata è già in uso.<br/>                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort è definito come 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

