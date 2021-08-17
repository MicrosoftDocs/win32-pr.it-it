---
title: Metodo IVMVirtualMachine RemoveConfigurationValue (VPCCOMInterfaces.h)
description: Rimuove il valore dell'impostazione di configurazione specificata per questa macchina virtuale.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Metodo RemoveConfigurationValue Virtual PC
- Metodo RemoveConfigurationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 130feab953b5116ae8d6194f23cefc88c6792cf584ec884edd359ce6fc44a906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752290"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a>Metodo IVMVirtualMachine::RemoveConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Rimuove il valore dell'impostazione di configurazione specificata per questa macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave di configurazione* \[ Pollici\]
</dt> <dd>

Chiave usata per identificare il valore di configurazione archiviato nel \* file "vmc".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                      | Descrizione                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>           | Il parametro è **NULL** o vuoto.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl>      | La configurazione è sconosciuta.<br/>       |
| <dl> <dt>**Macchina virtuale \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl> | La preferenza non è stata trovata.<br/>       |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>      | Si è verificato un errore imprevisto.<br/>   |



 

## <a name="remarks"></a>Commenti

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione. Può essere usato per rimuovere i valori di configurazione per le chiavi definite dal cliente. Prestare attenzione se si usa questo metodo per rimuovere i valori di configurazione di sistema, poiché alcuni valori non possono essere modificati mentre la macchina virtuale è in esecuzione.

Le chiavi di configurazione si trovano nel \* file "vmc" della macchina virtuale in formato XML. Le chiavi vengono archiviate in modo gerarchico simile alle chiavi del Registro di sistema in Windows. Per specificare una sottochiave specifica, viene costruito un "percorso di chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per rimuovere il valore della chiave "ram \_ size" che si trova nell'albero delle chiavi seguente:

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

La *stringa di percorso configurationKey* viene specificata come segue:

``` syntax
"hardware/memory/ram_size"
```

Se una delle chiavi nell'albero desiderato ha un valore di attributo "id", l'attributo e il relativo valore vengono incorporati nella stringa di percorso *configurationKey* immediatamente dopo la chiave di configurazione associata usando il formato tra parentesi quadre seguente: " \[ @id ="*id \_ value*" \] ".

Ad esempio, per rimuovere il valore della chiave "absolute" che si trova nell'albero delle chiavi seguente:

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

La *stringa di percorso configurationKey* viene specificata come segue:

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
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

 

