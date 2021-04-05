---
title: Aggiunta di visualizzazioni
description: Aggiunta di visualizzazioni
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- creazione di interfacce, visualizzazioni
- Interfacce di Media Player Windows, visualizzazioni
- interfacce, visualizzazioni
- Visualizzazioni, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710786"
---
# <a name="adding-visualizations"></a>Aggiunta di visualizzazioni

È possibile aggiungere una finestra di visualizzazione nello stesso modo in cui è stata aggiunta una finestra video. È possibile utilizzare la stessa interfaccia, ma viene utilizzato un elemento **Effects** .

Prima di tutto è necessario aggiungere l'elemento **Effects** e assegnargli un ID e una dimensione:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



È quindi possibile assegnare i due pulsanti a una stringa di codice di visualizzazione precedente e successiva:


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



I livelli e le bitmap sono gli stessi usati nell'esempio video, ad eccezione del fatto che la freccia di riproduzione è stata copiata e capovolta orizzontalmente.

Infine, è stato aggiunto un semplice elemento **Player** con l'attributo **URL** per scegliere un brano da riprodurre.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



Nella sezione di esempio dell'SDK è possibile visualizzare un'interfaccia di visualizzazione di lavoro simile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




