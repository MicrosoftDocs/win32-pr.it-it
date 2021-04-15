---
title: Scrittura di file nel dispositivo
description: Scrittura di file nel dispositivo
ms.assetid: 66eaed16-032b-4ac0-a768-aded80f10255
keywords:
- Windows Media Gestione dispositivi, scrittura di file nei dispositivi
- Gestione dispositivi, scrittura di file nei dispositivi
- Guida per programmatori, scrittura di file nei dispositivi
- applicazioni desktop, scrittura di file nei dispositivi
- creazione di applicazioni Windows Media Gestione dispositivi, scrittura di file nei dispositivi
- scrittura di file nei dispositivi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d8b5234cc275eed1b4aa344c16a2b927b8122d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515502"
---
# <a name="writing-files-to-the-device"></a>Scrittura di file nel dispositivo

Prima di inviare un file a un dispositivo, è necessario che l'applicazione Scopra quali tipi di file e formati possono essere gestiti dal dispositivo, in modo che l'applicazione possa determinare se il file deve essere transcodificato prima di inviarlo o inviarlo senza modifiche o non inviarlo.

Nei passaggi seguenti viene illustrato come inviare un file esistente al dispositivo. Per creare un nuovo file nel dispositivo, ad esempio una playlist, vedere [creazione di una playlist nel dispositivo](creating-a-playlist-on-the-device.md).

1.  Ottenere il formato del file che si intende inviare al dispositivo. Per ulteriori informazioni, vedere [individuazione del formato di un file](discovering-a-files-format.md).
2.  Se il dispositivo è destinato a riprodurre il file,
    -   Eseguire una query sul file per le relative funzionalità di formato. Per ulteriori informazioni, vedere [individuazione delle funzionalità del formato del dispositivo](discovering-device-format-capabilities.md).
    -   Trovare un formato accettabile che l'applicazione possa creare dal file originale.
    -   Se il file deve essere transcodificato, transcodificarlo.
3.  Trovare una risorsa di archiviazione padre per il nuovo oggetto. Windows Media Gestione dispositivi non consente di individuare la posizione di archiviazione standard per i tipi di file specifici (file video o audio, WMV o BMP, una cartella "Preferiti" e così via), pertanto sarà necessario esaminare ogni dispositivo per tentare di individuare la posizione migliore per archiviare il nuovo oggetto. Altre applicazioni applicano una determinata struttura di cartelle, ad esempio Windows Media Player crea album, playlist e cartelle musica in cui la cartella Music contiene un artista e un albumname gerarchia. Per questo motivo, e poiché alcuni dispositivi potrebbero non essere stati testati con software diverso da Windows Media Player, tenere presente che la posizione degli oggetti playlist o album in una cartella diversa dalle cartelle playlist o album può talvolta causare oggetti non funzionanti in alcuni dispositivi.
4.  Se l'archiviazione di destinazione supporta [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3), creare una nuova interfaccia di metadati chiamando [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject). Impostare i metadati in un'interfaccia [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) . Per ulteriori informazioni, vedere [impostazione dei metadati in un file](setting-metadata-on-a-file.md). Gli unici metadati obbligatori sono g \_ wszWMDMFormatCode (un valore [**WMDM \_ FORMATCODE**](wmdm-formatcode.md) che descrive il contenuto), ma maggiore è il numero di metadati che è possibile fornire, più efficiente sarà il trasferimento per il provider di servizi.
5.  Inviare il file al dispositivo usando il metodo [**Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) . **Insert3** consente di includere i metadati nel dispositivo come parte del metodo. Per altre informazioni, vedere [invio del file al dispositivo](sending-the-file-to-the-device.md).

Il codice che illustra ognuno di questi passaggi è disponibile nelle pagine degli argomenti collegati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




