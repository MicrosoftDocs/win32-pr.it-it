---
description: KTM definisce le maschere di accesso alle transazioni seguenti da usare quando si apre una transazione.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Maschere di accesso alle transazioni (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faafcce45944e37418191254fc5a2b81d00d9248b27ea5e8753fe8e34a734754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520641"
---
# <a name="transaction-access-masks"></a>Maschere di accesso alle transazioni

KTM definisce le maschere di accesso alle transazioni seguenti da usare quando si apre una transazione.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**INFORMAZIONI \_ SULLE QUERY DI \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



Il chiamante può eseguire query sulle informazioni sulla transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**INFORMAZIONI \_ SUI SET DI \_ TRANSAZIONI**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



Il chiamante può impostare le informazioni sulla transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**INTEGRAZIONE \_ DELLE TRANSAZIONI**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



Il chiamante può integrarsi in questa transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**\_COMMIT TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



Il chiamante può eseguire il commit della transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**ROLLBACK \_ DELLE TRANSAZIONI**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



Il chiamante può eseguire il rollback di questa transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**PROPAGAZIONE \_ DELLE TRANSAZIONI**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



Il chiamante può propagare questa transazione a un gestore di risorse superiore, ad esempio Distributed Transaction Coordinator (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**LETTURA \_ GENERICA \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



Il chiamante ha i privilegi seguenti: **STANDARD \_ RIGHTS \_ READ,** **TRANSACTION QUERY \_ \_ INFORMATION** e **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**SCRITTURA \_ GENERICA \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



Il chiamante ha i privilegi seguenti: **STANDARD \_ RIGHTS \_ WRITE,** **TRANSACTION SET \_ \_ INFORMATION,** **TRANSACTION \_ COMMIT,** **TRANSACTION \_ ENLIST,** **TRANSACTION \_ ROLLBACK,** **TRANSACTION \_ PROPAGATE** e **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



Il chiamante ha i privilegi seguenti: **STANDARD \_ RIGHTS \_ EXECUTE,** **TRANSACTION \_ COMMIT,** **TRANSACTION \_ ROLLBACK** e **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



Il chiamante ha il privilegio **seguente: STANDARD \_ RIGHTS \_ REQUIRED,** **TRANSACTION GENERIC \_ \_ READ,** **TRANSACTION GENERIC \_ \_ WRITE** e **TRANSACTION GENERIC \_ \_ EXECUTE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**DIRITTI \_ DI TRANSACTION RESOURCE \_ \_ MANAGER**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



Il chiamante ha i privilegi seguenti: **TRANSACTION \_ GENERIC \_ READ,** **STANDARD RIGHTS \_ \_ WRITE,** **TRANSACTION SET \_ \_ INFORMATION, TRANSACTION** **\_ ROLLBACK,** **TRANSACTION \_ ENLIST,** **TRANSACTION \_ PROPAGATE** e **SYNCHRONIZE**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È consigliabile che i gestori delle risorse, quando si integrano in una transazione, specificano **TRANSACTION \_ RESOURCE MANAGER \_ \_ RIGHTS** all'apertura di una transazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




