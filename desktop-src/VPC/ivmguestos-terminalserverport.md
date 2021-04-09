---
title: Proprietà TerminalServerPort di IVMGuestOS
description: Porta utilizzata da Servizi Desktop remoto nel sistema operativo guest.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Proprietà TerminalServerPort Virtual PC
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
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121195"
---
# <a name="ivmguestosterminalserverport-property"></a>Proprietà IVMGuestOS:: TerminalServerPort

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Porta utilizzata da Servizi Desktop remoto (precedentemente nota come servizi Terminal) nel sistema operativo guest.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Valore proprietà

Restituisce la porta utilizzata da Servizi Desktop remoto nel sistema operativo guest.



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
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                            | Il parametro *tsPort* è **null**.<br/>                                           |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                                           |
| <dl> <dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non sono installati in questa macchina virtuale.<br/>             |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                             |



## <a name="remarks"></a>Commenti

Il valore di questa proprietà non è valido a meno che la proprietà [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) non sia **Variant \_ true**.

Se la proprietà [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) è **Variant \_ false** a causa di un errore di connessione sulla porta, il valore restituito dalla proprietà **TerminalServerPort** contiene il valore di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                      |
| IDL<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

