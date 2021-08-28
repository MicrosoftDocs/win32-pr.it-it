---
title: Metodo IVMGuestOS GetOsVersionInfo (VPCCOMInterfaces.h)
description: Recupera le informazioni sulla versione per il sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- Metodo GetOsVersionInfo Virtual PC
- Metodo GetOsVersionInfo Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo GetOsVersionInfo
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef39259b429d096246bbdbe5cb23e6021f498b2d9d47cd14fb12409eca814c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653471"
---
# <a name="ivmguestosgetosversioninfo-method"></a>Metodo IVMGuestOS::GetOsVersionInfo

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera le informazioni sulla versione per il sistema operativo guest in esecuzione nella macchina virtuale .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*guestOsVersionInfo* \[ out, retval\]
</dt> <dd>

Puntatore a una [**struttura GUESTOSVERSIONINFOEX.**](guestosversioninfoex.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                             | L'operazione è stata completata.<br/>                                  |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                               | Il parametro è **NULL.**<br/>                                     |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl> | La memoria disponibile non è sufficiente per completare la richiesta.<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                       | Si è verificato un errore imprevisto.<br/>                              |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt> </dl>                  | La macchina virtuale non è in esecuzione.<br/>                                         |
| <dl> <dt>**Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505**</dt> <dt></dt> </dl>    | I componenti di integrazione non sono installati in questa macchina virtuale.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

