---
description: Avvia un'operazione di arresto del sistema operativo nella macchina virtuale figlio associata. Se viene restituito zero (0), l'arresto è stato avviato correttamente. Qualsiasi altro codice restituito indica una condizione di errore.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Metodo InitiateShutdown della Msvm_ShutdownComponent classe (Winreg.h)
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
ms.openlocfilehash: f128eb2babfed0c70aca063832e579ad254ca1b02d6beaefb451c64598faa8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950400"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Metodo InitiateShutdown della classe Msvm \_ ShutdownComponent

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

*Forza* \[ Pollici\]
</dt> <dd>

Tipo: **booleano**

Flag che, se **True, forza** la chiusura delle applicazioni nonostante siano presenti dati non salvati.

</dd> <dt>

*Motivo* \[ Pollici\]
</dt> <dd>

Tipo: **string**

Motivo dell'operazione di arresto. Si tratta di una stringa definita dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Non riuscito** (32768)
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
</dt> <dt>

**File non trovato** (32779)
</dt> <dt>

**Il sistema non è pronto** (32780)
</dt> <dt>

**Il computer è bloccato e non può essere arrestato senza l'opzione force** (32781)
</dt> <dt>

**Arresto del sistema in corso** (32782)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md) potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winreg.h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

