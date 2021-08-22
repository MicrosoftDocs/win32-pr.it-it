---
description: Simula una sequenza di tasti di rilascio stampa.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Metodo TypeKey della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d387e1b0d0d939d997589c90195b4a50427f1973eaf46520a0fa70caf62c610b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068351"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a>Metodo TypeKey della classe Keyboard \_ Msvm

Simula una sequenza di tasti di rilascio stampa. Equivale a chiamare [**PressKey seguito**](presskey-msvm-keyboard.md) da [**ReleaseKey**](releasekey-msvm-keyboard.md).

## <a name="syntax"></a>Sintassi


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*keyCode* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Codice del tasto virtuale del tasto da premere. Per l'elenco dei codici di chiave virtuale, vedere [**Codici di chiave virtuale**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Un valore restituito pari a zero indica l'esito positivo. Un valore diverso da zero indica un errore di modifica dello stato della chiave.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Tastiera Msvm \_**](msvm-keyboard.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Tastiera \_ Msvm**](msvm-keyboard.md)
</dt> <dt>

[**Codici di chiave virtuale**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

