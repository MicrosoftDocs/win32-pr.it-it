---
title: Proprietà IVMGuestOS TerminalServicesInitialized (VPCCOMInterfaces.h)
description: Stato del Servizi Desktop remoto nel sistema operativo guest.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- TerminalServicesInitialized - proprietà Virtual PC
- Proprietà TerminalServicesInitialized Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà TerminalServicesInitialized
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595ae6028bea1984a320a699d204e4d3c23c1ca44e021cbbd994bbc5b832655a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512151"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a>Proprietà IVMGuestOS::TerminalServicesInitialized

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera lo stato di Servizi Desktop remoto (in precedenza noto come Servizi terminal) nel sistema operativo guest.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a>Valore proprietà

Stato di inizializzazione.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione ha avuto esito positivo Servizi Desktop remoto è stata inizializzata. Il valore della proprietà restituita indica se Servizi Desktop remoto è disponibile nel sistema operativo guest.<br/> |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | La funzionalità dei componenti di integrazione è in esecuzione, Servizi Desktop remoto non è ancora stata inizializzata.<br/>                                                                                               |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **NULL.**<br/>                                                                                                                                                                       |
| <dl> <dt>Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | Per questa operazione, la macchina virtuale deve essere in esecuzione.<br/>                                                                                                                                     |
| <dl> <dt>Macchina virtuale \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0xA0040505</dt> </dl> | La funzionalità dei componenti di integrazione non è in esecuzione nel sistema operativo guest.<br/>                                                                                                                 |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS è definito come \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

