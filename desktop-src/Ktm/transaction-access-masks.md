---
description: KTM definisce le seguenti maschere di accesso alle transazioni da utilizzare per l'apertura di una transazione.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Maschere di accesso alle transazioni (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311130"
---
# <a name="transaction-access-masks"></a>Maschere di accesso alle transazioni

KTM definisce le seguenti maschere di accesso alle transazioni da utilizzare per l'apertura di una transazione.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_informazioni query \_ transazione**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



Il chiamante può eseguire query sulle informazioni sulle transazioni.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_informazioni sul set di transazioni \_**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



Il chiamante può impostare le informazioni sulle transazioni.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**integrazione della transazione \_**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



Il chiamante può integrarsi in questa transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**\_commit transazione**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



Il chiamante può eseguire il commit della transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**ROLLBACK delle transazioni \_**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



Il chiamante può eseguire il rollback della transazione.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**\_propagazione transazione**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



Il chiamante può propagare questa transazione a un gestore di risorse superiore, ad esempio il Distributed Transaction Coordinator (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_lettura generica transazione \_**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **\_ diritti standard \_ letti**, **\_ \_ informazioni sulle query di transazione** e **sincronizzazione**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_scrittura generica transazione \_**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **\_ \_ scrittura diritti standard**, **\_ \_ informazioni sui set di transazioni**, **\_ commit transazioni**, **\_ integrazione transazioni**, **\_ rollback transazioni**, **\_ propagazione transazioni** e **sincronizzazione**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_esecuzione generica transazione \_**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **\_ diritti standard \_ Execute**, **\_ commit transazione**, **\_ rollback transazioni** e **sincronizzazione**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_accesso a tutte le transazioni \_**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



Il chiamante dispone del privilegio seguente: **\_ diritti standard \_ necessari**, **\_ \_ lettura generica** transazione **, \_ \_ scrittura** generica transazione e **\_ \_ esecuzione generica transazione**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_diritti di \_ gestione \_ risorse transazioni**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **transazione \_ \_ lettura generica**, **\_ \_ scrittura diritti standard**, **\_ \_ informazioni sui set di transazioni**, **\_ rollback delle** transazioni, **\_ integrazione delle** transazioni, **\_ propagazione delle transazioni** e **sincronizzazione**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È consigliabile che i gestori di risorse, durante l'integrazione in una transazione, specifichino **\_ \_ \_ i diritti di gestione delle risorse di transazione** durante l'apertura di una transazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




