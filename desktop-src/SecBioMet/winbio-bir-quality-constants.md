---
title: WINBIO_BIR_QUALITY costanti (Winbio \_ types.h)
description: Specificare la qualità relativa dei dati biometrici nel BIR se non è stato specificato un valore intero compreso tra 0 e 100.
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
ms.openlocfilehash: 5bbb5139b1420ea3dbfbc9e37a9dc07421788bb051acb40449e9c0117031320e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911053"
---
# <a name="winbio_bir_quality-constants"></a>Costanti WINBIO \_ BIR \_ QUALITY

I flag seguenti vengono usati dal membro **DataQuality** della struttura [**WINBIO \_ BIR \_ HEADER**](winbio-bir-header.md) per specificare la qualità relativa dei dati biometrici nel BIR se non è stato specificato un valore intero compreso tra 0 e 100.



| Costante/valore                                                                                                                                                                                                                                                                       | Descrizione                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ DATA \_ QUALITY NON IMPOSTATO \_ \_ SU**</dt> <dt> 1</dt> </dl>                   | Le misurazioni di qualità sono supportate dall'autore di BIR, ma non viene impostato alcun valore nel BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ DATA \_ QUALITY \_ NON \_ SUPPORTATO**</dt> <dt> 2</dt> </dl> | Le misurazioni di qualità non sono supportate dall'autore di BIR.<br/>                             |



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

 

 





