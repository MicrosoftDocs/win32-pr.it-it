---
description: KTM definisce le seguenti maschere di accesso all'elenco da utilizzare per l'apertura di una gestione transazioni (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Maschere di accesso di gestione transazioni (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881210"
---
# <a name="transaction-manager-access-masks"></a>Maschere di accesso di gestione transazioni

KTM definisce le seguenti maschere di accesso all'elenco da utilizzare per l'apertura di una gestione transazioni (TM).

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_ \_ informazioni sulle query TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



Il chiamante può eseguire query sulle informazioni relative a questa TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_informazioni sui set di TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Il chiamante può impostare informazioni su questo TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**\_ripristino TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Il chiamante può recuperare questa TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**ridenominazione TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Il chiamante può rinominare un'istanza TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ creare \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Il chiamante può creare un gestore di risorse associato a questa TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_transazione di binding TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Questo valore è riservato.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_lettura generica TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **informazioni \_ sui diritti standard \_ Read** e **TRANSACTIONMANAGER \_ query \_**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_scrittura generica TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



Il chiamante presenta i privilegi seguenti: **standard \_ Rights \_ Write**, **TRANSACTIONMANAGER \_ set \_ Information**, **TRANSACTIONMANAGER \_ Recover**, **TRANSACTIONMANAGER \_ Rename** e **TRANSACTIONMANAGER \_ Create \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_esecuzione generica TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



Il chiamante presenta il privilegio seguente: **\_ diritti standard \_ Execute**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER \_ tutti gli \_ accessi**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



Questo valore imposta tutti i bit validi per un valore di accesso TM.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                           |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinNT. h</dt> </dl> |



 

 




