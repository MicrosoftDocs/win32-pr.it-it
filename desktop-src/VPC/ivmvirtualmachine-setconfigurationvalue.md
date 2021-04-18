---
title: Metodo IVMVirtualMachine SetConfigurationValue (VPCCOMInterfaces. h)
description: Imposta il valore dell'impostazione di configurazione specificata per la macchina virtuale (VM).
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Metodo SetConfigurationValue Virtual PC
- Metodo SetConfigurationValue Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302214"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>Metodo IVMVirtualMachine:: SetConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Imposta il valore dell'impostazione di configurazione specificata per la macchina virtuale (VM).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configurationKey* \[ in\]
</dt> <dd>

Chiave utilizzata per identificare il valore di configurazione archiviato nel \* file ". vmc".

> [!IMPORTANT]
> Le modifiche devono essere apportate a " \* . vmc" solo usando il metodo **SetConfigurationValue** . La modifica di " \* . vmc" con qualsiasi altro metodo non è supportata.

 

</dd> <dt>

*configurationValue* \[ in\]
</dt> <dd>

Valore di configurazione. Questo valore Cay è uno dei seguenti tipi **Variant** : VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String), **VT \_ UI4** (Integer) o **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                                                                            |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>      | Il parametro *configurationKey* è **null** o vuoto oppure il parametro *configurationValue* non è un tipo Variant valido.<br/> |
| <dl> <dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt> </dl> | La configurazione è sconosciuta.<br/>                                                                                            |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

Per il parametro *configurationKey* sono supportati i valori seguenti.



| valore *configurationKey*                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Tipo di dati            | Valore predefinito     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| "hardware/BIOS/ \_ sincronizzazione ora \_ all' \_ avvio"<br/>              | "true" Se il clock della macchina virtuale CMOS deve essere sincronizzato con il clock host all'avvio; "false" in caso contrario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Boolean<br/> | "true"<br/> |
| "Integration/Microsoft/host \_ time \_ Sync/Enabled" "<br/> | "true" se la sincronizzazione dell'ora dell'host è abilitata nei componenti di integrazione; "false" in caso contrario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Boolean<br/> | "true"<br/> |
| "Opzioni interfaccia utente \_ / \_ pubblicazione automatica app \_ "<br/>                  | "true" se la pubblicazione automatica delle applicazioni è abilitata nei componenti di integrazione; "false" in caso contrario. Questa operazione è detta anche applicazioni virtuali.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Boolean<br/> | "true"<br/> |
| "Opzioni interfaccia utente \_ /secondi \_ per il \_ salvataggio"<br/>                   | Numero di secondi di attesa prima del salvataggio della macchina virtuale dopo la chiusura di tutte le applicazioni. Tuttavia, i valori inferiori a 20 e più di 4.294.968 hanno un significato speciale. Per informazioni dettagliate, vedere l'elenco seguente<br/> <dl> <dt><span id="0"></span>0</dt> <dd> Non salvare mai la macchina virtuale.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Attendere 20 secondi prima di salvare la macchina virtuale.<br/> </dd> <dt><span id="214_294_967"></span>21 4.294.967</dt> <dd> Attendere il numero di secondi specificato prima di salvare la macchina virtuale.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4.294.968 4.294.967.295</dt> <dd> Attendere 4.294.968 secondi prima di salvare la macchina virtuale.<br/> </dd> </dl> | intero<br/> | 300<br/>    |



 

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione. Può essere usato per impostare i valori di configurazione per le chiavi definite dal cliente. Prestare attenzione se si utilizza questo metodo per impostare i valori di configurazione di sistema, in quanto non viene eseguito alcun controllo degli errori sul valore di configurazione. Inoltre, alcuni valori di configurazione non possono essere modificati mentre la macchina virtuale è in esecuzione.

Le chiavi di configurazione si trovano nel \* file ". vmc" della macchina virtuale in formato XML. Le chiavi vengono archiviate in modo gerarchico come le chiavi del registro di sistema di Windows. Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per impostare il valore della chiave "RAM \_ size" situata nell'albero delle chiavi seguente:

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

La stringa di percorso *configurationKey* viene specificata come indicato di seguito:

``` syntax
"hardware/memory/ram_size"
```

Se una delle chiavi nell'albero desiderato ha un valore di attributo "ID", l'attributo e il relativo valore vengono incorporati nella stringa del percorso *configurationKey* immediatamente dopo la chiave di configurazione associata usando il formato racchiuso tra parentesi: " \[ @id ="*\_ valore ID*" \] ".

Ad esempio, per impostare il valore della chiave "Golf" situata nell'albero delle chiavi seguente:

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

La stringa di percorso *configurationKey* viene specificata come indicato di seguito:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
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
</dt> <dt>

[**IVMVirtualPC::SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

