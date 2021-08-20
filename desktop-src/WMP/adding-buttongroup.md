---
title: Aggiunta di BUTTONGROUP
description: Aggiunta di BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- creazione di interfaccia, elemento BUTTONGROUP
- Windows Media Player, elemento BUTTONGROUP
- skins,BUTTONGROUP - elemento
- file di definizione dell'interfaccia utente,elemento BUTTONGROUP
- BUTTONGROUP - elemento
- elementi, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6719bb3974b254f8d9446d45fd6d34385dbfcada4084c7bdd5c3a4e03bb06dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865190"
---
# <a name="adding-buttongroup"></a>Aggiunta di BUTTONGROUP

In questo esempio viene utilizzato **l'elemento BUTTONGROUP** per la codifica nel file di definizione dell'interfaccia. **BUTTONGROUP** crea un modo semplice per elaborare gli eventi del mouse senza dover calcolare le posizioni esatte sullo schermo e usa il colore anziché le coordinate x e y.

Prima di tutto è necessario aggiungere **i tag BUTTONGROUP** al file di definizione dell'interfaccia creato. Inserire i tag dopo gli attributi del tag **THEME.**


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



Lasciare alcune righe vuote sopra il tag **BUTTONGROUP di** chiusura per i pulsanti che verranno aggiunti successivamente.

Per definire BUTTONGROUP vengono usati **gli attributi seguenti:**

**mappingImage**

Si tratta del nome file del file di grafica di mapping creato in precedenza, quello con i cerchi rosso e verde. Questo attributo è obbligatorio per **qualsiasi BUTTONGROUP.**

**hoverImage**

Questo è il nome del file di grafica al passaggio del mouse creato in precedenza, quello con i due pulsanti gialli "Riproduci" e "Chiudi". Questa operazione non è necessaria, ma un'immagine al passaggio del mouse consente di inviare commenti e suggerimenti all'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del file di definizione dell'interfaccia**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




