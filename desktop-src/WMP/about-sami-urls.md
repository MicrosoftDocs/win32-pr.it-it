---
title: Informazioni sugli URL SAMI
description: Informazioni sugli URL SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player a oggetti, Synchronized Accessible Media Interchange (SAMI)
- modello a oggetti,Interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Controllo ActiveX mobile,Interscambio multimediale accessibile sincronizzato (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Synchronized Accessible Media Interchange (SAMI), files
- SAMI (Synchronized Accessible Media Interchange),files
- Synchronized Accessible Media Interchange (SAMI), URL
- SAMI (Synchronized Accessible Media Interchange), URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a35976c6988ad4298c812005002da010730d5254bd7c010f24fe32741be393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956801"
---
# <a name="about-sami-urls"></a>Informazioni sugli URL SAMI

I file SAMI possono essere associati ai file multimediali digitali usando un singolo URL. Questa operazione viene eseguita usando il *parametro url sami.* Il parametro URL è preceduto dall'URL di base e da ? . Un URL con un *parametro sami* segue questa sintassi:

*URL*? *sami* = *captionsURL*.

Il valore del parametro URL segue il nome del parametro e un segno di uguale, come nell'esempio seguente:


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



Questa sintassi dell'URL viene comunemente usata in un collegamento ipertestuale o in un metafile di Windows Media per collegarsi direttamente ai percorsi del file multimediale digitale e del file SAMI. Quando l'utente fa clic sul collegamento ipertestuale, Windows Media Player viene avviato in modalità completa e riproduce il contenuto multimediale digitale.

Se il parametro url *sami* non viene specificato, Windows Media Player cerca un file SAMI che si trova nello stesso percorso del file multimediale digitale e che ha lo stesso nome file, ad eccezione dell'estensione del nome file, che deve essere smi. Se tale file è presente, verrà aperto automaticamente se la visualizzazione dei sottotitoli è stata abilitata nel lettore.

I sottotitoli codificati vengono abilitati Windows Media Player clic sul menu **Riproduci,** quindi su Sottotitoli e infine su **Su**. Se i sottotitoli codificati sono abilitati, i sottotitoli contenuti nel file SAMI verranno visualizzati durante la riproduzione dell'elemento multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




