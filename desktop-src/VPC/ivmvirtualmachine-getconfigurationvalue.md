---
title: Metodo IVMVirtualMachine GetConfigurationValue (VPCCOMInterfaces. h)
description: Recupera il valore dell'impostazione di configurazione specificata per questa macchina virtuale.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Metodo GetConfigurationValue Virtual PC
- Metodo GetConfigurationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400694"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a>Metodo IVMVirtualMachine:: GetConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera il valore dell'impostazione di configurazione specificata per questa macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configurationKey* \[ in\]
</dt> <dd>

Chiave utilizzata per identificare il valore di configurazione archiviato nel \* file ". vmc".

</dd> <dt>

*configurationValue* \[ out, retval\]
</dt> <dd>

Valore di configurazione. Questo valore può essere uno dei tipi **Variant** seguenti: VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String) **, VT \_ I4** (Integer) o **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                      | Descrizione                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>                          |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>           | Il parametro *configurationKey* è **null** o vuoto.<br/> |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>              | Il parametro *configurationValue* è **null**.<br/>        |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl>      | La configurazione è sconosciuta.<br/>                          |
| <dl> <dt>**Macchina virtuale \_ E \_ pref \_ non \_ trovato**</dt> <dt>0xA0040300</dt> </dl> | La preferenza non è stata trovata.<br/>                          |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>      | Si è verificato un errore imprevisto.<br/>                      |



 

## <a name="remarks"></a>Commenti

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione. Può essere usato per leggere i valori di configurazione per le chiavi definite dal cliente.

Le chiavi di configurazione si trovano nel \* file ". vmc" della macchina virtuale in formato XML. Le chiavi vengono archiviate in modo gerarchico come le chiavi del registro di sistema di Windows. Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per leggere il valore della chiave "RAM \_ size" situata nell'albero delle chiavi seguente:

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

La stringa di percorso *configurationKey* viene specificata come indicato di seguito:

``` syntax
"hardware/memory/ram_size"
```

Se una delle chiavi nell'albero desiderato ha un valore di attributo "ID", l'attributo e il relativo valore vengono incorporati nella stringa del percorso *configurationKey* immediatamente dopo la chiave di configurazione associata usando il formato racchiuso tra parentesi: " \[ @id ="*\_ valore ID*" \] ".

Ad esempio, per leggere il valore della chiave "Absolute" situata nell'albero delle chiavi seguente:

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

La stringa di percorso *configurationKey* viene specificata come indicato di seguito:

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
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

 

