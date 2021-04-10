---
title: Costanti WINBIO_DB (tipi WinBio \_ . h)
description: Specificare il database da utilizzare per un pool di sistema.
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
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120230"
---
# <a name="winbio_db-constants"></a>\_Costanti database WINBIO

Quando si chiama [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) per specificare il database da utilizzare per un pool di sistema, è possibile utilizzare le costanti seguenti.



| Costante                                                                                                                                                                         | Descrizione                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**\_ \_ impostazione predefinita database WINBIO**</dt> </dl>       | Ogni unità biometrica nel pool di sensori usa il database predefinito specificato nella configurazione predefinita dell'unità biometrica.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**\_bootstrap del database WINBIO \_**</dt> </dl> | Può essere usato per gli scenari prima dell'avvio di Windows. In genere, il database fa parte del chip del sensore o fa parte del BIOS e può essere usato solo per la registrazione e l'eliminazione del modello.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ database \_ OnChip**</dt> </dl>          | Il database si trova sul chip del sensore.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





