---
title: Metodo IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces.h)
description: Recupera il valore dell'impostazione di configurazione specificata.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Metodo GetConfigurationValue Virtual PC
- Metodo GetConfigurationValue Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a483211353474f3328fc4e5da3b80ecf3fbbece53bc306e546f85543ac9027e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591862"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>Metodo IVMVirtualPC::GetConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il valore dell'impostazione di configurazione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*preferenceKey* \[ Pollici\]
</dt> <dd>

Chiave utilizzata per identificare la preferenza, come archiviato nel file di configurazione.

</dd> <dt>

*preferenceValue* \[ out, retval\]
</dt> <dd>

Valore della preferenza. Questo parametro può essere uno dei tipi **VARIANT** seguenti: **VT \_ ARRAY** \| **VT \_ UI1** (byte non elaborati), **VT \_ BSTR** (stringa), **VT \_ I4** (integer) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                | Il *parametro preferenceKey* o *preferenceValue* è **NULL.**<br/>                      |
| <dl> <dt>**Macchina virtuale \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xa0040300</dt> </dl>                   | La preferenza non è stata trovata.<br/>                                                        |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/> |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |



 

## <a name="remarks"></a>Commenti

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di preferenza per l'utente corrente. Può essere usato per recuperare i valori delle preferenze per le chiavi definite dal cliente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

