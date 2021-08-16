---
description: Recupera l'elenco di controllo di accesso discrezionale (DACL) corrente che controlla l'accesso alla sessione interattiva di una macchina virtuale.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Metodo GetInteractiveSessionACL della classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37f33ce16d0b5eb2b998f4f08a37a6e601f82d3aecf49a2e8e68b2a7f571a01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253721"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a>Metodo GetInteractiveSessionACL della classe Msvm \_ TerminalService

Recupera l'elenco di controllo di *accesso discrezionale* (DACL) corrente che controlla l'accesso alla sessione interattiva di una macchina virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a un'istanza della [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale di cui verrà recuperato l'elenco DACL.

</dd> <dt>

*AccessControlList* \[ Cambio\]
</dt> <dd>

Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della [**classe Msvm \_ InteractiveSessionACE**](msvm-interactivesessionace.md) che rappresenta una voce di controllo di accesso (ACE) nell'elenco DACL della sessione interattiva della macchina virtuale. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non** valido (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

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

[**Msvm \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

 




