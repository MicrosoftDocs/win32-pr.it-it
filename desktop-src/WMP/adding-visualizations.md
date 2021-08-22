---
title: Aggiunta di visualizzazioni
description: Aggiunta di visualizzazioni
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- creazione di interfaccia, visualizzazioni
- Windows Media Player, visualizzazioni
- interfaccia, visualizzazioni
- visualizzazioni, interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d236990d3e29cf4e51dbb46e8e1269b0c8a50ccaf205940a6f34b97c89fa6e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619151"
---
# <a name="adding-visualizations"></a>Aggiunta di visualizzazioni

È possibile aggiungere una finestra di visualizzazione nello stesso modo in cui è stata aggiunta una finestra video. È possibile usare la stessa interfaccia, ma viene usato un **elemento EFFECTS.**

Prima di tutto è necessario aggiungere **l'elemento EFFECTS** e assegnargli un ID e una dimensione:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



È quindi possibile assegnare ai due pulsanti una stringa di codice di visualizzazione precedente e successiva:


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

Infine, è stato **aggiunto un** semplice elemento PLAYER con **l'attributo URL** per scegliere un brano da riprodurre.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



È possibile visualizzare un'interfaccia di visualizzazione funzionante simile nella sezione di esempio dell'SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla creazione dell'interfaccia**](skin-creation-guide.md)
</dt> </dl>

 

 




