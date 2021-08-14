---
title: Comandi script
description: Comandi script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows MEDIA Format SDK,comandi script
- Advanced Systems Format (ASF), comandi script
- ASF (Advanced Systems Format), comandi script
- Windows MEDIA Format SDK, flussi di script
- Advanced Systems Format (ASF), flussi di script
- ASF (Advanced Systems Format), flussi di script
- Windows MEDIA Format SDK, flussi
- Advanced Systems Format (ASF), streams
- ASF (Advanced Systems Format), flussi
- script,comandi
- script, flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6f6487958db820892f57af2b1348dcd4304031976aaaf56ddeb6233e1b8a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197529"
---
# <a name="script-commands"></a>Comandi script

I comandi script supportati da Windows Media Format SDK sono coppie di stringhe di nome e valore semplici. Ad esempio, un comando script comune è "URL", che viene usato da Windows Media Player e altre applicazioni in riproduzione per aprire pagine Web. L'altra metà della coppia di script per il comando "URL" contiene un URL (Uniform Resource Locator) valido, ad esempio `https://www.adatum.com` . Gli oggetti di questo SDK non supportano alcun comando specifico. L'applicazione deve includere la logica per gestire i comandi in uso. È possibile usare i comandi supportati da Windows Media Player per mantenere la compatibilità con la maggior parte dei lettori.

I comandi script possono essere recapitati in uno dei due modi seguenti: in un flusso di script o nell'intestazione del file.

## <a name="script-streams"></a>Script Flussi

È possibile distribuire comandi script nel proprio flusso in un file ASF. Ogni esempio in un flusso di script contiene le due stringhe della coppia nome/valore. Il vantaggio dell'uso di un flusso di script è che i comandi verranno recapitati al momento della presentazione corretta.

## <a name="script-commands-in-the-file-header"></a>Comandi script nell'intestazione del file

I comandi script possono essere inclusi nell'intestazione del file per il recupero al momento della riproduzione. L'applicazione in riproduzione è responsabile dell'esecuzione dei comandi script nel momento appropriato. Il vantaggio dell'uso di comandi script nell'intestazione del file è che tutti i comandi script sono disponibili prima di iniziare a ricevere gli esempi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Uso di comandi script**](using-script-commands.md)
</dt> </dl>

 

 




