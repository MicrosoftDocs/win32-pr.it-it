---
title: Uso di comandi script
description: Uso di comandi script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows Media Format SDK, comandi script
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), comandi script
- script, comandi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044797"
---
# <a name="using-script-commands"></a>Uso di comandi script

Windows Media Format SDK supporta l'uso di comandi script per comunicare le azioni dell'applicazione nei file ASF. Ogni comando di script è costituito da due stringhe, la prima stringa è il tipo di comando, il secondo è costituito dai dati del comando. Ad esempio, è possibile usare il tipo di script "URL" e passare un URL Internet valido come dati del comando. Quando un'applicazione di lettura che supporta i comandi script di tipo "URL" riceve questo comando, l'indirizzo specificato verrà aperto in una finestra del browser.

Windows Media Format SDK fornisce due opzioni per la distribuzione di script nei file ASF. È possibile creare un flusso di script oppure è possibile includere i comandi di script nell'intestazione del file. I flussi di script sono utili perché i comandi di script vengono recapitati nell'ordine temporale della presentazione. Se si usano i comandi script nell'intestazione del file, l'applicazione dovrà recuperare tutti i comandi di script prima di avviare la riproduzione. È necessario tenere traccia dei tempi di presentazione dei comandi script e rispondere al momento giusto.

Nelle sezioni seguenti viene descritto come includere comandi script in un file ASF.



| Sezione                                                                                                                | Descrizione                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Per usare un flusso di script](to-use-a-script-stream.md)                                                                   | Viene descritto come includere comandi script in un flusso di script. |
| [Per aggiungere dati di script all'intestazione](to-add-script-data-to-the-header.md)                                               | Viene descritto come includere i comandi script nell'intestazione del file. |
| [Uso di comandi script supportati da Windows Media Player](using-script-commands-supported-by-windows-media-player.md) | Descrive i comandi script usati da Windows Media Player.  |



 

> [!Note]  
> Nelle versioni precedenti di Windows Media Format SDK, i flussi di script venivano usati per aprire indirizzi Web corrispondenti al contenuto di un file ASF. È ora possibile usare i flussi Web per lavorare con le pagine Web sincronizzate. Per altre informazioni. vedere [flussi Web](web-streams.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Comandi script**](script-commands.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




