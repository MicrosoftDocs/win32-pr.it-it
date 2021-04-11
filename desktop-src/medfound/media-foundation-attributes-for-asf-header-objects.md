---
description: Attributi di Media Foundation per oggetti intestazione ASF
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Attributi di Media Foundation per oggetti intestazione ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db74ccb03536c7766dd7e1564119edbd41d5dbe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351601"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Attributi di Media Foundation per oggetti intestazione ASF

L'oggetto intestazione ASF di primo livello per un file contiene diversi oggetti dell'intestazione secondaria ASF. L'oggetto ContentInfo archivia le informazioni di tutti questi oggetti Header ed espone determinati valori a un'applicazione tramite gli attributi.

## <a name="file-properties-object"></a>Oggetto proprietà file

Questo oggetto intestazione è presente in tutti i file ASF. Questi campi descrivono gli attributi a livello di file dell'intera presentazione. Nella tabella seguente sono elencati i campi dell'oggetto proprietà file e gli attributi del descrittore di presentazione corrispondente.



| Campo oggetto proprietà file | Attribute descrittore presentazione                                                                            | Descrizione                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| ID file                      | [**\_ \_ \_ ID file delle proprietà dell'ASF MF \_ PD \_**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Identificatore univoco per il file.                                                               |
| Dimensioni file                    | [**\_ \_ dimensioni totali del \_ file MF PD \_**](mf-pd-total-file-size-attribute.md)                                         | Dimensioni del file, in byte.                                                                    |
| Data creazione                | [**ora di creazione delle proprietà di MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | Data e ora di creazione del file.                                                               |
| Numero di pacchetti di dati           | [**\_ \_ \_ pacchetti FileProperties ASF MF \_ PD**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Numero di pacchetti di dati nell'oggetto dati ASF.                                                 |
| Durata riproduzione                | [**\_ \_ \_ durata riproduzione FileProperties ASF \_ di MF PD \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Tempo necessario per riprodurre il file, in unità da 100 nanosecondi. Questo valore include il tempo di preiscrizione. |
| Durata invio                | [**\_durata dell' \_ \_ invio delle Proprietà FileProperties ASF \_ \_ di MF PD**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Tempo necessario per l'invio del file, in unità di 100 nanosecondi.                                       |
| Preroll                      | [**preroll delle proprietà di MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Tempo di memorizzazione dei dati nel buffer prima della riproduzione del file, in unità di 100 nanosecondi.            |
| Flags                        | [**flag per le proprietà di MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Flag che indicano se il file è broadcast o cercabile.                                    |
| Dimensioni minime pacchetto dati     | [**\_ \_ \_ \_ dimensioni minime del \_ pacchetto \_ per le proprietà ASF del valore MF PD ASF**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Dimensioni minime dei pacchetti di dati nel file, in byte.                                        |
| Dimensioni massime pacchetto dati     | [**\_dimensioni del \_ \_ \_ pacchetto max PD ASF FileProperties \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Dimensioni massime dei pacchetti di dati nel file, in byte.                                        |
| Velocità in bit massima              | [**\_velocità in \_ \_ \_ bit max PD ASF FileProperties \_**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Velocità in bit massima istantanea, in bit al secondo.                                            |



 

## <a name="stream-properties-object"></a>Oggetto proprietà flusso

Questo oggetto Header descrive le proprietà dei flussi nel file ASF. In Media Foundation, viene gestito dall'oggetto profilo e dall'oggetto di configurazione del flusso. Per ulteriori informazioni, vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Oggetto elenco di codec

Se questo oggetto intestazione è presente, l'attributo [**codec di MF \_ PD \_ ASF \_**](mf-pd-asf-codeclist-attribute.md) fornisce un elenco di codec usati per codificare i flussi all'interno del file ASF. Ogni flusso deve avere le informazioni sul codec in questo oggetto.

## <a name="script-command-object"></a>Oggetto comando script

Se questo oggetto intestazione è presente, viene specificato un elenco di comandi script supportati nel file ASF. Un comando per script è costituito da un tipo di comando, un nome di comando e un'ora di presentazione. Il tipo di comando e il nome del comando sono stringhe a caratteri wide. Questi comandi possono essere usati per notificare al client di eseguire un'azione in un determinato punto della presentazione. Ad esempio, un'applicazione può utilizzare il tipo di comando "FILENAME" per riprodurre una sequenza continua di file ASF.

Per ottenere l'elenco dei comandi di script, ottenere l'attributo di [**\_ \_ \_ script MF PD ASF**](mf-pd-asf-script-attribute.md) dal descrittore della presentazione. Un'applicazione deve recuperare tutti i comandi di script prima di avviare la riproduzione.

## <a name="marker-object"></a>Oggetto marcatore

Un marcatore è un segnalibro all'interno di un file ASF. Un'applicazione può usare i marcatori per cercare diversi punti all'interno del contenuto. Ogni marcatore è costituito da un nome di marcatore, dall'ora di presentazione associata e dall'offset dall'inizio del file. L'attributo [**MF \_ PD \_ ASF \_ marker**](mf-pd-asf-marker-attribute.md) fornisce un elenco di marcatori disponibili per il file.

## <a name="stream-bitrate-properties-object"></a>Oggetto proprietà velocità in bit flusso

Questa intestazione archivia la velocità in bit media di ogni flusso presente nel file ASF. Questo valore viene archiviato nel descrittore di flusso per il flusso nell'attributo di [**\_ velocità in \_ \_ \_ bit STREAMBITRATES di MF SD ASF**](mf-sd-asf-streambitrates-bitrate-attribute.md) .

## <a name="content-encryption-object"></a>Oggetto di crittografia del contenuto

Questo oggetto intestazione è presente se il provider di contenuti ha protetto il contenuto tramite Microsoft Digital Rights Management. Nella tabella seguente sono elencati i campi dell'oggetto di crittografia del contenuto e gli attributi del descrittore di presentazione corrispondenti:



| Campo oggetto crittografia contenuto | Attribute descrittore presentazione                                                                         | Descrizione                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Dati segreti                     | [**\_ \_ \_ dati segreti del CONTENTENCRYPTION \_ MF PD ASF \_**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Matrice di byte contenente dati Secret.                                                                 |
| Tipo di protezione                 | [**\_tipo di CONTENTENCRYPTION MF PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-type-attribute.md)                | Stringa con terminazione null con valore "DRM".                                                       |
| ID chiave                          | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Stringa con terminazione null che descrive l'identificatore di chiave.                                          |
| URL della licenza                     | [**\_URL della licenza MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) | Stringa con terminazione null che contiene l'URL da cui acquisire la licenza per utilizzare il contenuto. |



 

## <a name="extended-content-encryption-object"></a>Oggetto di crittografia del contenuto esteso

Questo oggetto intestazione è presente se il provider di contenuti ha protetto il contenuto mediante Windows Media Rights Manager 7 SDK. L'attributo dell' [**\_ URL di licenza MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) fornisce una matrice di byte che corrisponde al campo dati dell'oggetto intestazione. Questo campo è necessario per usare il contenuto.

## <a name="extended-stream-properties-object"></a>Oggetto proprietà del flusso esteso

Questa intestazione fa parte dell'oggetto estensione dell'intestazione. L'oggetto proprietà del flusso esteso fornisce le proprietà del flusso che non sono definite nell'oggetto proprietà del flusso. Queste proprietà vengono usate principalmente per determinare i parametri "leaky bucket", usati dal decodificatore. Queste proprietà vengono usate anche dal codificatore quando si comprimono i dati. Questa operazione viene gestita dall'oggetto profilo e dall'oggetto di configurazione del flusso. Per ulteriori informazioni, vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md).

La tabella seguente elenca i campi dell'oggetto delle proprietà del flusso esteso e gli attributi del descrittore di flusso corrispondenti.



| Campo proprietà flusso esteso | Attributo del descrittore di flusso                                                                                | Descrizione                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Velocità in bit dei dati                     | [**\_velocità in \_ \_ \_ \_ bit dei dati media \_ di MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Velocità media dei dati, in bit al secondo.                                                                                   |
| Dimensione buffer                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Avg \_ bufferSize**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Dimensioni bucket a perdita. Value indica il numero di millisecondi di dati che possono essere inseriti nel buffer in base alla velocità media dei dati.      |
| Velocità in bit alternativa dei dati           | [**\_velocità in \_ \_ \_ \_ bit massima dei dati di EXTSTRMPROP \_ MF SD ASF**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Velocità massima dei dati, in morsi al secondo. La velocità massima dei dati viene usata per i flussi con una velocità in bit variabile.                    |
| Dimensioni del buffer alternativo            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ bufferSize**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Dimensioni massime del bucket. Value indica il numero di millisecondi di dati che possono essere inseriti nel buffer alla velocità massima dei dati. |
| ID lingua flusso               | [**\_ \_ \_ \_ \_ indice ID lingua \_ MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | Linguaggio utilizzato dal flusso, specificato come indice nell'elenco di lingue nell'oggetto elenco lingue.         |



 

## <a name="language-list-object"></a>Oggetto elenco lingue

Questo oggetto intestazione fa parte dell'oggetto estensione dell'intestazione. Se presente, l'attributo per l'elenco di lingue [**MF \_ PD \_ ASF \_**](mf-pd-asf-langlist-attribute.md) fornisce un elenco di identificatori di lingua supportati nel file. Gli identificatori sono conformi a RFC 1766 per specificare le lingue.

## <a name="mutual-exclusion-object"></a>Oggetto di esclusione reciproca

Questa intestazione specifica i gruppi di flussi e le relative proprietà. solo uno di questi verrà recapitato alla volta. Per ulteriori informazioni, vedere [utilizzo dell'esclusione reciproca per i flussi ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto ContentInfo ASF](asf-contentinfo-object.md)
</dt> <dt>

[Oggetto intestazione ASF](asf-file-structure.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



