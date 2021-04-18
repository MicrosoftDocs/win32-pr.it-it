---
description: La classe CImageSample implementa un esempio di supporto che gestisce una bitmap (DIB) indipendente dal dispositivo GDI.
ms.assetid: 620ea791-458e-441e-8f0c-2184c44c742e
title: Classe CImageSample (Winutil. h)
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
ms.openlocfilehash: 2235d50c952ce1b76e4a70eda0341f0fe3c4167c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325047"
---
# <a name="cimagesample-class"></a>Classe CImageSample

![gerarchia di classi cimagesample](images/wutil03.png)

La `CImageSample` classe implementa un esempio di supporto che gestisce una bitmap (DIB) indipendente dal dispositivo GDI. Questa classe deriva dalla classe [**CMediaSample**](cmediasample.md) . È progettato per essere usato con la classe [**CImageAllocator**](cimageallocator.md) . La classe **CImageAllocator** fornisce un allocatore che crea `CImageSample` oggetti.



| Variabili membro protette                        | Descrizione                                                       |
|---------------------------------------------------|-------------------------------------------------------------------|
| [**\_DibData m**](cimagesample-m-dibdata.md)      | Contiene informazioni sulla DIB gestita da questo oggetto.  |
| [**m \_ Binit**](cimagesample-m-binit.md)          | Indica se l'oggetto è stato inizializzato.                |
| Metodi pubblici                                    | Descrizione                                                       |
| [**CImageSample**](cimagesample-cimagesample.md) | Metodo del costruttore.                                               |
| [**GetDIBData**](cimagesample-getdibdata.md)     | Recupera le informazioni relative alla DIB gestita da questo oggetto. |
| [**SetDIBData**](cimagesample-setdibdata.md)     | Imposta le informazioni sulla DIB gestite da questo oggetto.      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




