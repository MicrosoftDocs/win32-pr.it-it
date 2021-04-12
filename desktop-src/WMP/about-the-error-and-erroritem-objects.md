---
title: Informazioni sugli oggetti Error e ErrorItem
description: Informazioni sugli oggetti Error e ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player, oggetto Error
- Modello a oggetti di Windows Media Player, oggetto Error
- modello a oggetti, oggetto Error
- Controllo ActiveX Windows Media Player, oggetto Error
- Controllo ActiveX, oggetto Error
- Controllo ActiveX Windows Media Player Mobile, oggetto Error
- Windows Media Player Mobile, oggetto Error
- Oggetto errore
- Windows Media Player, oggetto ErrorItem
- Modello a oggetti di Windows Media Player, oggetto ErrorItem
- modello a oggetti, oggetto ErrorItem
- Controllo ActiveX Windows Media Player, oggetto ErrorItem
- Controllo ActiveX, oggetto ErrorItem
- Controllo ActiveX Windows Media Player Mobile, oggetto ErrorItem
- Windows Media Player Mobile, oggetto ErrorItem
- Oggetto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330439"
---
# <a name="about-the-error-and-erroritem-objects"></a>Informazioni sugli oggetti Error e ErrorItem

Gli oggetti **Error** e **ErrorItem** regolano le funzionalità di gestione degli errori di Windows Media Player. L'oggetto **Error** viene ottenuto dall'oggetto **Player** tramite la proprietà **Error** . È possibile ottenere un codice specifico dall'oggetto **Error** usando la proprietà **Item** dell'oggetto **Error** per creare l'oggetto **ErrorItem** . Per ottenere, ad esempio, il codice di errore del primo elemento Error, digitare:


```C++
myerrorcode = player.error.item(0).errorCode;

```



È anche possibile richiamare la guida Web con l'oggetto **Error** usando il codice seguente:


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetto Error**](error-object.md)
</dt> <dt>

[**Oggetto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




