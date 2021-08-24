---
title: Metodo SetParameter IVMGuestOS (VPCCOMInterfaces.h)
description: Imposta un parametro denominato all'interno del sistema operativo guest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Metodo SetParameter Virtual PC
- Metodo SetParameter Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo SetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69a8a22257aea0f30d2620d610a2ef3745c9c2a640f034bd1c30d1f582a6c9a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512301"
---
# <a name="ivmguestossetparameter-method"></a>Metodo IVMGuestOS::SetParameter

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Imposta un parametro denominato all'interno del sistema operativo guest.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inParameterName* \[ Pollici\]
</dt> <dd>

Nome del parametro. Deve avere una lunghezza compresa tra 1 e 255 caratteri e non può contenere una barra rovesciata ( \\ ).

</dd> <dt>

*inParameterValue* \[ Pollici\]
</dt> <dd>

Valore del parametro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                    | Descrizione                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | Parametro non valido o non specificato.<br/>           |
| <dl> <dt>**Macchina virtuale \_ E \_ TIMEOUT \_ 0xA0040202**</dt> <dt></dt> </dl>                     | L'operazione non è stata completata in modo corretto.<br/>   |
| <dl> <dt>**Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>             |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SOSPESA**</dt> <dt>0XA00400507</dt> </dl>                    | La macchina virtuale è sospesa.<br/>                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non vengono installati in questa macchina virtuale.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                    |



 

## <a name="remarks"></a>Commenti

La macchina virtuale deve essere in esecuzione e i componenti di integrazione devono essere installati quando viene richiamato questo metodo. Questo metodo è supportato solo per i Windows operativi guest basati su Windows.

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

 

