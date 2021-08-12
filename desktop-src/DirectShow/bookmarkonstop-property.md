---
description: La proprietà DVDAdm.BookmarkOnStop imposta o recupera un valore che indica all'oggetto MSWebDVD se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul pulsante Arresta.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Proprietà BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c73d8b9829075125437e05da96c78d101f5a7f5df4dc2decc25f044cc3f5f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662673"
---
# <a name="bookmarkonstop-property"></a>Proprietà BookmarkOnStop

La proprietà imposta o recupera un valore che indica all'oggetto MSWebDVD se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul `DVDAdm.BookmarkOnStop` **pulsante** Arresta.

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se l'oggetto MSDVDAdm salverà un segnalibro di tutte le impostazioni DVD, tra cui la posizione sul disco, il livello di genitori e il paese/area geografica dei genitori.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con il valore predefinito false.

I segnalibri sono validi solo per un computer specifico. Un utente non può salvare un segnalibro e quindi inviarlo a un altro utente per leggere in un altro computer.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



