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
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752234"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a>Metodo GetInteractiveSessionACL della classe MSVM \_ TerminalService

Recupera l' *elenco di controllo di accesso discrezionale* (DACL) corrente che controlla l'accesso alla sessione interattiva di una macchina virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale di cui verrà recuperato il DACL.

</dd> <dt>

*AccessControlList* \[ out\]
</dt> <dd>

Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**\_ InteractiveSessionACE MSVM**](msvm-interactivesessionace.md) che rappresenta una *voce di controllo di accesso* (ACE) nell'elenco DACL della sessione interattiva della macchina virtuale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

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

[**\_TerminalService MSVM**](msvm-terminalservice.md)
</dt> </dl>

 

 




