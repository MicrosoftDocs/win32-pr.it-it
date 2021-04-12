---
title: Metodo separameter IVMGuestOS (VPCCOMInterfaces. h)
description: Imposta un parametro denominato all'interno del sistema operativo guest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Metodo separameter Virtual PC
- Metodo separameter Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo separameter
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
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517896"
---
# <a name="ivmguestossetparameter-method"></a>Metodo IVMGuestOS:: separameter

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*Inparametername* \[ in\]
</dt> <dd>

Nome del parametro. Deve avere una lunghezza compresa tra 1 e 255 caratteri e non può contenere una barra rovesciata ( \) carattere.

</dd> <dt>

*inParameterValue* \[ in\]
</dt> <dd>

Valore del parametro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                    | Descrizione                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                        |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                         | Un parametro non è valido o non è specificato.<br/>           |
| <dl> <dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt> </dl>                     | L'operazione non è stata completata in modo tempestivo.<br/>   |
| <dl> <dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale (VM) non è in esecuzione.<br/>             |
| <dl> <dt>**Macchina virtuale \_ 0xA00400507 \_ macchina virtuale E \_ sospesa**</dt> <dt></dt> </dl>                    | La macchina virtuale è sospesa.<br/>                                    |
| <dl> <dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non sono installati in questa macchina virtuale.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                    |



 

## <a name="remarks"></a>Commenti

Quando viene richiamato questo metodo, è necessario che la macchina virtuale sia in esecuzione e che i componenti di integrazione siano installati. Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.

Con i componenti di integrazione installati, la chiave seguente viene aggiunta automaticamente al registro di sistema del sistema operativo guest:

**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Virtual Machine \\ \\ parametri Guest**

Quando viene avviato il sistema operativo guest, i valori stringa del registro di sistema seguenti vengono popolati nella chiave **Parameters** :

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

