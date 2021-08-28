---
title: Descrizione (WINDOWS MEDIA PLAYER SDK)
description: Descrizione
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Windows Media Player Interfaccia per dispositivi mobili, sezione Description
- skins, sezione Description
- informazioni di riferimento per le interfaccia, sezione Description
- Sezione Description nelle interfaccia
- file di definizione dell'interfaccia utente, sezione Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ca5235939352ffabb924aaf38a706b436d4c1358a92b9aef4996614c53623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749958"
---
# <a name="description-windows-media-player-sdk"></a>Descrizione (WINDOWS MEDIA PLAYER SDK)

Quando si crea un'interfaccia per Windows Media Player serie 9 per Windows Mobile 2003 o versione successiva, è necessario includere una sezione Description. La sezione Description (Descrizione) consente di specificare la larghezza e l'altezza dello schermo, la risoluzione dello schermo e l'orientamento dello schermo per cui è stata progettata l'interfaccia. La sezione Description deve essere visualizzata nel file di definizione dell'interfaccia prima di qualsiasi altra sezione e subito dopo la dichiarazione della versione iniziale.

La sezione Description del file di definizione dell'interfaccia deve iniziare con la riga seguente:


```C++
[ Description ]

```



È quindi necessario aggiungere informazioni sulle dimensioni dell'interfaccia e sulla risoluzione dello schermo. Nell'esempio seguente viene illustrato come specificare le dimensioni:


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



Specifica che l'interfaccia è stata progettata per la visualizzazione di 240 pixel di larghezza, 320 pixel di altezza e con risoluzione dello schermo di 96 DPI. Si noti che ciò implica un orientamento in modalità verticale.

Facoltativamente, è possibile specificare la modalità di orientamento per cui è stata progettata l'interfaccia nella sezione della descrizione. L'esempio seguente illustra come specificare l'orientamento:


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



Nella tabella seguente sono elencati i valori che è possibile usare per Orientation.



| Orientamento | Descrizione                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| Orizzontale   | La larghezza dell'interfaccia è maggiore dell'altezza dell'interfaccia. La visualizzazione è orientata in modo orizzontale.   |
| Verticale    | L'altezza dell'interfaccia è maggiore della larghezza dell'interfaccia. La visualizzazione è orientata in senso verticale. |
| Square      | L'altezza dell'interfaccia è uguale alla larghezza dell'interfaccia. La visualizzazione non ha orientamento.                    |



 

> [!Note]  
> Windows Media Player serie 9 per Windows Mobile 2003 visualizza una particolare interfaccia solo quando la sezione description specificata nel file di definizione dell'interfaccia corrisponde allo stato corrente del dispositivo.

 

È necessario prestare attenzione a specificare sempre le dimensioni, la risoluzione e l'orientamento corretti per cui è stata creato l'interfaccia. Ad esempio, se le dimensioni specificate dall'interfaccia descrivono un orientamento orizzontale, l'interfaccia non sarà disponibile quando il dispositivo è in modalità verticale, anche se si specifica Verticale nella linea di orientamento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento per l'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




