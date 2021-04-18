---
title: Costanti WINBIO_POOL (tipi WinBio \_ . h)
description: Consente di specificare il tipo di pool di unità biometriche da usare nella sessione.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7af1ec8d5692a390bb91ecb63736bd94efb2e85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519024"
---
# <a name="winbio_pool-constants"></a>\_Costanti pool WINBIO

Nella funzione [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) è possibile usare le costanti seguenti per specificare il tipo di pool di unità biometriche da usare nella sessione.



| Costante                                                                                                                                                                                  | Descrizione                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_pool WINBIO \_ sconosciuto**</dt> </dl>          | Il tipo di pool è sconosciuto.<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_sistema pool \_ WINBIO**</dt> </dl>             | Specifica una raccolta condivisa di unità biometriche gestite dal provider di servizi.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**\_pool WINBIO \_ privato**</dt> </dl>          | Specifica una raccolta di unità biometriche gestite dal chiamante.<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**POOL WINBIO non \_ \_ assegnato**</dt> </dl> | Riservato.<br/>                                                                         |



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

 

 





