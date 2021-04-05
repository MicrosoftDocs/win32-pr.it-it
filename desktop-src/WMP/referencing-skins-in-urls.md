---
title: Riferimento a interfacce in URL
description: Riferimento a interfacce in URL
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Windows Media Player Skin, riferimenti URL
- interfacce, riferimenti URL
- Riferimenti URL nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714047"
---
# <a name="referencing-skins-in-urls"></a>Riferimento a interfacce in URL

Se si utilizza un URL per caricare un file multimediale che verrà riprodotto da Windows Media Player, è possibile richiedere l'utilizzo di una particolare interfaccia con tale file. Se l'interfaccia è già installata nel computer dell'utente, verrà utilizzata. in caso contrario, verrà utilizzata l'interfaccia precedente.

Per richiedere un'interfaccia personalizzata, aggiungere quanto segue alla fine dell'URL:


```C++
?WMPSkin=skinname
```



*SkinName* è il nome dell'interfaccia che si vuole richiedere. Non usare le virgolette intorno al nome dell'interfaccia.

Per richiedere, ad esempio, l'utilizzo dell'interfaccia Headspace, digitare l'URL http seguente:


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulle interfacce**](about-skins.md)
</dt> </dl>

 

 




