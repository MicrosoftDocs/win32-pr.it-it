---
title: Metodo IVMVirtualMachine RemoveActivationValue (VPCCOMInterfaces. h)
description: Rimuove il valore dell'impostazione di attivazione specificata per questa macchina virtuale.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Metodo RemoveActivationValue Virtual PC
- Metodo RemoveActivationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveActivationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048457"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a>Metodo IVMVirtualMachine:: RemoveActivationValue

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Rimuove il valore dell'impostazione di attivazione specificata per questa macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attivazione* \[ in\]
</dt> <dd>

Chiave utilizzata per identificare il valore di attivazione archiviato nel \* file ". vmc".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                      | Descrizione                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>                                                |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>           | Il parametro è **null** o vuoto.<br/>                                          |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>      | La configurazione è sconosciuta.<br/>                                                |
| <dl> <dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt> </dl> | La preferenza non è stata trovata o questa configurazione non ha un'attivazione valida.<br/> |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>      | Si è verificato un errore imprevisto.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di attivazione. Può essere usato per rimuovere i valori di attivazione per le chiavi definite dal cliente. Prestare attenzione se si utilizza questo metodo per rimuovere i valori di attivazione del sistema, poiché alcuni valori non possono essere modificati mentre la macchina virtuale è in esecuzione. Quando viene avviata una macchina virtuale, viene creata una copia dei valori di configurazione, che diventa il set di valori di attivazione. I valori di attivazione vengono mantenuti fino a quando la macchina virtuale non viene arrestata o riavviata. Si noti che Windows Virtual PC può utilizzare la configurazione solo per archiviare i valori per determinate chiavi, ovvero il valore di attivazione non può mai essere utilizzato.

> [!Note]  
> Per modificare i valori di attivazione, è necessario che la sessione della macchina virtuale sia in esecuzione.

 

Le chiavi di attivazione sono archiviate internamente in modo gerarchico Analogamente alle chiavi del registro di sistema di Windows. Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per rimuovere il valore della \_ chiave "azione predefinita" situata nell'albero delle chiavi seguente:

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

La stringa di percorso *attivazione* viene specificata come indicato di seguito:

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

