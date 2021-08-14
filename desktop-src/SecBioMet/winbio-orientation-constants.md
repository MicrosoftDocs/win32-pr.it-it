---
title: WINBIO_ORIENTATION costanti (Winbio \_ types.h)
description: Le costanti seguenti specificano i possibili orientamenti della fotocamera specificati dal componente sensore come obbligatori.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73846137747af6cda3ed1728c8600f354f7ca458782a69f8494781f01b3ae75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909920"
---
# <a name="winbio_orientation-constants"></a>Costanti \_ DI ORIENTAMENTO WINBIO

Le costanti seguenti specificano i possibili orientamenti della fotocamera specificati dal componente sensore come obbligatori.



| Costante/valore                                                                                                                                                                                                                                                           | Descrizione                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <dt>**WINBIO \_ ORIENTAMENTO \_ NON SPECIFICATO**</dt> <dt>0</dt> </dl> | Non è specificato un orientamento obbligatorio per la fotocamera.<br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <dt>**WINBIO \_ ORIENTAMENTO \_ ORIZZONTALE**</dt> <dt>1</dt> </dl>       | L'orientamento orizzontale è necessario per la fotocamera.<br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <dt>**WINBIO \_ ORIENTAMENTO \_ VERTICALE**</dt> <dt>2</dt> </dl>          | L'orientamento verticale è obbligatorio per la fotocamera.<br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <dt>**WINBIO \_ ORIENTAMENTO \_ ANY**</dt> <dt>3</dt> </dl>                         | Qualsiasi orientamento è consentito per la fotocamera.<br/>             |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (includere Winbio.h per le applicazioni client o Adapters.h Winbio \_ per gli adapter)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SUI SENSORI ESTESI WINBIO \_ \_ \_**](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





