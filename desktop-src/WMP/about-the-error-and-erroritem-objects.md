---
title: Informazioni sugli oggetti Error e ErrorItem
description: Informazioni sugli oggetti Error e ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player,Oggetto Error
- Windows Media Player a oggetti, oggetto Error
- modello a oggetti,oggetto Error
- Windows Media Player ActiveX, oggetto Error
- ActiveX, oggetto Error
- Windows Media Player Controllo ActiveX mobile,oggetto Error
- Windows Media Player Mobile, oggetto Error
- Oggetto errore
- Windows Media Player,Oggetto ErrorItem
- Windows Media Player a oggetti, oggetto ErrorItem
- modello a oggetti,oggetto ErrorItem
- Windows Media Player ActiveX, oggetto ErrorItem
- ActiveX, oggetto ErrorItem
- Windows Media Player Controllo ActiveX mobile, oggetto ErrorItem
- Windows Media Player Oggetto Mobile,ErrorItem
- Oggetto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84dcd8e0961007c185640b32ac53d249d2e739ca5e1aa4247a6735e09b2a3242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004401"
---
# <a name="about-the-error-and-erroritem-objects"></a>Informazioni sugli oggetti Error e ErrorItem

Gli **oggetti Error** e **ErrorItem** regolano le funzionalità di gestione degli errori di Windows Media Player. **L'oggetto Error** viene ottenuto dall'oggetto **Player** tramite la **proprietà error.** È possibile ottenere un codice specifico **dall'oggetto Error** usando la proprietà **item** dell'oggetto **Error** per creare **l'oggetto ErrorItem.** Ad esempio, per ottenere il codice di errore del primo elemento di errore, digitare:


```C++
myerrorcode = player.error.item(0).errorCode;

```



È anche possibile richiamare la Guida Web con **l'oggetto Error** usando il codice seguente:


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Modello a oggetti lettore per linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




