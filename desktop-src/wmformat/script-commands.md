---
title: Comandi script
description: Comandi script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media Format SDK, comandi script
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), comandi script
- Windows Media Format SDK, flussi di script
- Formati di sistema avanzati (ASF), flussi di script
- ASF (formato avanzato dei sistemi), flussi di script
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- script, comandi
- script, flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047566"
---
# <a name="script-commands"></a>Comandi script

I comandi script supportati da Windows Media Format SDK sono coppie di stringhe nome e valore semplici. Un comando script comune, ad esempio, è "URL", che viene utilizzato da Windows Media Player e da altre applicazioni di riproduzione per aprire le pagine Web. L'altra metà della coppia di script per il comando "URL" contiene un URL (Uniform Resource Locator) valido, ad esempio `https://www.adatum.com` . Nessun supporto fornito dagli oggetti di questo SDK per i comandi specifici. l'applicazione deve includere la logica per gestire qualsiasi comando utilizzato. È possibile utilizzare i comandi supportati da Windows Media Player per mantenere la compatibilità con la maggior parte dei giocatori.

I comandi di script possono essere recapitati in uno dei due modi seguenti: in un flusso di script o nell'intestazione del file.

## <a name="script-streams"></a>Flussi di script

È possibile recapitare i comandi script nel proprio flusso in un file ASF. Ogni esempio in un flusso di script contiene le due stringhe della coppia nome/valore. Il vantaggio dell'utilizzo di un flusso di script consiste nel fatto che i comandi verranno recapitati al momento della presentazione corretta.

## <a name="script-commands-in-the-file-header"></a>Script per comandi nell'intestazione del file

I comandi di script possono essere inclusi nell'intestazione del file per il recupero al momento della riproduzione. L'applicazione di riproduzione è responsabile dell'esecuzione dei comandi script al momento giusto. Il vantaggio di utilizzare i comandi script nell'intestazione del file è che tutti i comandi di script sono disponibili prima di iniziare a ricevere esempi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Uso di comandi script**](using-script-commands.md)
</dt> </dl>

 

 




