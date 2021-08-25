---
title: WINBIO_DB costanti (Winbio \_ types.h)
description: Specificare il database da usare per un pool di sistema.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9d8392fd38e9d53588002c8aeab688ffc8b76efced83819318d9c6b6c2b721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867981"
---
# <a name="winbio_db-constants"></a>Costanti del database WINBIO \_

Le costanti seguenti possono essere usate quando si chiama [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) per specificare il database da usare per un pool di sistema.



| Costante                                                                                                                                                                         | Descrizione                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA DI WINBIO \_ \_ DB**</dt> </dl>       | Ogni unità biometrica nel pool di sensori usa il database predefinito specificato nella configurazione predefinita dell'unità biometrica.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**BOOTSTRAP DEL DATABASE WINBIO \_ \_**</dt> </dl> | Può essere usato per gli scenari prima di iniziare Windows. In genere, il database fa parte del chip del sensore o fa parte del BIOS e può essere usato solo per la registrazione e l'eliminazione di modelli.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ DB \_ ONCHIP**</dt> </dl>          | Il database si trova nel chip del sensore.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





