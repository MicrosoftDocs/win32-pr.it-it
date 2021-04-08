---
title: Metodo IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Rimuove il valore dell'impostazione di configurazione specificata.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Metodo RemoveConfigurationValue Virtual PC
- Metodo RemoveConfigurationValue Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874281"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a>Metodo IVMVirtualPC:: RemoveConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Rimuove il valore dell'impostazione di configurazione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*preferenceKey* \[ in\]
</dt> <dd>

Chiave utilizzata per identificare la preferenza, archiviata nel file di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                | Il parametro *preferenceKey* è **null**.<br/>                                           |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                             | Il parametro *preferenceKey* non è valido o è una stringa vuota.<br/>                    |
| <dl> <dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt> </dl>                   | La preferenza non è stata trovata.<br/>                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

Questo metodo fornisce accesso di basso livello a qualsiasi valore di preferenza per l'utente corrente. Può essere usato per rimuovere i valori di preferenza per le chiavi definite dal cliente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

