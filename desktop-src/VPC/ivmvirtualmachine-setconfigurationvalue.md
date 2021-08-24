---
title: Metodo IVMVirtualMachine SetConfigurationValue (VPCCOMInterfaces.h)
description: Imposta il valore dell'impostazione di configurazione specificata per questa macchina virtuale(VM).
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
ms.openlocfilehash: 7edef64484161f6151b1d2ac14fd6916a7d2a082c0c787b983019305027f4949
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652971"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a>Metodo IVMVirtualMachine::SetConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Imposta il valore dell'impostazione di configurazione specificata per questa macchina virtuale(VM).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave di configurazione* \[ Pollici\]
</dt> <dd>

Chiave usata per identificare il valore di configurazione archiviato nel \* file "vmc".

> [!IMPORTANT]
> Le modifiche devono essere apportate a \* "vmc" solo usando il **metodo SetConfigurationValue.** La modifica \* di ".vmc" con qualsiasi altro metodo non è supportata.

 

</dd> <dt>

*configurationValue* \[ Pollici\]
</dt> <dd>

Valore di configurazione. Questo valore può essere uno dei tipi **VARIANT** seguenti: **VT \_ ARRAY** \| **VT \_ UI1** (byte non elaborati), **VT \_ BSTR** (stringa), **VT \_ UI4** (integer) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                 | Descrizione                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>                                                                                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | Il *parametro configurationKey* è **NULL** o vuoto oppure il *parametro configurationValue* non è un tipo variant valido.<br/> |
| <dl> <dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA**</dt> <dt>0xA0040207</dt> </dl> | La configurazione è sconosciuta.<br/>                                                                                            |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>                                                                                        |



 

## <a name="remarks"></a>Commenti

Per il parametro *configurationKey* sono supportati i valori seguenti.



| *valore configurationKey*                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Tipo di dati            | Valore predefinito     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| "hardware/bios/time \_ sync \_ at \_ boot"<br/>              | "true" se l'orologio CMOS della macchina virtuale deve essere sincronizzato con l'orologio dell'host all'avvio; "false" in caso contrario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | "boolean"<br/> | "true"<br/> |
| "integration/microsoft/host \_ time \_ sync/enabled""<br/> | "true" se nei componenti di integrazione è abilitata la sincronizzazione dell'ora dell'host; "false" in caso contrario.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | "boolean"<br/> | "true"<br/> |
| "opzioni \_ dell'interfaccia utente/pubblicazione \_ automatica \_ dell'app"<br/>                  | "true" se la pubblicazione automatica delle applicazioni è abilitata nei componenti di integrazione; "false" in caso contrario. Questa operazione è detta anche applicazioni virtuali.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | "boolean"<br/> | "true"<br/> |
| "opzioni \_ dell'interfaccia \_ utente/secondi per il \_ salvataggio"<br/>                   | Numero di secondi di attesa prima del salvataggio della macchina virtuale dopo la chiusura di tutte le applicazioni. Tuttavia, i valori inferiori a 20 e superiori a 4.294.968 hanno significati speciali. Per informazioni dettagliate, vedere l'elenco seguente<br/> <dl> <dt><span id="0"></span>0</dt> <dd> Non salvare mai la macchina virtuale.<br/> </dd> <dt><span id="120"></span>1 20</dt> <dd> Attendere 20 secondi prima di salvare la macchina virtuale.<br/> </dd> <dt><span id="214_294_967"></span>21 4,294,967</dt> <dd> Attendere il numero di secondi specificato prima di salvare la macchina virtuale.<br/> </dd> <dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt> <dd> Attendere 4.294.968 secondi prima di salvare la macchina virtuale.<br/> </dd> </dl> | "integer"<br/> | 300<br/>    |



 

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione. Può essere usato per impostare i valori di configurazione per le chiavi definite dal cliente. Prestare attenzione se si usa questo metodo per impostare i valori di configurazione di sistema, perché non viene eseguito alcun controllo degli errori sul valore di configurazione. Inoltre, alcuni valori di configurazione non possono essere modificati mentre la macchina virtuale è in esecuzione.

Le chiavi di configurazione si trovano nel \* file "vmc" della macchina virtuale in formato XML. Le chiavi vengono archiviate in modo gerarchico simile alle chiavi del Registro di sistema in Windows. Per specificare una sottochiave specifica, viene costruito un "percorso di chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per impostare il valore della chiave "ram \_ size" che si trova nell'albero delle chiavi seguente:

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

La *stringa di percorso configurationKey* viene specificata come segue:

``` syntax
"hardware/memory/ram_size"
```

Se una delle chiavi nell'albero desiderato ha un valore di attributo "id", l'attributo e il relativo valore vengono incorporati nella stringa di percorso *configurationKey* immediatamente dopo la chiave di configurazione associata usando il formato tra parentesi quadre seguente: " \[ @id ="*id \_ value*" \] ".

Ad esempio, per impostare il valore della chiave "tutto" che si trova nell'albero delle chiavi seguente:

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

La *stringa di percorso configurationKey* viene specificata come segue:

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
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
</dt> <dt>

[**IVMVirtualPC::SetConfigurationValue**](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

