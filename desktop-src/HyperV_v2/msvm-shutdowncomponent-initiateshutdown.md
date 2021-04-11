---
description: Avvia un'operazione di arresto del sistema operativo nella macchina virtuale figlio associata. Se viene restituito zero (0), l'arresto è stato avviato correttamente. Qualsiasi altro codice restituito indica una condizione di errore.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Metodo InitiateShutdown della classe Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232267"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Metodo InitiateShutdown della classe MSVM \_ ShutdownComponent

Avvia un'operazione di arresto del sistema operativo nella macchina virtuale figlio associata. Se viene restituito zero (0), l'arresto è stato avviato correttamente. Qualsiasi altro codice restituito indica una condizione di errore.

## <a name="syntax"></a>Sintassi


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Forza* \[ in\]
</dt> <dd>

Tipo: **booleano**

Flag che, se **true**, impone la chiusura delle applicazioni nonostante i dati non salvati.

</dd> <dt>

*Motivo* \[ in\]
</dt> <dd>

Tipo: **stringa**

Motivo dell'operazione di arresto. Si tratta di una stringa definita dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

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

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ ShutdownComponent di MSVM**](msvm-shutdowncomponent.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winreg. h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ShutdownComponent MSVM**](msvm-shutdowncomponent.md)
</dt> </dl>

 

