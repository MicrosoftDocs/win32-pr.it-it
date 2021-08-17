---
description: Quando si installa un codec, è necessario registrarlo nel Registro di sistema. È anche necessario assicurarsi che la cache delle anteprime venga aggiornata nel caso in cui nel computer siano già presenti immagini nel formato specificato.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Installazione e registrazione di codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc13a2d937e82eae3517b9b20440f4acbb10b16af3fa0b872eb0ddd6c2a8d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965180"
---
# <a name="codec-installation-and-registration"></a>Installazione e registrazione di codec

Quando si installa un codec, è necessario registrarlo nel Registro di sistema. È anche necessario assicurarsi che la cache delle anteprime venga aggiornata nel caso in cui nel computer siano già presenti immagini nel formato specificato.

In questo argomento sono incluse le sezioni seguenti:

-   [Registrazione di un codec](#registering-a-codec)
-   [Aggiornamento della cache delle anteprime durante l'installazione del codec](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Rendere il codec WIC-Enabled disponibile agli utenti](#making-your-wic-enabled-codec-available-to-users)
-   [Argomenti correlati](#related-topics)

## <a name="registering-a-codec"></a>Registrazione di un codec

Quando si registra un codec, vengono effettivamente registrati due componenti: il codificatore e il decodificatore. È anche necessario creare voci del Registro di sistema per registrare il formato del contenitore con i gestori di metadati per i formati di metadati supportati dal formato immagine.

Gli argomenti seguenti descrivono le voci del Registro di sistema necessarie per registrare il codec:

[Voci generali del Registro di sistema](-wic-generalregentries.md)

[Voci del Registro di sistema specifiche del codificatore](-wic-encoderregentries.md)

[Voci del Registro di sistema specifiche del decodificatore](-wic-decoderregentries.md)

[Integrazione con Windows Raccolta foto e Windows Explorer](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Aggiornamento della cache delle anteprime durante l'installazione del codec

Quando viene installato un codec, il programma di installazione deve chiamare la funzione seguente dopo aver scritto le voci del Registro di sistema.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Questa chiamata notifica Windows disponibili nuove informazioni sull'associazione di file. Se le immagini nel formato immagine esistono già nel computer, la cache delle anteprime conterrà le anteprime predefinite perché non era disponibile alcun decodificatore per estrarre le anteprime quando le immagini sono state acquisite per la prima volta. Quando si notifica Windows che è disponibile una nuova associazione di file, la cache delle anteprime elimina eventuali anteprime vuote ed estrae le anteprime effettive dai file che possono ora essere decodificati.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Rendere il codec WIC-Enabled disponibile agli utenti

Se si è un produttore di fotocamere, è possibile spedire i codec non elaborati nella scatola con le fotocamere. È anche possibile pubblicare i codec nella pagina Download del sito Web. Tuttavia, se un utente acquisisce un file di immagine nel formato da un'altra origine, ad esempio un amico, un collega aziendale o un altro sito Web, potrebbe non sapere dove ottenere il codec con cui decodificarlo.

A causa di questo problema, Windows un modo più semplice per gli utenti del formato immagine per trovare il codec e scaricarlo nel computer, a partire da Windows Vista. Se il Windows Raccolta foto riconosce un'estensione di file come formato di immagine e il codec per tale formato non è installato, una finestra di dialogo indica all'utente che la foto non può essere visualizzata e chiede se l'utente vuole scaricare il software necessario per visualizzarla. Quando l'utente accetta, viene visualizzato un sito Web ospitato da Microsoft con un collegamento al sito di download del produttore del codec. Facoltativamente, è possibile richiedere che gli utenti siano portati direttamente nel sito di download.

Se si vuole che le estensioni di file del formato immagine siano riconosciute dal Windows Raccolta foto in modo che gli utenti possano essere indirizzati al sito di download, è necessario eseguire le operazioni seguenti:

1.  Fornire un sito di download per il codec. È possibile avere una pagina separata per ogni codec fornito o una pagina che fornisce i download per tutti i codec.

    Il sito di download deve essere localizzato e facilmente ricercabile in base al modello di fotocamera.

2.  Fornire a Microsoft un elenco di estensioni per i formati di immagine e gli URL per i siti di download.

È necessario informare Microsoft delle estensioni per i nuovi codec che si sviluppano in futuro e di eventuali modifiche agli URL dei siti di download, in modo che le nuove informazioni possano essere aggiunte al Windows Raccolta foto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Conclusione (come scrivere un codec WIC-Enabled)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



