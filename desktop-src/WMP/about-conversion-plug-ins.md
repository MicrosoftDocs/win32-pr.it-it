---
title: Informazioni sui plug-in di conversione
description: Informazioni sui plug-in di conversione
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, plug-in di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, informazioni
- Advanced Systems Format (ASF)
- ASF (formato avanzato dei sistemi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708053"
---
# <a name="about-conversion-plug-ins"></a>Informazioni sui plug-in di conversione

È possibile creare un plug-in di Windows Media Player per convertire i file multimediali digitali creati usando le tecnologie non fornite da Microsoft, nel formato ASF (Advanced Systems Format).

I plug-in di conversione sono oggetti Component Object Model (COM) che vengono inseriti in un pacchetto e distribuiti come file eseguibili (exe). Windows Media Player crea un'istanza dei plug-in di conversione per convertire i formati multimediali digitali di terze parti negli scenari seguenti:

-   Il contenuto multimediale digitale viene copiato nel computer da un dispositivo portatile.
-   Il contenuto multimediale digitale viene aggiunto alla libreria usando **IWMPMediaCollection:: Add**.
-   Il contenuto multimediale digitale viene aggiunto alla libreria usando la funzionalità di ricerca di Windows Media Player.
-   Il contenuto multimediale digitale viene aggiunto alla libreria dalla funzionalità di monitoraggio delle cartelle di Windows Media Player.
-   Il contenuto multimediale digitale viene aggiunto all'elenco di sincronizzazione quando l'utente trascina un file e lo rilascia.

Dopo che Windows Media Player crea un'istanza di un plug-in di conversione, il plug-in deve convertire il file fornito in ASF o WMA e aggiungere i relativi metadati. Non usare il plug-in di conversione per la transcodifica del file. Il plug-in deve quindi copiare il file convertito nella cartella specificata e restituire il percorso del nuovo file a Windows Media Player.

I plug-in di conversione devono implementare l'interfaccia **IWMPConvert** . Vedere informazioni [di riferimento sulla programmazione di plug-in di conversione](conversion-plug-ins-programming-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul processo di conversione**](about-the-conversion-process.md)
</dt> <dt>

[**Aggiunta di metadati ai file convertiti**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Plug-in di conversione di Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




