---
description: KTM definisce le maschere di accesso all'integrazione seguenti da usare quando si apre una gestione transazioni.
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Maschere di accesso per la gestione transazioni (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfa093f38898ec49a789699fc5c7230612ef744fec78f200021361327d9f714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913901"
---
# <a name="transaction-manager-access-masks"></a>Maschere di accesso per la gestione transazioni

KTM definisce le maschere di accesso all'integrazione seguenti da usare quando si apre una gestione transazioni.

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**INFORMAZIONI SULLE \_ QUERY \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



Il chiamante può eseguire query sulle informazioni su questo TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**INFORMAZIONI SUI \_ SET \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



Il chiamante può impostare informazioni su questo TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER \_ RECOVER**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



Il chiamante può ripristinare questa TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**RIDENOMINAZIONE DI \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



Il chiamante può rinominare un'istanza TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ CREATE \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



Il chiamante può creare un gestore di risorse associato a questo TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER \_ BIND \_ TRANSACTION**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Questo valore è riservato.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**LETTURA \_ GENERICA TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **STANDARD \_ RIGHTS READ \_ e** **TRANSACTIONMANAGER QUERY \_ \_ INFORMATION**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**SCRITTURA \_ GENERICA TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



Il chiamante dispone dei privilegi seguenti: **STANDARD \_ RIGHTS \_ WRITE,** **TRANSACTIONMANAGER SET \_ \_ INFORMATION,** **TRANSACTIONMANAGER \_ RECOVER,** **TRANSACTIONMANAGER \_ RENAME** e **TRANSACTIONMANAGER CREATE \_ \_ RM.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**ESECUZIONE GENERICA DI TRANSACTIONMANAGER \_ \_**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



Il chiamante ha il privilegio seguente: **STANDARD \_ RIGHTS \_ EXECUTE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER \_ ALL \_ ACCESS**
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
| Intestazione<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




