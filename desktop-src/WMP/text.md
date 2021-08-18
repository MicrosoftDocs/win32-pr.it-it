---
title: Testo (Windows Media Player SDK)
description: Testo
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Skin per dispositivi mobili, testo
- skins,text
- informazioni di riferimento per le skin, testo
- testo nelle skin, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55027415222516e72df61afab01a14cceb503528467bf329264014c94bf31ed7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118099"
---
# <a name="text-windows-media-player-sdk"></a>Testo (Windows Media Player SDK)

È possibile usare una o più caselle di visualizzazione del testo nell'interfaccia. Ogni casella di visualizzazione del testo utilizzata deve essere definita nel file di definizione dell'interfaccia. Se non si definisce una casella di visualizzazione del testo in questa sezione, l'interfaccia non sarà in grado di usarla.

La sezione Text del file di definizione dell'interfaccia inizia con questa riga:


```C++
[ Text ]

```



È quindi necessario aggiungere una o più righe contenenti informazioni su ognuna delle caselle di visualizzazione del testo nell'interfaccia


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



È possibile usare il modello seguente per la sezione Text del file di definizione dell'interfaccia:


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



È necessario usare l'ordine indicato nel modello precedente per le informazioni sulla casella di visualizzazione del testo per ogni riga nella sezione Testo. Ogni parte della riga è obbligatoria. Le sezioni seguenti descrivono ogni elemento in dettaglio.

1.  [Tipo di testo](text-type.md)
2.  [Posizione del testo](text-location.md)
3.  [Allineamento del testo](text-alignment.md)
4.  [Tipo di carattere del testo](text-font.md)
5.  [Colore del testo](text-color.md)

Per un esempio di codice di testo, vedere [Sezione Testo di esempio](sample-text-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento su Skin**](skin-reference.md)
</dt> </dl>

 

 




