---
title: Proprietà TerminalServerPort IVMGuestOS
description: La porta usata Servizi Desktop remoto nel sistema operativo guest.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- TerminalServerPort - proprietà Virtual PC
- Proprietà TerminalServerPort Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b9eea5c545613f05dbd828a9436175fab6bfc5a05ba2fe5f59588f78da913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512161"
---
# <a name="ivmguestosterminalserverport-property"></a>Proprietà IVMGuestOS::TerminalServerPort

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Porta usata da Servizi Desktop remoto (precedentemente nota come Servizi terminal) nel sistema operativo guest.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Valore proprietà

Restituisce la porta utilizzata Servizi Desktop remoto nel sistema operativo guest.



| Valore                                                                              | Significato                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | Valore predefinito<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | Intervallo valido<br/>                        |
| <dl> <dt>0</dt> </dl>       | Il valore di porta valido non è disponibile.<br/> |



 

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Servizi Desktop remoto non è ancora inizializzato nel sistema operativo guest.<br/> |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il *parametro tsPort* è **NULL.**<br/>                                           |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                                           |
| <dl> <dt>Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505</dt> <dt></dt> </dl> | I componenti di integrazione non sono installati in questa macchina virtuale.<br/>             |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                             |



## <a name="remarks"></a>Commenti

Il valore di questa proprietà non è valido a meno che la [**proprietà TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) non **sia VARIANT \_ TRUE.**

Se la [**proprietà TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) è **VARIANT \_ FALSE** a causa di un errore di connessione sulla porta, il valore restituito dalla proprietà **TerminalServerPort** contiene il valore di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                      |
| Idl<br/>                      | <dl> <dt>IVMGuestOS.idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

