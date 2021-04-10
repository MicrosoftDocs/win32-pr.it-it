---
description: La proprietà DVDAdm. BookmarkOnStop imposta o recupera un valore che indica all'oggetto MSWebDVD se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul pulsante Interrompi.
ms.assetid: bcadaa3c-23b7-4408-8199-058103a92a34
title: Proprietà BookmarkOnStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355ae01c43ef28a086c76f4716fe3d46d250fbe4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125055"
---
# <a name="bookmarkonstop-property"></a>Proprietà BookmarkOnStop

La `DVDAdm.BookmarkOnStop` proprietà imposta o recupera un valore che indica all'oggetto mswebdvd se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul pulsante **Interrompi** .

``` syntax
[ bBookmarkOnStop = ] DVD.DVDAdm.BookmarkOnStop
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se l'oggetto MSDVDAdm salverà un segnalibro di tutte le impostazioni DVD, inclusa la posizione sul disco, il livello padre e il paese padre/area geografica.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è false.

I segnalibri sono validi solo per un computer specifico. Un utente non può salvare un segnalibro e quindi inviarlo a un altro utente per leggere in un computer diverso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BookmarkOnClose**](bookmarkonclose-property.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



