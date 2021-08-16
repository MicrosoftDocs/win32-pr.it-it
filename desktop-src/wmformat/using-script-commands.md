---
title: Uso di comandi script
description: Uso di comandi script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows MEDIA Format SDK,comandi script
- Advanced Systems Format (ASF), comandi script
- ASF (Advanced Systems Format), comandi script
- script,comandi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b77de3e892d4f7b479822442a2637849df3d4bcd56273deb952246fba14f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195787"
---
# <a name="using-script-commands"></a>Uso di comandi script

L Windows Media Format SDK supporta l'uso di comandi script per comunicare le azioni dell'applicazione nei file ASF. Ogni comando script è costituito da due stringhe, la prima stringa è il tipo di comando, la seconda è i dati del comando. Ad esempio, è possibile usare il tipo di script "URL" e passare un URL Internet valido come dati del comando. Quando un'applicazione di lettura che supporta comandi script di tipo "URL" riceve questo comando, aprirà l'indirizzo specificato in una finestra del browser.

L Windows Media Format SDK offre due opzioni per la distribuzione di script nei file ASF. È possibile creare un flusso di script oppure includere comandi script nell'intestazione del file. I flussi di script sono utili perché i comandi script vengono recapitati in ordine di tempo di presentazione. Se si usano comandi script nell'intestazione del file, l'applicazione dovrà recuperare tutti i comandi script prima di avviare la riproduzione. È necessario tenere traccia dei tempi di presentazione dei comandi script e rispondere al momento giusto.

Le sezioni seguenti descrivono come includere comandi script in un file ASF.



| Sezione                                                                                                                | Descrizione                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Per usare un flusso di script](to-use-a-script-stream.md)                                                                   | Viene descritto come includere comandi script in un flusso di script. |
| [Per aggiungere dati script all'intestazione](to-add-script-data-to-the-header.md)                                               | Viene descritto come includere comandi script nell'intestazione del file. |
| [Uso di comandi script supportati da Windows Media Player](using-script-commands-supported-by-windows-media-player.md) | Descrive i comandi script usati da Windows Media Player.  |



 

> [!Note]  
> Nelle versioni precedenti di Windows Media Format SDK, i flussi di script venivano usati per aprire indirizzi Web corrispondenti al contenuto di un file ASF. È ora possibile usare i flussi Web per usare le pagine Web sincronizzate. Per altre informazioni. vedere [Web Flussi](web-streams.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Comandi script**](script-commands.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




