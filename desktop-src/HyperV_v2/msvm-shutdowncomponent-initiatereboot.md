---
description: Avvia un'operazione di riavvio del sistema operativo sulla macchina virtuale figlio associata.
ms.assetid: 9f3ebbaf-ee0f-4c01-8f73-1f37c08a0feb
title: Metodo InitiateReboot della classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateReboot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 527569e8a5d6c2bb0a54294637ae19c13f5e3af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308205"
---
# <a name="initiatereboot-method-of-the-msvm_shutdowncomponent-class"></a>Metodo InitiateReboot della classe MSVM \_ ShutdownComponent

Avvia un'operazione di riavvio del sistema operativo sulla macchina virtuale figlio associata.

Se viene restituito zero (0), il riavvio è stato avviato correttamente. Qualsiasi altro codice restituito indica una condizione di errore.

## <a name="syntax"></a>Sintassi


```mof
uint32 InitiateReboot(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Forza* \[ in\]
</dt> <dd>

Flag che, se TRUE, impone la chiusura delle applicazioni nonostante i dati non salvati.

</dd> <dt>

*Motivo* \[ in\]
</dt> <dd>

Motivo dell'operazione di riavvio. Si tratta di una stringa definita dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti:

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
</dt> <dt>

**File non trovato** (32779)
</dt> <dt>

**Il sistema non è pronto** (32780)
</dt> <dt>

**Il computer è bloccato e non può essere arrestato senza l'opzione Force** (32781)
</dt> <dt>

**È in corso un arresto del sistema** (32782)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ShutdownComponent MSVM**](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




