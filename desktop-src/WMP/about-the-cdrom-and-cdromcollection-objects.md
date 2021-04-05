---
title: Informazioni sugli oggetti cdrom e cdromcollection
description: Informazioni sugli oggetti cdrom e cdromcollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player, oggetto cdrom
- Modello a oggetti di Windows Media Player, oggetto cdrom
- modello a oggetti, oggetto cdrom
- Controllo ActiveX Windows Media Player, oggetto cdrom
- Controllo ActiveX, oggetto cdrom
- Controllo ActiveX Windows Media Player Mobile, oggetto cdrom
- Windows Media Player Mobile, oggetto cdrom
- Oggetto cdrom
- Windows Media Player, oggetto cdromcollection
- Modello a oggetti di Windows Media Player, oggetto cdromcollection
- modello a oggetti, oggetto cdromcollection
- Controllo ActiveX Windows Media Player, oggetto cdromcollection
- Controllo ActiveX, oggetto cdromcollection
- Controllo ActiveX Windows Media Player Mobile, oggetto cdromcollection
- Oggetto Windows Media Player Mobile, cdromcollection
- Oggetto cdromcollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711401"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a>Informazioni sugli oggetti cdrom e cdromcollection

Gli oggetti **CDROM** e **cdromcollection** governano l'interfaccia per le unità CD del computer per la lettura e la riproduzione di CDS.

È possibile accedere all'oggetto **cdromcollection** solo tramite la proprietà **cdromcollection** dell'oggetto **Player** . La proprietà **cdromcollection** restituisce l'oggetto **cdromcollection** . È possibile accedere alle proprietà dell'oggetto **cdromcollection** solo dopo averlo creato. Ad esempio, per usare la proprietà **count** , è necessario usare il codice seguente:


```C++
mycount = player.cdromcollection.count;
```



È possibile accedere all'oggetto **CDROM** solo tramite l'oggetto **cdromcollection** . Ad esempio, per estrarre il CD utilizzando il metodo **eject** , è necessario innanzitutto creare l'oggetto raccolta e quindi un elemento nell'oggetto. Per estrarre il CD, usare il codice seguente:


```C++
player.cdromcollection.item(0).eject();
```



In entrambi i casi, si crea prima l'oggetto raccolta (**cdromcollection**) e quindi si recupera un oggetto specifico della raccolta. L'oggetto è il primo elemento della raccolta, **Item**(0), che corrisponde alla prima unità CD. Quindi, si chiama un metodo, **eject**, su tale elemento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto cdrom**](cdrom-object.md)
</dt> <dt>

[**Oggetto cdromcollection**](cdromcollection-object.md)
</dt> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




