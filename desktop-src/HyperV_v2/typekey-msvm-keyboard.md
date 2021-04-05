---
description: Simula una sequenza di tasti stampa-rilascio.
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
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968324"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a>Metodo TypeKey della classe della \_ tastiera MSVM

Simula una sequenza di tasti stampa-rilascio. Equivale alla chiamata a [**pulsanteper**](presskey-msvm-keyboard.md) seguita da [**ReleaseKey**](releasekey-msvm-keyboard.md).

## <a name="syntax"></a>Sintassi


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*codice* \[ di stato in\]
</dt> <dd>

Tipo: **UInt32**

Codice chiave virtuale della chiave da premere. Per l'elenco dei codici delle chiavi virtuali, vedere [**codici a chiave virtuale**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Un valore restituito pari a zero indica esito positivo. Un valore diverso da zero indica un errore di modifica dello stato della chiave.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Tastiera MSVM**](msvm-keyboard.md)
</dt> <dt>

[**Codici chiave virtuale**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

