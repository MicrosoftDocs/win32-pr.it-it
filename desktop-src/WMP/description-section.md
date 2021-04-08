---
title: Sezione Descrizione
description: Sezione Descrizione
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player Mobile Skins, sezione Descrizione
- interfacce, sezione Descrizione
- creazione di interfacce, sezione Descrizione
- scrittura del codice per le interfacce, sezione Descrizione
- Sezione Descrizione in Skins
- file di definizione dell'interfaccia, sezione Descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856797"
---
# <a name="description-section"></a>Sezione Descrizione

Successivamente, è necessario fornire una sezione che descriva le dimensioni e l'orientamento dell'interfaccia durante la creazione di un'interfaccia per Windows Media Player 9 Series per Windows Mobile 2003 e versioni successive:


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



La sezione Descrizione deve iniziare con la parola Descrizione tra parentesi quadre, quindi includere una riga che specifichi le dimensioni e la risoluzione dello schermo per l'interfaccia.

Le righe che iniziano con due barre non vengono elaborate e possono essere usate per i commenti o, come illustrato nel codice precedente, un modello che consente di ricordare cosa accade in una sezione. È anche possibile usare i modelli per allineare tutti gli elementi alle colonne.

Per ulteriori informazioni sulla sezione Descrizione, vedere [Description](description.md) in the Skin Reference.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura del codice**](writing-the-code.md)
</dt> </dl>

 

 




