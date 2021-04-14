---
title: Aggiunta di BUTTONGROUP
description: Aggiunta di BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- creazione di interfacce, elemento BUTTONGROUP
- Windows Media Player Skin, elemento BUTTONGROUP
- interfacce, elemento BUTTONGROUP
- file di definizione dell'interfaccia, elemento BUTTONGROUP
- Elemento BUTTONGROUP
- elementi, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329079"
---
# <a name="adding-buttongroup"></a>Aggiunta di BUTTONGROUP

Questo esempio usa l'elemento **ButtonGroup** per il codice nel file di definizione dell'interfaccia personalizzata. **ButtonGroup** crea un modo semplice per elaborare gli eventi del mouse senza dover calcolare le posizioni esatte sullo schermo e usa il colore anziché le coordinate x e y.

Per prima cosa, è necessario aggiungere i tag **ButtonGroup** al file di definizione dell'interfaccia creata. Inserirli dopo gli attributi del tag del **tema** .


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Lasciare alcune righe vuote sopra il tag di chiusura **ButtonGroup** per i pulsanti che verrà aggiunto successivamente.

Gli attributi seguenti vengono usati per definire **ButtonGroup**:

**mappingImage**

Si tratta del nome file del file di grafica di mapping creato in precedenza, quello con i cerchi rossi e verdi. Questo attributo è obbligatorio per qualsiasi **ButtonGroup**.

**hoverImage**

Si tratta del nome file del file di immagine del passaggio del mouse creato in precedenza, quello con i due pulsanti gialli che leggono "Play" e "close". Questa operazione non è obbligatoria, ma un'immagine del passaggio del mouse consente di fornire commenti e suggerimenti all'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




