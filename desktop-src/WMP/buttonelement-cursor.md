---
title: BUTTONelement. Cursor
description: L'attributo Cursor specifica o Recupera il valore del cursore BUTTONelement visualizzato quando il mouse è posizionato sul pulsante.
ms.assetid: 29e7fadb-30d8-40e4-9a64-6b6f45eac80a
keywords:
- Media Player di Windows BUTTONelement. Cursor
topic_type:
- apiref
api_name:
- BUTTONELEMENT.cursor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f267cd54c36ad8f89a7242d7f428fd0d52b75fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333759"
---
# <a name="buttonelementcursor"></a>BUTTONelement. Cursor

L'attributo **Cursor** specifica o Recupera il valore del cursore **ButtonElement** visualizzato quando il mouse è posizionato sul **pulsante**.

``` syntax
        elementID.cursor
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura.



| Valore            | Descrizione                                                                                 |
|------------------|---------------------------------------------------------------------------------------------|
| sistema           | Valore predefinito. Cursore dipendente dalla piattaforma (in genere una freccia).                                      |
| a sinistra             | A sinistra.                                                                                       |
| help             | La freccia con il punto interrogativo che indica la guida è disponibile.                                      |
| sizeall          | Freccia a quattro punte che punta a nord, Sud, est e ovest.                                   |
| sizenesw         | Freccia a due punte che indica nordest e sud-ovest.                                      |
| sizens           | Freccia a due punte che punta verso nord e sud.                                              |
| sizenwse         | Freccia a due punte che indica nord-ovest e sud-est.                                      |
| sizewe           | Freccia a due punte che indica ovest e est.                                                |
| UpArrow          | Freccia verticale che punta verso l'alto.                                                             |
| \*. ani o \* . cur | Qualsiasi file. ani o. cur (deve trovarsi nella stessa directory del file con estensione WMS o nel file con estensione WMZ). |



 

## <a name="remarks"></a>Commenti

Se viene specificato un valore non valido, viene mantenuto il valore precedente.

I percorsi dei nomi di file di cursore vengono ignorati, pertanto il file di cursore deve trovarsi nella directory predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BUTTONelement (elemento)**](buttonelement-element.md)
</dt> </dl>

 

 





