---
description: Revoca l'accesso alla sessione interattiva della macchina virtuale dall'elenco specificato di trustees.
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Metodo RevokeInteractiveSessionAccess della classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 48fa52d97e58e421442c77f1503e72bb6a3d793e35a4d1dbd12624bffdbcd9d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746201"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a>Metodo RevokeInteractiveSessionAccess della classe Msvm \_ TerminalService

Revoca l'accesso alla sessione interattiva della macchina virtuale dall'elenco specificato di trustees.

## <a name="syntax"></a>Sintassi


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ComputerSystem* \[ Pollici\]
</dt> <dd>

Riferimento a un'istanza della classe [**\_ ComputerSystem CIM**](cim-computersystem.md) che rappresenta la macchina virtuale a cui verrà revocato l'accesso.

</dd> <dt>

*Fiduciari* \[ Pollici\]
</dt> <dd>

Matrice di stringhe, ognuna delle quali identifica un trustee i cui diritti di accesso verranno revocati. Gli identificatori del trustee devono essere specificati in Windows formato compatibile con SAM o Windows formato stringa SID.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
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
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

