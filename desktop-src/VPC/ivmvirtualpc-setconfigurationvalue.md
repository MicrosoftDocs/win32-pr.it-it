---
title: Metodo IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces.h)
description: Imposta il valore dell'impostazione di configurazione specificata.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Metodo SetConfigurationValue Virtual PC
- Metodo SetConfigurationValue Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo SetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d3ea585182794c1e96195fdbef842bc35c86342d390dd59e7077b31d4ef9a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591704"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>Metodo IVMVirtualPC::SetConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Imposta il valore dell'impostazione di configurazione specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*preferenceKey* \[ Pollici\]
</dt> <dd>

Chiave usata per identificare la preferenza, archiviata nel file di configurazione per utente (Options.xml in "%LocalAppData% \\ Microsoft \\ Windows Virtual PC").

> [!IMPORTANT]
> È consigliabile apportare modifiche Options.xml solo usando il **metodo SetConfigurationValue.** La Options.xml con qualsiasi altro metodo non è supportata.

 

</dd> <dt>

*preferenceValue* \[ Pollici\]
</dt> <dd>

Valore della preferenza. Questo valore può essere uno dei tipi **VARIANT** seguenti: **VT \_ ARRAY** \| **VT \_ UI1** (byte non elaborati), **VT \_ BSTR** (stringa), **VT \_ UI4** (integer) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ Puntatore**</dt> <dt>0x80004003</dt> </dl>                                | Il *parametro preferenceKey* o *preferenceValue* è **NULL.**<br/>                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | Il *parametro preferenceKey* non è valido o è una stringa vuota.<br/>                    |
| <dl> <dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**E \_ Accesso negato**</dt> <dt>0x80070005</dt> </dl>                           | L'utente corrente non ha accesso sufficiente al file di configurazione.<br/>                  |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ VIRTUALIZZAZIONE HARDWARE \_ DISABILITATA**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni haV (Hardware Accelerated Virtualization).<br/> |



 

## <a name="remarks"></a>Commenti

Per il parametro *preferenceKey* sono supportati i valori seguenti.



| *valore preferenceKey*      | Descrizione                                                                                                                                                                           | Tipo di dati            | Valore predefinito   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| "timeout di \_ inattività"<br/> | Numero di secondi di attesa vpc.exe prima di uscire se non sono presenti macchine virtuali o applicazioni attive che usano le interfacce Windows [Virtual PC.](virtual-pc-interfaces.md)<br/> | "integer"<br/> | "30"<br/> |



 

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione. Può essere usato per impostare i valori di configurazione per le chiavi definite dal cliente. Prestare attenzione se si usa questo metodo per impostare i valori di configurazione di sistema, perché non viene eseguito alcun controllo degli errori sul valore di configurazione. Inoltre, alcuni valori di configurazione non possono essere modificati durante l'esecuzione di una macchina virtuale.

Le chiavi di configurazione si trovano nel file "Options.xml" della macchina virtuale in formato XML. Le chiavi vengono archiviate in modo gerarchico simile alle chiavi del Registro di sistema in Windows. Per specificare una sottochiave specifica, viene costruito un "percorso di chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per impostare il valore della chiave \_ "idle timeout" che si trova nell'albero delle chiavi seguente:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

La *stringa di percorso preferenceKey* viene specificata come segue:

``` syntax
"idle_timeout"
```

Se una delle chiavi nell'albero desiderato ha un valore di attributo "id", l'attributo e il relativo valore vengono incorporati nella stringa di percorso *preferenceKey* immediatamente dopo la chiave di configurazione associata usando il formato tra parentesi quadre seguente: " \[ @id ="*id \_ valore*" \] ".

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

La *stringa di percorso preferenceKey* viene specificata come segue:

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
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

