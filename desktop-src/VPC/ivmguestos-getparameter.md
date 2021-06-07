---
title: Metodo GetParameter IVMGuestOS (VPCCOMInterfaces.h)
description: Recupera un parametro denominato all'interno del sistema operativo guest.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Metodo GetParameter Virtual PC
- Metodo GetParameter Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo GetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12bddec3fac5dc918f06d926fe5e5656b70d84d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387647"
---
# <a name="ivmguestosgetparameter-method"></a>Metodo IVMGuestOS::GetParameter

\[Virtual PC Windows non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un parametro denominato all'interno del sistema operativo guest.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inParameterName* \[ Pollici\]
</dt> <dd>

Nome del parametro. Deve avere una lunghezza compresa tra 1 e 255 caratteri e non può contenere una barra rovesciata ( \\ ).

</dd> <dt>

*outParameterValue* \[ out, retval\]
</dt> <dd>

Valore del parametro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                    | Descrizione                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | Parametro non valido o non specificato.<br/>                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **NULL.**<br/>                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ TIMEOUT \_ 0xA0040202**</dt> <dt></dt> </dl>                     | L'operazione non è stata completata in modo corretto.<br/>                |
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                               |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SOSPESA**</dt> <dt>0XA00400507</dt> </dl>                    | La macchina virtuale è sospesa.<br/>                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non vengono installati in questa macchina virtuale.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                 |



 

## <a name="remarks"></a>Commenti

La macchina virtuale deve essere in esecuzione e i componenti di integrazione devono essere installati quando viene richiamato questo metodo. Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.

Con i componenti di integrazione installati, la chiave seguente viene aggiunta automaticamente al Registro di sistema del sistema operativo guest:

**HKEY \_ LOCAL MACHINE SOFTWARE Parametri guest macchina virtuale \_ \\ \\ \\ \\ \\ Microsoft**

All'avvio del sistema operativo guest, i valori di stringa del Registro di sistema seguenti vengono popolati nella **chiave Parameters:**

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows 7 \[\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS è definito come \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

