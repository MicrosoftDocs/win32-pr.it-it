---
title: Metodo IVMVirtualMachine SetActivationValue (VPCCOMInterfaces.h)
description: Imposta il valore dell'impostazione di attivazione specificata per questa macchina virtuale.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Metodo SetActivationValue Virtual PC
- Metodo SetActivationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo SetActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f7c669db848a668d294e509ad65a56ef19aebd53d0c718f12e524cfc16a940
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124721"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a>Metodo IVMVirtualMachine::SetActivationValue

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Imposta il valore dell'impostazione di attivazione specificata per questa macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*activationKey* \[ Pollici\]
</dt> <dd>

Chiave usata per identificare il valore di attivazione archiviato nel \* file "vmc".

</dd> <dt>

*activationValue* \[ Pollici\]
</dt> <dd>

Valore di attivazione. Questo valore può essere uno dei tipi **VARIANT** seguenti: **VT \_ ARRAY** \| **VT \_ UI1** (byte non elaborati), **VT \_ BSTR** (stringa), **VT \_ UI4** (integer) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                      | Descrizione                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | Il *parametro activationKey* è **NULL** o vuoto oppure il *parametro activationValue* non è un tipo variant valido.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>      | La configurazione è sconosciuta.<br/>                                                                                       |
| <dl> <dt>**Macchina virtuale \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | La configurazione non ha un'attivazione valida.<br/>                                                                          |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>      | Si è verificato un errore imprevisto.<br/>                                                                                   |



 

## <a name="remarks"></a>Commenti

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di attivazione. Può essere usato per impostare i valori di attivazione per le chiavi definite dal cliente. Prestare attenzione se si usa questo metodo per impostare i valori di attivazione del sistema, poiché non viene eseguito alcun controllo degli errori sul valore di attivazione. Inoltre, alcuni valori di attivazione non possono essere modificati mentre la macchina virtuale è in esecuzione. Quando viene avviata una macchina virtuale, viene creata una copia dei relativi valori di configurazione, che diventa il set di valori di attivazione. I valori di attivazione vengono mantenuti fino a quando la macchina virtuale non viene arrestata o riavviata. Si noti Windows Virtual PC può usare la configurazione solo per archiviare i valori per determinate chiavi, in altri casi il valore di attivazione non può mai essere usato.

> [!Note]  
> La sessione della macchina virtuale deve essere in esecuzione prima di poter modificare i valori di attivazione.

 

Le chiavi di attivazione vengono archiviate internamente in modo gerarchico simile alle chiavi del Registro di sistema in Windows. Per specificare una sottochiave specifica, viene costruito un "percorso di chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per impostare il valore della chiave "azione \_ predefinita" che si trova nell'albero delle chiavi seguente:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

La *stringa del percorso activationKey* viene specificata nel modo seguente:

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

