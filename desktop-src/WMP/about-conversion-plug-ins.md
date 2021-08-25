---
title: Informazioni sui plug-in di conversione
description: Informazioni sui plug-in di conversione
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player,plug-in di conversione
- Windows Media Player plug-in, conversione
- plug-in, conversione
- plug-in di conversione, informazioni
- Advanced Systems Format (ASF)
- ASF (Advanced Systems Format)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4331f2cc0cdf8726e2ba26e834c56546ee614e012a9dd6acdad56906d450b66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903551"
---
# <a name="about-conversion-plug-ins"></a>Informazioni sui plug-in di conversione

È possibile creare un plug-in Windows Media Player per convertire i file multimediali digitali creati usando tecnologie non fornite da Microsoft in Advanced Systems Format (ASF).

I plug-in di conversione Component Object Model oggetti (COM) che vengono in pacchetto e distribuiti come file eseguibili (.exe). Windows Media Player crea un'istanza dei plug-in di conversione per convertire formati multimediali digitali di terze parti negli scenari seguenti:

-   Il contenuto multimediale digitale viene copiato nel computer da un dispositivo portatile.
-   Il contenuto multimediale digitale viene aggiunto alla libreria **usando IWMPMediaCollection::add.**
-   Il contenuto multimediale digitale viene aggiunto alla raccolta usando la funzionalità di ricerca di Windows Media Player.
-   Il contenuto multimediale digitale viene aggiunto alla raccolta dalla funzionalità di monitoraggio delle cartelle di Windows Media Player.
-   Il contenuto multimediale digitale viene aggiunto all'elenco di sincronizzazione quando l'utente trascina e rilascia un file.

Dopo Windows Media Player crea un'istanza di un plug-in di conversione, il plug-in deve convertire il file fornito in ASF o WMA e aggiungere i metadati pertinenti. Non usare il plug-in di conversione per transcodificare il file. Il plug-in deve quindi copiare il file convertito nella cartella specificata e restituire il percorso del nuovo file Windows Media Player.

I plug-in di conversione devono implementare **l'interfaccia IWMPConvert.** Vedere [Guida di riferimento alla programmazione dei plug-in di conversione.](conversion-plug-ins-programming-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul processo di conversione**](about-the-conversion-process.md)
</dt> <dt>

[**Aggiunta di metadati ai file convertiti**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Windows Media Player Plug-in di conversione**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




