---
description: La proprietà DVDAdm. BookmarkOnClose imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente chiude l'applicazione.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Proprietà BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfbbfe194a496dba3568b7dfa4d75b97d4ed57c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341926"
---
# <a name="bookmarkonclose-property"></a>Proprietà BookmarkOnClose

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DVDAdm.BookmarkOnClose` proprietà imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente chiude l'applicazione.

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che, se impostato su true, indica che il controllo MSDVDAdm salverà un segnalibro di tutte le impostazioni DVD, inclusa la posizione su disco, il livello padre e il paese/area padre quando l'utente chiude l'applicazione DVD Player.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e il valore predefinito è true.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



