---
description: Media Foundation attributi per gli oggetti intestazione ASF
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Media Foundation attributi per gli oggetti intestazione ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f0125373000c370f848239717b00aa2615fc16faa84270236704e124cb3bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061181"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Media Foundation attributi per gli oggetti intestazione ASF

L'oggetto intestazione ASF di primo livello per un file contiene diversi oggetti intestazione secondaria ASF. L'oggetto ContentInfo archivia le informazioni di tutti questi oggetti Header ed espone determinati valori a un'applicazione tramite attributi.

## <a name="file-properties-object"></a>Oggetto Proprietà file

Questo oggetto intestazione è presente in tutti i file ASF. Questi campi descrivono gli attributi a livello di file dell'intera presentazione. Nella tabella seguente sono elencati i campi nell'oggetto Proprietà file e gli attributi del descrittore di presentazione corrispondenti.



| Campo Oggetto proprietà file | Attributo del descrittore di presentazione                                                                            | Descrizione                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| ID file                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FILE \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Identificatore univoco per questo file.                                                               |
| Dimensioni file                    | [**DIMENSIONI TOTALI \_ DEL \_ \_ FILE MF PD \_**](mf-pd-total-file-size-attribute.md)                                         | Dimensioni del file, in byte.                                                                    |
| Data creazione                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ CREATION \_ TIME**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | Data e ora di creazione del file.                                                               |
| Conteggio pacchetti di dati           | [**PACCHETTI \_ MF PD \_ ASF \_ FILEPROPERTIES \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Numero di pacchetti di dati nell'oggetto dati ASF.                                                 |
| Durata riproduzione                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ DURATA \_ RIPRODUZIONE**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Tempo necessario per riprodurre il file, in unità da 100 nanosecondi. Questo valore include il tempo di pre-registrazione. |
| Durata invio                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ SEND \_ DURATION**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Tempo necessario per inviare il file, in unità da 100 nanosecondi.                                       |
| Preroll                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PREROLL**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Periodo di tempo per il buffer dei dati prima della riproduzione del file, in unità da 100 nanosecondi.            |
| Flags                        | [**FLAG MF \_ PD \_ ASF \_ FILEPROPERTIES \_**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Flag che indicano se il file è trasmesso o ricercabile.                                    |
| Dimensioni minime pacchetti di dati     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Dimensioni minime dei pacchetti di dati nel file, in byte.                                        |
| Dimensioni massime pacchetti di dati     | [**FILE \_ ASF PD \_ \_ MFPROPRIETÀ \_ DIMENSIONI \_ MASSIME \_ PACCHETTI**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Dimensioni massime in byte dei pacchetti di dati nel file.                                        |
| Velocità in bit massima              | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Velocità in bit istantanea massima, in bit al secondo.                                            |



 

## <a name="stream-properties-object"></a>Oggetto Proprietà flusso

Questo oggetto intestazione descrive le proprietà dei flussi nel file ASF. In Media Foundation, questa operazione viene gestita dall'oggetto profilo e dall'oggetto di configurazione del flusso. Per altre informazioni, vedere [Creazione e configurazione di asf Flussi](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Oggetto Elenco codec

Se questo oggetto intestazione è presente, l'attributo [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md) fornisce un elenco di codec usati per codificare i flussi all'interno del file ASF. Ogni flusso deve avere le informazioni sul codec in questo oggetto.

## <a name="script-command-object"></a>Oggetto comando script

Se questo oggetto intestazione è presente, specifica un elenco di comandi script supportati nel file ASF. Un comando script è costituito da un tipo di comando, un nome di comando e un'ora di presentazione. Il tipo di comando e il nome del comando sono stringhe di caratteri wide. Questi comandi possono essere usati per notificare al client di eseguire un'azione in un determinato punto della presentazione. Ad esempio, un'applicazione può usare il tipo di comando "FILENAME" per riprodurre una sequenza continua di file ASF.

Per ottenere l'elenco dei comandi script, ottenere l'attributo [**SCRIPT \_ \_ ASF \_ PD MF**](mf-pd-asf-script-attribute.md) dal descrittore di presentazione. Un'applicazione deve recuperare tutti i comandi script prima di avviare la riproduzione.

## <a name="marker-object"></a>Oggetto Marker

Un marcatore è un segnalibro all'interno di un file ASF. Un'applicazione può usare marcatori per cercare vari punti all'interno del contenuto. Ogni marcatore è costituito da un nome di marcatore, dall'ora di presentazione associata e dall'offset dall'inizio del file. [**L'attributo \_ MF PD \_ ASF \_ MARKER**](mf-pd-asf-marker-attribute.md) fornisce un elenco di marcatori disponibili per il file.

## <a name="stream-bitrate-properties-object"></a>Oggetto Proprietà velocità in bit del flusso

Questa intestazione archivia la velocità in bit media di ogni flusso presente nel file ASF. Questo valore viene archiviato nel descrittore di flusso per il flusso nell'attributo [**\_ MF SD \_ ASF \_ STREAMBITRATES \_ BITRATE.**](mf-sd-asf-streambitrates-bitrate-attribute.md)

## <a name="content-encryption-object"></a>Oggetto di crittografia del contenuto

Questo oggetto intestazione è presente se il provider di contenuto ha protetto il contenuto usando Microsoft Digital Rights Management. Nella tabella seguente sono elencati i campi nell'oggetto Content Encryption Object e gli attributi del descrittore di presentazione corrispondenti:



| Campo Dell'oggetto di crittografia del contenuto | Attributo del descrittore di presentazione                                                                         | Descrizione                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Dati segreti                     | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ SECRET \_ DATA**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Matrice di byte contenente i dati segreti.                                                                 |
| Tipo di protezione                 | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ TYPE**](mf-pd-asf-contentencryption-type-attribute.md)                | Stringa con terminazione Null con valore "DRM".                                                       |
| ID chiave                          | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Stringa con terminazione Null che descrive l'identificatore di chiave.                                          |
| URL licenza                     | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ LICENSE \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md) | Stringa con terminazione Null contenente l'URL da cui acquisire la licenza per usare il contenuto. |



 

## <a name="extended-content-encryption-object"></a>Oggetto di crittografia del contenuto esteso

Questo oggetto intestazione è presente se il provider di contenuto ha protetto il contenuto usando Windows Media Rights Manager 7 SDK. [**L'attributo URL MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ LICENSE \_**](mf-pd-asf-contentencryption-license-url-attribute.md) fornisce una matrice di byte che corrisponde al campo Dati dell'oggetto intestazione. Questo campo è obbligatorio per usare il contenuto.

## <a name="extended-stream-properties-object"></a>Oggetto Proprietà flusso esteso

Questa intestazione fa parte dell'oggetto estensione intestazione. L'oggetto Proprietà flusso esteso fornisce le proprietà del flusso che non sono definite nell'oggetto Proprietà flusso. Queste proprietà vengono usate principalmente per determinare i parametri "bucket di perdita", usati dal decodificatore. Queste proprietà vengono usate anche dal codificatore durante la compressione dei dati. Viene gestito dall'oggetto profilo e dall'oggetto di configurazione del flusso. Per altre informazioni, vedere [Creazione e configurazione di asf Flussi](creating-and-configuring-asf-streams.md).

Nella tabella seguente sono elencati i campi Extended Stream Properties Object e gli attributi del descrittore di flusso corrispondenti.



| Campo Proprietà flusso esteso | Attributo del descrittore di flusso                                                                                | Descrizione                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Velocità in bit dei dati                     | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Velocità media dei dati, in bit al secondo.                                                                                   |
| Dimensione buffer                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Dimensioni del bucket di perdita. Il valore è il numero di millisecondi di dati che possono essere memorizzati nel buffer alla velocità media dei dati.      |
| Velocità in bit dei dati alternativa           | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Velocità massima dei dati, in bit al secondo. La velocità massima dei dati viene usata per i flussi con una velocità in bit variabile.                    |
| Dimensioni alternative del buffer            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Dimensioni massime del bucket di perdita. Il valore è il numero di millisecondi di dati che possono essere memorizzati nel buffer al picco di velocità dei dati. |
| ID lingua del flusso               | [**INDICE \_ DELL'ID LINGUA DI MF SD \_ ASF \_ EXTSTRMPROP \_ \_ \_**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | Lingua utilizzata dal flusso, specificata come indice nell'elenco delle lingue nell'oggetto Elenco lingue.         |



 

## <a name="language-list-object"></a>Oggetto Language List

Questo oggetto intestazione fa parte dell'oggetto estensione intestazione. Se presente, [**l'attributo \_ \_ \_ LANGLIST ASF di MF PD**](mf-pd-asf-langlist-attribute.md) fornisce un elenco di identificatori di lingua supportati nel file. Gli identificatori sono conformi a RFC 1766 per specificare le lingue.

## <a name="mutual-exclusion-object"></a>Oggetto di esclusione reciproca

Questa intestazione specifica gruppi di flussi e le relative proprietà, solo uno dei quali verrà recapitato alla volta. Per altre informazioni, vedere [Using Mutual Exclusion for ASF Flussi](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto ContentInfo di ASF](asf-contentinfo-object.md)
</dt> <dt>

[Oggetto Intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Supporto di ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



