---
title: VIDEO.cursor
description: L'attributo cursor specifica o recupera il valore del cursore utilizzato quando il mouse si trova su un'area selezionabile del video.
ms.assetid: 2faaf9cd-47be-47d5-ad4e-8f3bb322d812
keywords:
- Video.cursor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73c39b40412a02e145b8063f473272184e1d7cf03caaa170de19bde7fad37a50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134244"
---
# <a name="videocursor"></a>VIDEO.cursor

**L'attributo cursor** specifica o recupera il valore del cursore utilizzato quando il mouse si trova su un'area selezionabile del video.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una stringa di **lettura/scrittura.**



| Valore            | Descrizione                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Cursore dipendente dalla piattaforma (in genere una freccia).                                               |
| Mano             | Mano.                                                                                       |
| help             | Freccia con punto interrogativo che indica che la Guida è disponibile.                                      |
| sizeall          | Freccia a quattro punte che punta a nord, sud, est e ovest.                                   |
| sizenesw         | Freccia a due punte che punta verso nord-est e sud-ovest.                                      |
| sizens           | Freccia a due punte che punta a nord e a sud.                                              |
| dimensioninwse         | Freccia a due punte che punta a nord-ovest e a sud-est.                                      |
| sizewe           | Freccia a due punte che punta a ovest e a est.                                                |
| uparrow          | Freccia verticale che punta verso l'alto.                                                             |
| \*.ani o \* .cur | Qualsiasi file con estensione ani o cur (deve essere nella stessa directory del file con estensione wms o nel file wmz). |



 

## <a name="remarks"></a>Commenti

Ai fini del rendering, system è il cursore predefinito. Il valore predefinito recuperato da questo attributo è "" (stringa vuota).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 





