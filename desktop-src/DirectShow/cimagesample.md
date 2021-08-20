---
description: La classe CImageSample implementa un esempio multimediale che gestisce una bitmap GDI indipendente dal dispositivo (DIB).
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Classe CImageSample (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afd19b6aba7546ec420985adf6d58d3f7acc7546913ec8f1c168c80ad3b7ffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402409"
---
# <a name="cimagesample-class"></a>Classe CImageSample

![Gerarchia di classi cimagesample](images/wutil03.png)

La classe implementa un esempio multimediale che gestisce una bitmap GDI indipendente dal dispositivo `CImageSample` (DIB). Questa classe deriva dalla [**classe CMediaSample.**](cmediasample.md) Deve essere usato con la [**classe CImageAllocator.**](cimageallocator.md) La **classe CImageAllocator** fornisce un allocatore che crea `CImageSample` oggetti.



| Variabili membro protette                        | Descrizione                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**m \_ DibData**](cimagesample-m-dibdata.md)      | Contiene informazioni sulla dib che questo oggetto sta gestendo.  |
| [**m \_ bInit**](cimagesample-m-binit.md)          | Indica se l'oggetto è stato inizializzato.                |
| Metodi pubblici                                    | Descrizione                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | Metodo del costruttore.                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | Recupera informazioni sulla dib che l'oggetto sta gestendo. |
| [**SetDIBData**](cimagesample-setdibdata.md)     | Imposta le informazioni sulla dib che l'oggetto gestisce.      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




