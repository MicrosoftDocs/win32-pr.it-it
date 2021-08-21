---
title: Proprietà IVMGuestOS SuiteMask (VPCCOMInterfaces.h)
description: Recupera l'oggetto SuiteMask del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Proprietà SuiteMask Virtual PC
- Proprietà SuiteMask Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22075c68ef30fda7360f25e76c84dbffbf7e306335a0ef20bda45559cb6dac09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472296"
---
# <a name="ivmguestossuitemask-property"></a>Proprietà IVMGuestOS::SuiteMask

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera l'oggetto SuiteMask del sistema operativo guest in esecuzione nella macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Valore proprietà

Maschera della suite. Sono supportati i valori stringa seguenti.



| Valore                                                                                   | Significato                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x00000004"</dt> </dl> | Vengono installati i componenti di Microsoft BackOffice.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows Server 2003, Web Edition è installato.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows È installato Server 2003, Compute Cluster Edition.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows È installato Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server.<br/> |
| <dl> <dt>"0x00000002"</dt> </dl> | Windows È installato Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, edizione Enterprise o Windows 2000 Advanced Server.<br/>   |
| <dl> <dt>"0x00000040"</dt> </dl> | Windows È installato XP Embedded.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.<br/>                                                              |
| <dl> <dt>"0x00000100"</dt> </dl> | Desktop remoto è supportata, ma è supportata una sola sessione interattiva.<br/>                                                                                 |
| <dl> <dt>"0x00000001"</dt> </dl> | Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows.<br/>                                 |
| <dl> <dt>"0x00000020"</dt> </dl> | Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore.<br/>                                                                  |
| <dl> <dt>"0x00002000"</dt> </dl> | Windows Archiviazione Server 2003 R2 o Windows Archiviazione Server 2003 è installato.<br/>                                                                                 |
| <dl> <dt>"0x00000010"</dt> </dl> | Servizi Desktop remoto installato. Questo valore è sempre impostato.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows Home Server è installato.<br/>                                                                                                                           |



 

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                        |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **NULL.**<br/>                           |
| <dl> <dt>Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                               |
| <dl> <dt>Macchina virtuale \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non vengono installati in questa macchina virtuale.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                    |



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

 

