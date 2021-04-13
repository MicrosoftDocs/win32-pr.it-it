---
title: Metodo IVMVirtualPC SetConfigurationValue (VPCCOMInterfaces. h)
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
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518466"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a>Metodo IVMVirtualPC:: SetConfigurationValue

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*preferenceKey* \[ in\]
</dt> <dd>

Chiave utilizzata per identificare la preferenza, archiviata nel file di configurazione per utente (Options.xml in "% LocalAppData% \\ Microsoft \\ Windows Virtual PC").

> [!IMPORTANT]
> Le modifiche devono essere apportate Options.xml solo usando il metodo **SetConfigurationValue** . Non è supportata la modifica di Options.xml con altri metodi.

 

</dd> <dt>

*preferenceValue* \[ in\]
</dt> <dd>

Valore di preferenza. Questo valore può essere uno dei tipi **Variant** seguenti: VT **\_ Array** VT \| **\_ Ui1** (byte non elaborati), **VT \_ BSTR** (String) **, VT \_ UI4** (Integer) o **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice/valore restituito                                                                                                                                                                        | Descrizione                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | L'operazione è stata completata.<br/>                                                        |
| <dl> <dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt> </dl>                                | Il parametro *preferenceKey* o *preferenceValue* è **null**.<br/>                      |
| <dl> <dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG </dl>                             | Il parametro *preferenceKey* non è valido o è una stringa vuota.<br/>                    |
| <dl> <dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt> </dl>                        | Si è verificato un errore imprevisto.<br/>                                                    |
| <dl> <dt>**E \_**</dt> <dt>0x80070005</dt> AccessDenied </dl>                           | L'utente corrente non dispone di accesso sufficiente al file di configurazione.<br/>                  |
| <dl> <dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt> </dl> | Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).<br/> |



 

## <a name="remarks"></a>Commenti

Per il parametro *preferenceKey* sono supportati i valori seguenti.



| valore *preferenceKey*      | Descrizione                                                                                                                                                                           | Tipo di dati            | Valore predefinito   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| "timeout di inattività \_ "<br/> | Numero di secondi che vpc.exe deve attendere prima di uscire se non sono presenti macchine virtuali o applicazioni attive che utilizzano le [interfacce di Windows Virtual PC](virtual-pc-interfaces.md).<br/> | intero<br/> | 30<br/> |



 

Questo metodo fornisce l'accesso di basso livello a qualsiasi valore di configurazione. Può essere usato per impostare i valori di configurazione per le chiavi definite dal cliente. Prestare attenzione se si utilizza questo metodo per impostare i valori di configurazione di sistema, in quanto non viene eseguito alcun controllo degli errori sul valore di configurazione. Inoltre, alcuni valori di configurazione non possono essere modificati mentre una macchina virtuale è in esecuzione.

Le chiavi di configurazione si trovano nel file "Options.xml" della macchina virtuale in formato XML. Le chiavi vengono archiviate in modo gerarchico come le chiavi del registro di sistema di Windows. Per specificare una sottochiave specifica, viene creato un "percorso della chiave" che specifica le varie chiavi in un formato delimitato da barre.

Ad esempio, per impostare il valore della chiave "Idle \_ timeout" presente nell'albero delle chiavi seguente:

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

La stringa di percorso *preferenceKey* viene specificata come indicato di seguito:

``` syntax
"idle_timeout"
```

Se una delle chiavi nell'albero desiderato ha un valore di attributo "ID", l'attributo e il relativo valore vengono incorporati nella stringa del percorso *preferenceKey* immediatamente dopo la chiave di configurazione associata usando il formato racchiuso tra parentesi: " \[ @id ="*\_ valore ID*" \] ".

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

La stringa di percorso *preferenceKey* viene specificata come indicato di seguito:

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
| IID<br/>                      | IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> <dt>

[**IVMVirtualMachine::SetConfigurationValue**](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

