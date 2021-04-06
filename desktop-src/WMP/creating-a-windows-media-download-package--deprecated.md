---
title: Creazione di un pacchetto di download di Windows Media (deprecato)
description: Creazione di un pacchetto di download di Windows Media (deprecato)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- Pacchetti di download di Windows Media, creazione
- creazione di pacchetti di download di Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044920"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a>Creazione di un pacchetto di download di Windows Media (deprecato)

Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.

Per creare un pacchetto di download di Windows Media, attenersi alla seguente procedura.

1.  **Creare un bordo.** Utilizzare le stesse tecniche utilizzate per creare un'interfaccia per Windows Media Player. Progettare il bordo in modo che il ridimensionamento di Windows Media Player non rovini la composizione degli elementi del bordo. Usare, ad esempio, una visualizzazione o un colore a tinta unita come sfondo, in quanto questi aumenteranno le prestazioni in base al ridimensionamento di Windows Media Player.
2.  **Comprimere il contenuto del bordo.** Creare una cartella compressa (con estensione zip) che contiene i file di bordo: immagini, file JScript e il file di definizione dell'interfaccia con estensione WMS. Rinominare il file compresso in modo che disponga di un'estensione di file WMZ.
3.  **Scrivere un metafile di Windows Media.** Windows Media Player non caricherà il bordo a meno che non si crei un metafile Windows Media con un'estensione del nome di file. ASX che implementi l'elemento **Skin** . Il metafile può essere utilizzato anche per creare una playlist che descriva il contenuto incluso nel pacchetto.
4.  **Assemblare il contenuto.** Inserire tutti i file che si desidera utilizzare in una cartella. Sono inclusi file audio, file video, metafile e file di definizione dei bordi.
5.  **Creare il pacchetto.** Creare una cartella compressa (con estensione zip) che contiene il file del bordo, i file di contenuto e il metafile. Modificare l'estensione del nome file del file con estensione zip in un'estensione di file WMD.
6.  **Pubblica il pacchetto in un sito Web.** Il pacchetto completato è pronto per essere pubblicato in un sito Web e scaricato dagli utenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Pacchetti di download di Windows Media (deprecato)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




