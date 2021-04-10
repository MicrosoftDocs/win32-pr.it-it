---
title: Costanti WINBIO_BIR_QUALITY (tipi WinBio \_ . h)
description: Specificare la qualità relativa dei dati biometrici in BIR se non è stato specificato un valore intero compreso tra 0 e 100.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121446"
---
# <a name="winbio_bir_quality-constants"></a>\_Costanti di \_ qualità WINBIO Bir

I flag seguenti vengono usati dal membro **dataquality** della struttura dell' [**\_ \_ intestazione WINBIO bir**](winbio-bir-header.md) per specificare la qualità relativa dei dati biometrici in Bir se non è stato specificato un valore intero compreso tra 0 e 100.



| Costante/valore                                                                                                                                                                                                                                                                       | Descrizione                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ DATA \_ Quality \_ non \_ impostata**</dt> <dt> 1</dt> </dl>                   | Le misurazioni di qualità sono supportate dal creatore di BIR, ma in BIR non è impostato alcun valore.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ DATA \_ Quality \_ non \_ supportata**</dt> <dt> 2</dt> </dl> | Le misurazioni di qualità non sono supportate da BIR Creator.<br/>                             |



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

 

 





