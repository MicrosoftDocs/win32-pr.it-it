---
title: Informazioni sugli URL SAMI
description: Informazioni sugli URL SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- SAMI (Synchronized Accessible Media Interchange), file
- SAMI (interscambio multimediale accessibile sincronizzato), file
- SAMI (Synchronized Accessible Media Interchange), URL
- SAMI (interscambio multimediale accessibile sincronizzato), URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221246"
---
# <a name="about-sami-urls"></a>Informazioni sugli URL SAMI

I file SAMI possono essere associati a file multimediali digitali usando un singolo URL. Questa operazione viene eseguita tramite *il parametro dell'URL Sami* . Il parametro URL è preceduto dall'URL di base e da un? . Un URL con un parametro *Sami* segue questa sintassi:

*URL*? *Sami* = *captionsURL*.

Il valore del parametro URL segue il nome del parametro e un segno di uguale, come nell'esempio seguente:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Questa sintassi dell'URL viene comunemente utilizzata in un collegamento ipertestuale o in un metafile di Windows Media per collegarsi direttamente ai percorsi del file multimediale digitale e del file SAMI. Quando l'utente fa clic sul collegamento ipertestuale, Windows Media Player viene avviato in modalità completa e riproduce il contenuto multimediale digitale.

Se il parametro dell'URL *Sami* non è specificato, Windows Media Player cerca un file Sami che si trova nella stessa posizione del file multimediale digitale e che ha lo stesso nome di file, ad eccezione dell'estensione del nome file, che deve essere. SMI. Se è presente un file di questo tipo, questo verrà aperto automaticamente se nel lettore è stata abilitata la visualizzazione della didascalia.

Le didascalie chiuse sono abilitate in Windows Media Player facendo clic sul menu **Riproduci** , quindi facendo clic su **didascalie e sottotitoli** e quindi **su on**. Se le didascalie chiuse sono abilitate, le didascalie contenute nel file SAMI verranno visualizzate durante la riproduzione dell'elemento multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




