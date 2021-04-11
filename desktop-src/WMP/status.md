---
title: Stato (Windows Media Player SDK)
description: Stato
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Interfacce di Windows Media Player Mobile, visualizzazione dello stato
- interfacce, visualizzazione stato
- informazioni di riferimento per Skins, status display
- visualizzazione dello stato in interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047685"
---
# <a name="status-windows-media-player-sdk"></a>Stato (Windows Media Player SDK)

Si consiglia di usare una visualizzazione dello stato nell'interfaccia personalizzata. In tal caso, l'elemento status deve essere definito nel file di definizione dell'interfaccia personalizzata. In alternativa, è possibile visualizzare queste informazioni anche usando l'attributo status nell'elemento di testo.

La sezione stato del file di definizione dell'interfaccia personalizzata inizia con questa riga:


```C++
[ Status ]

```



È quindi necessario aggiungere una o più righe che contengono informazioni sulla visualizzazione dello stato nell'interfaccia.


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



È possibile usare il modello seguente per la sezione stato del file di definizione dell'interfaccia utente:


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



È necessario usare l'ordine illustrato nel modello precedente per informazioni sullo stato di visualizzazione per ogni riga nella sezione stato. Ogni parte della riga è obbligatoria. Le sezioni seguenti descrivono ogni elemento:

-   [Stato](status-item.md)
-   [Percorso stato](status-location.md)
-   [Allineamento stato](status-alignment.md)
-   [Carattere stato](status-font.md)
-   [Colore di stato](status-color.md)

Per un esempio di codice di stato, vedere la [sezione Sample status](sample-status-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




