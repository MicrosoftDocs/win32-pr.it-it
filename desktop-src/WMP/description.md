---
title: Descrizione (Windows Media Player SDK)
description: Descrizione
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Mobile Skins, sezione Descrizione
- interfacce, sezione Descrizione
- riferimento per le interfacce, sezione Descrizione
- Sezione Descrizione in Skins
- file di definizione dell'interfaccia, sezione Descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400134"
---
# <a name="description-windows-media-player-sdk"></a>Descrizione (Windows Media Player SDK)

Quando si crea un'interfaccia per Windows Media Player 9 Series per Windows Mobile 2003 o versione successiva, è necessario includere una sezione Descrizione. La sezione Descrizione consente di specificare la larghezza e l'altezza dello schermo, la risoluzione dello schermo e l'orientamento di visualizzazione per cui è stata progettata l'interfaccia. La sezione Description deve essere visualizzata nel file di definizione dell'interfaccia prima di qualsiasi altra sezione e subito dopo la dichiarazione di versione iniziale.

La sezione Descrizione del file di definizione dell'interfaccia deve iniziare con la riga seguente:


```C++
[ Description ]

```



È quindi necessario aggiungere informazioni sulle dimensioni dell'interfaccia e la risoluzione dello schermo. Nell'esempio seguente viene illustrato come specificare le dimensioni:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



In questo modo si specifica che l'interfaccia è stata progettata per essere visualizzata 240 pixel di larghezza, 320 pixel di altezza e con la risoluzione dello schermo 96 DPI. Si noti che questo implica un orientamento in modalità verticale.

Facoltativamente, è possibile specificare la modalità di orientamento per la quale è stata progettata l'interfaccia nella sezione Descrizione. Nell'esempio seguente viene illustrato come specificare l'orientamento:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



Nella tabella seguente sono elencati i valori che è possibile utilizzare per l'orientamento.



| Orientamento | Descrizione                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Orizzontale   | La larghezza dell'interfaccia è maggiore dell'altezza dell'interfaccia. La visualizzazione è orientata in modo orizzontale.   |
| Verticale    | L'altezza dell'interfaccia è maggiore della larghezza dell'interfaccia. La visualizzazione è orientata in modo verticale. |
| Square      | L'altezza dell'interfaccia è uguale alla larghezza dell'interfaccia. La visualizzazione non ha un orientamento.                    |



 

> [!Note]  
> Windows Media Player 9 Series per Windows Mobile 2003 visualizzerà solo una particolare interfaccia quando la sezione Descrizione specificata nel file di definizione dell'interfaccia personalizzata corrisponde allo stato corrente del dispositivo.

 

È necessario prestare attenzione a specificare sempre le dimensioni, la risoluzione e l'orientamento corrette per le quali è stata creata l'interfaccia. Se, ad esempio, le dimensioni specificate dall'interfaccia descrivono un orientamento orizzontale, l'interfaccia non sarà disponibile quando il dispositivo è in modalità verticale, anche se si specifica verticale nella linea di orientamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




