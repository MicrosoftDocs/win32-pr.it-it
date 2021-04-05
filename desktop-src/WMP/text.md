---
title: Testo (Windows Media Player SDK)
description: Testo
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Windows Media Player Mobile Skins, testo
- interfacce, testo
- riferimento per interfacce, testo
- testo nelle interfacce, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873241"
---
# <a name="text-windows-media-player-sdk"></a>Testo (Windows Media Player SDK)

Si consiglia di usare una o più caselle di testo visualizzate nell'interfaccia personalizzata. Ogni casella di visualizzazione di testo usata deve essere definita nel file di definizione dell'interfaccia utente. Se non si definisce una casella di visualizzazione di testo in questa sezione, l'interfaccia non sarà in grado di utilizzarla.

La sezione di testo del file di definizione dell'interfaccia personalizzata inizia con questa riga:


```C++
[ Text ]

```



È quindi necessario aggiungere una o più righe contenenti informazioni su ognuna delle caselle di testo visualizzate nell'interfaccia


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



È possibile usare il modello seguente per la sezione di testo del file di definizione dell'interfaccia personalizzata:


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



È necessario utilizzare l'ordine illustrato nel modello precedente per informazioni sulla casella di visualizzazione del testo per ogni riga della sezione di testo. Ogni parte della riga è obbligatoria. Le sezioni seguenti descrivono ogni elemento in dettaglio.

1.  [Tipo di testo](text-type.md)
2.  [Posizione del testo](text-location.md)
3.  [Allineamento del testo](text-alignment.md)
4.  [Carattere testo](text-font.md)
5.  [Colore del testo](text-color.md)

Per un esempio di codice di testo, vedere la [sezione di testo di esempio](sample-text-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




