---
title: Testo scorrevole
description: Testo scorrevole
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- riferimento per Skin, Marquees
- Marquees in Skin, about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396447"
---
# <a name="marquee"></a>Testo scorrevole

Un Marquee è una casella di visualizzazione di testo a scorrimento che visualizza informazioni da una o più caselle di visualizzazione di testo. Non è necessario aggiungere un Marquee, ma può essere molto utile quando si dispone di informazioni dettagliate che si desidera visualizzare all'utente in uno spazio limitato.

Il testo nella casella di selezione verrà spostato solo se vengono soddisfatte entrambe le condizioni seguenti:

-   Il testo visualizzato nella casella di selezione è maggiore della larghezza della casella di visualizzazione Marquee.
-   L'elemento multimediale viene arrestato o sospeso.

La sezione Marquee del file di definizione dell'interfaccia deve iniziare con questa riga:


```C++
[ Marquee ]

```



> [!Note]  
> Per mantenere la compatibilità con le versioni di Windows Media Player Mobile precedenti a Windows Media Player 10 Mobile, l'utilizzo di "Marquis" in un file di definizione dell'interfaccia personalizzata è ancora considerato valido.

 

È quindi necessario aggiungere una o più righe contenenti informazioni su ciascuna casella di visualizzazione Marquee nell'interfaccia.


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



È possibile usare il modello seguente per la sezione Marquee del file di definizione dell'interfaccia utente:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



È necessario utilizzare l'ordine seguente per informazioni in ogni riga della sezione Marquee (è necessaria ogni parte della riga):

1.  [Posizione Marquee](marquee-location.md)
2.  [Carattere Marquee](marquee-font.md)
3.  [Colore Marquee](marquee-color.md)
4.  [Combinazioni di testo](text-combinations.md)

Per un esempio di codice Marquee, vedere la [sezione Sample Marquee](sample-marquee-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




