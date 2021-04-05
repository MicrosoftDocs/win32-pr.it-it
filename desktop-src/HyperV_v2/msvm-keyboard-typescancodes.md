---
description: Simula una sequenza di chiavi usando i codici di analisi.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Metodo TypeScancodes della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752359"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a>Metodo TypeScancodes della classe della \_ tastiera MSVM

Simula una sequenza di chiavi usando i codici di analisi.

## <a name="syntax"></a>Sintassi


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Scancode* \[ in\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matrice che contiene i codici di analisi da digitare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Questo metodo restituisce 0 se ha esito positivo. Qualsiasi altro valore restituito indica un errore. Il valore restituito può essere uno dei valori seguenti.

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
</dt> </dl>

 

