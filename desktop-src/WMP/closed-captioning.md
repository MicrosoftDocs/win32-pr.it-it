---
title: Didascalie chiuse
description: Didascalie chiuse
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- Media Player di Windows, migrazione di didascalie chiuse
- Modello a oggetti di Windows Media Player, sottotitoli Smigrating
- modello a oggetti, migrazione di didascalie chiuse
- Windows Media Player Mobile, migrazione di didascalie chiuse
- Controllo ActiveX di Windows Media Player, migrazione di didascalie chiuse
- Controllo ActiveX di Windows Media Player Mobile, migrazione di didascalie chiuse
- Controllo ActiveX, migrazione di didascalie chiuse
- SAMI (Synchronized Accessible Media Interchange), migrazione di didascalie chiuse
- SAMI (interscambio multimediale accessibile sincronizzato), migrazione di didascalie chiuse
- Guida alla migrazione, l'interscambio multimediale accessibile sincronizzato (SAMI)
- Guida alla migrazione, sottotitoli codificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117415"
---
# <a name="closed-captioning"></a>Didascalie chiuse

Il controllo ActiveX di Windows Media Player 6,4 include un pannello di visualizzazione didascalia chiuso integrato che, quando reso visibile, Abilita i sottotitoli codificati accessibili da Media Interchange (SAMI) sincronizzati e visualizza il testo del titolo chiuso. Il controllo Windows Media Player 7 o versioni successive Abilita la visualizzazione della didascalia chiusa di SAMI usando un **<DIV>** elemento HTML. Ad esempio:


```C++
<DIV  ID = "CCDiv"></DIV>

```



Questa tecnica offre una flessibilità completa, dal momento che è possibile progettare la pagina Web per visualizzare le didascalie chiuse in modo personalizzato; non è più necessario che la visualizzazione didascalia chiusa si trovi in una posizione fissa adiacente all'interfaccia utente di Windows Media Player.

Dopo aver creato un'area per la visualizzazione di didascalie chiuse, usare *ClosedCaption*. proprietà **captioningID** per specificare il percorso in cui Windows Media Player esegue il rendering del testo della didascalia chiusa.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



Windows Media Player Software Development Kit (SDK) contiene un esempio funzionante di un lettore incorporato che Visualizza il testo del titolo chiuso. Per ottenere gli esempi di SDK, scaricare e installare l'SDK completo di Windows Media Player dal sito Web Microsoft. Per ulteriori informazioni sui sottotitoli codificati e SAMI, vedere il [sito Web di accessibilità Microsoft](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Oggetto ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Guida alla migrazione del modello a oggetti**](object-model-migration-guide.md)
</dt> </dl>

 

 




