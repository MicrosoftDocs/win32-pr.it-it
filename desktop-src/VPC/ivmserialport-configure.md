---
title: Metodo Configure IVMSerialPort (VPCCOMInterfaces.h)
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
ms.openlocfilehash: e6e67d84239f7b672b5b8c47346d1dde73de6a35c1e99a3ba231b8425fe8b7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136624"
---
# <a name="ivmserialportconfigure-method"></a>Metodo IVMSerialPort::Configure

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*portType* \[ Pollici\]
</dt> <dd>

Tipo di porta seriale. Per un elenco di valori, vedere [**VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*portName* \[ Pollici\]
</dt> <dd>

Nome della porta seriale. Ad esempio, "COM1" per **vmSerialPort \_ HostPort,**"C: \\SerialPort.txt" per **vmSerialPort \_ TextFile** o " \\ \\ *servername* \\ \\ *pipename*" **per vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ Pollici\]
</dt> <dd>

**TRUE** se la porta seriale host deve essere aperta immediatamente all'avvio della macchina virtuale e **FALSE in caso contrario.** Ignorato se *portType* non è **vmSerialPort \_ HostPort**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                            | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | L'operazione è stata completata.<br/>                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | Il *parametro portType* non è valido.<br/>                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Si è verificato un errore imprevisto.<br/>                                                                                      |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                    | Il *parametro portName* è **NULL.**<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | La memoria disponibile non è sufficiente per completare la richiesta.<br/>                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Il percorso specificato dal *parametro portName* è troppo lungo. Il percorso deve essere minore di **MAX \_ PATH** (260 caratteri).<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Il *parametro portName* contiene un carattere non valido (uno di " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Il *parametro portName* specifica un percorso vuoto o relativo. È necessario un percorso assoluto.<br/>                            |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>                            | La configurazione per questa macchina virtuale non è valida.<br/>                                                               |
| <dl> <dt>**Macchina virtuale \_ E \_ PREF \_ ILLEGAL \_ VALUE**</dt> <dt>0xA0040301</dt> </dl>                   | La porta specificata è già in uso.<br/>                                                                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMSerialPort è definito come \_ 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

