---
description: Quando si installa un codec, è necessario registrarlo nel registro di sistema. È inoltre necessario assicurarsi che la cache delle anteprime venga aggiornata nel caso in cui siano presenti immagini nel formato già presenti nel computer.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Installazione e registrazione di codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313417"
---
# <a name="codec-installation-and-registration"></a>Installazione e registrazione di codec

Quando si installa un codec, è necessario registrarlo nel registro di sistema. È inoltre necessario assicurarsi che la cache delle anteprime venga aggiornata nel caso in cui siano presenti immagini nel formato già presenti nel computer.

In questo argomento sono incluse le sezioni seguenti:

-   [Registrazione di un codec](#registering-a-codec)
-   [Aggiornamento della cache delle anteprime durante l'installazione del codec](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Rendere disponibile il codec WIC-Enabled per gli utenti](#making-your-wic-enabled-codec-available-to-users)
-   [Argomenti correlati](#related-topics)

## <a name="registering-a-codec"></a>Registrazione di un codec

Quando si registra un codec, si registrano in realtà due componenti, ovvero il codificatore e il decodificatore. È anche necessario creare voci del registro di sistema per registrare il formato del contenitore con i gestori dei metadati per i formati di metadati supportati dal formato di immagine.

Negli argomenti seguenti vengono descritte le voci del registro di sistema necessarie per registrare il codec:

[Voci generali del registro di sistema](-wic-generalregentries.md)

[Voci del registro di sistema specifiche del codificatore](-wic-encoderregentries.md)

[Voci del registro di sistema specifiche del decodificatore](-wic-decoderregentries.md)

[Integrazione con raccolta foto di Windows e Esplora risorse](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Aggiornamento della cache delle anteprime durante l'installazione del codec

Quando viene installato un codec, il programma di installazione deve chiamare la funzione seguente dopo aver scritto le relative voci del registro di sistema.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Questa chiamata notifica a Windows che sono disponibili nuove informazioni sull'associazione di file. Se nel computer sono già presenti immagini nel formato immagine, la cache delle anteprime conterrà le anteprime predefinite perché non è disponibile alcun decodificatore per estrarre le anteprime quando le immagini sono state acquisite per la prima volta. Quando si notifica a Windows che è disponibile una nuova associazione di file, la cache delle anteprime Elimina eventuali anteprime vuote ed estrae le anteprime effettive dai file che possono essere decodificati.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Rendere disponibile il codec WIC-Enabled per gli utenti

Se sei un produttore di fotocamere, puoi spedire i tuoi codec non elaborati con le tue fotocamere. È anche possibile pubblicare i codec nella pagina di download del sito Web. Tuttavia, se un utente acquisisce un file di immagine nel formato da un'altra origine, ad esempio un amico, un socio aziendale o un altro sito Web, potrebbe non essere in grado di individuare la posizione in cui il codec deve decodificare.

A causa di questo problema, Windows offre agli utenti un modo più semplice per trovare il codec e scaricarlo nel computer, a partire da Windows Vista. Se la raccolta foto di Windows riconosce un'estensione di file come formato di immagine e il codec per tale formato non è installato, una finestra di dialogo indica all'utente che non è possibile visualizzare la foto e chiede se l'utente vuole scaricare il software necessario per visualizzarlo. Quando l'utente accetta, un sito Web ospitato da Microsoft viene visualizzato con un collegamento al sito di download del produttore di codec. Facoltativamente, è possibile richiedere che gli utenti vengano portati direttamente al sito di download.

Se si vuole che le estensioni di file del formato di immagine siano riconosciute dalla raccolta foto di Windows in modo che gli utenti possano essere indirizzati al sito di download, è necessario eseguire le operazioni seguenti:

1.  Fornire un sito di download per il codec. È possibile avere una pagina separata per ogni codec fornito o una pagina che fornisce i download per tutti i codec.

    Il sito di download deve essere localizzato e facilmente ricercabile con il modello di fotocamera.

2.  Fornire a Microsoft un elenco di estensioni per i formati di immagine e gli URL per i siti di download.

È necessario informare Microsoft delle estensioni per tutti i nuovi codec sviluppati in futuro e di eventuali modifiche apportate agli URL dei siti di download, in modo da poter aggiungere le nuove informazioni alla raccolta foto di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Conclusione (come scrivere un CODEC WIC-Enabled)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



