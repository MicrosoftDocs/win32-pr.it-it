---
title: Creazione di Windows pacchetto di download multimediale (deprecato)
description: Creazione di Windows pacchetto di download multimediale (deprecato)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Windows Metafile multimediali, Windows di download di supporti
- Windows Media Player,Windows pacchetti di download multimediale
- metafile, Windows di download multimediale
- Windows Pacchetti di Windows multimediali multimediali
- Windows pacchetti di download multimediale, creazione
- creazione Windows pacchetti di download multimediale
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ac29d647605feaae5cc9a93f713d112fad8e41ea459209644398d2aeab222168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839763"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a>Creazione di Windows pacchetto di download multimediale (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

Seguire questa procedura per creare un pacchetto Windows download multimediale.

1.  **Creare un bordo.** Usare le stesse tecniche usate per creare un'interfaccia per Windows Media Player. Progettare il bordo in modo che il ridimensionamento Windows Media Player non rovini la composizione degli elementi del bordo. Ad esempio, usare un colore a tinta unita o una visualizzazione come sfondo perché questi verranno ridimensionati Windows Media Player ridimensionati.
2.  **Comprimere il contenuto del bordo.** Creare una cartella compressa (con un.zip estensione di file) che contiene i file di bordo: immagini, JScript file e il file di definizione dell'interfaccia con estensione wms. Rinominare il file compresso in modo che abbia estensione wmz.
3.  **Scrivere un metafile Windows Media.** Windows Media Player il bordo non verrà caricato a meno che non si crei un metafile Windows Media con estensione asx che implementa **l'elemento SKIN.** Il metafile può essere usato anche per creare una playlist che descrive il contenuto incluso nel pacchetto.
4.  **Assemblare il contenuto.** Inserire tutti i file da usare in una cartella. Sono inclusi file audio, file video, metafile e file di definizione del bordo.
5.  **Creare il pacchetto.** Creare una cartella compressa (con .zip file con estensione ) che contiene il file di bordo, i file di contenuto e il metafile. Modificare l'estensione del nome file .zip file con estensione wmd.
6.  **Pubblicare il pacchetto in un sito Web.** Il pacchetto completato è pronto per essere pubblicato in un sito Web e scaricato dagli utenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Pacchetti di download multimediali (deprecati)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




