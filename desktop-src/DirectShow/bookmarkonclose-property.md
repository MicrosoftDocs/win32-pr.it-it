---
description: La proprietà DVDAdm.BookmarkOnClose imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente chiude l'applicazione.
ms.assetid: 54901ad6-7989-4fb3-bb28-f54c7a2bca44
title: Proprietà BookmarkOnClose
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83ed0ef05e2efe7edb3b6494e8f9709b23259207af257957551077dfbbddaba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103341"
---
# <a name="bookmarkonclose-property"></a>Proprietà BookmarkOnClose

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La proprietà imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente `DVDAdm.BookmarkOnClose` chiude l'applicazione.

``` syntax
[ bBookmarkOnClose = ] DVD.DVDAdm.BookmarkOnClose
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che, se true, indica che il controllo MSDVDAdm salverà un segnalibro di tutte le impostazioni DVD, inclusa la posizione sul disco, il livello di genitori e il paese/area geografica dei genitori quando l'utente chiude l'applicazione lettore DVD.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura con il valore predefinito true.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BookmarkOnStop**](bookmarkonstop-property.md)
</dt> <dt>

[Oggetto MSDVDAdm](msdvdadm-object.md)
</dt> </dl>

 

 



