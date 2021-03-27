---
description: Questi elementi costituiscono i XML Schema utilizzati nelle procedure guidate per il trasferimento dei manifesti di pubblicazione sul Web e degli ordini di stampa online.
title: Trasferimento dello schema del manifesto
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994941"
---
# <a name="transfer-manifest-schema"></a>Trasferimento dello schema del manifesto

Questi elementi costituiscono i XML Schema utilizzati nelle procedure guidate per il trasferimento dei manifesti di pubblicazione sul Web e degli ordini di stampa online.

Gli elementi seguenti sono definiti per il manifesto di trasferimento.

-   [cancelledpage](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [failurepage](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [preferito](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [file](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [filelist](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [cartella](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [cartella](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [FormData](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [htmlui](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [imageproperty](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [metadati](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [netplace](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [Inserisci](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [ridimensionare](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [successpage](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [target](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [transfermanifest](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [uploadinfo](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)

## <a name="cancelledpage"></a>cancelledpage

Consente di specificare la pagina HTML sul lato server da visualizzare prima della chiusura della procedura guidata quando l'utente fa clic sul pulsante **Annulla** .

### <a name="syntax"></a>Sintassi


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| href      | Obbligatorio. URL della pagina HTML sul lato server da visualizzare quando l'utente fa clic sul pulsante **Annulla** . |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio |
|-----------------------|----------------|
| [uploadinfo](#syntax) | nessuno           |



 

## <a name="failurepage"></a>failurepage

Specifica la pagina HTML sul lato server da visualizzare se il caricamento non riesce.

### <a name="syntax"></a>Sintassi


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| href      | Obbligatorio. URL della pagina HTML sul lato server da visualizzare se il caricamento non riesce. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuna. Testo consentito. |



 

## <a name="favorite"></a>preferito

Indica alla procedura guidata di creare una voce di sito Web preferita dal menu **Preferiti** per l'URL specificato. Se questo elemento non viene specificato, l'elemento [htmlui](#syntax) viene usato al suo posto.

### <a name="syntax"></a>Sintassi


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                            |
|-----------|------------------------------------------------------------------------|
| comment   | Obbligatorio. Commento associato alla voce **Preferiti** .         |
| href      | Obbligatorio. URL della voce **Preferiti** .                          |
| name      | Obbligatorio. Nome dell'URL visualizzato nel menu **Preferiti** . |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuna. Testo consentito. |



 

## <a name="file"></a>file

Descrive un singolo file da copiare. È possibile che più elementi [file](#syntax) siano contenuti in un singolo nodo di [file](#syntax) .

### <a name="syntax"></a>Sintassi


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a>Attributi



| Attributo   | Descrizione                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentType | facoltativo. Tipo MIME del file.                                                                                                                                         |
| destination | Obbligatorio. Percorso suggerito per il file dopo che è stato caricato. Questo percorso è relativo all'URL di destinazione del sito di caricamento. Il sito di caricamento può modificare questo valore se necessario. |
| estensione   | facoltativo. Estensione del nome file.                                                                                                                               |
| id          | Obbligatorio. Indice numerico del file.                                                                                                                                   |
| size        | facoltativo. Dimensioni, in byte, del file.                                                                                                                                    |
| source      | Obbligatorio. Percorso file system completo per il file.                                                                                                                            |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre      | Elementi figlio                                          |
|---------------------|---------------------------------------------------------|
| [filelist](#syntax) | [metadati](#syntax), [post](#syntax), [ridimensionamento](#syntax) |



 

## <a name="filelist"></a>filelist

Contenitore per gli elementi che descrivono i file da copiare. È possibile [che più elementi](#syntax) FileDirectory siano contenuti in un singolo nodo [transfermanifest](#syntax) .

### <a name="syntax"></a>Sintassi


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a>Attributi



| Attributo   | Descrizione      |
|-------------|------------------|
| usesfolders | Non implementato. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre              | Elementi figlio  |
|-----------------------------|-----------------|
| [transfermanifest](#syntax) | [file](#syntax) |



 

## <a name="folder"></a>folder

Descrive la cartella in cui sono archiviati i file. È possibile che più elementi [cartella](#syntax) siano contenuti in un singolo nodo di [cartelle](#syntax) .

### <a name="syntax"></a>Sintassi


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a>Attributi



| Attributo   | Descrizione                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination | Obbligatorio. Percorso suggerito per la cartella dopo il caricamento. Questo percorso è relativo all'URL di destinazione del sito di caricamento. Il sito di caricamento può modificare questo valore se necessario. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio |
|-----------------------|----------------|
| [cartella](#syntax) | nessuno           |



 

## <a name="folderlist"></a>cartella

Contenitore per gli elementi che descrivono i file da copiare. Più elementi [cartella](#syntax) possono essere contenuti in un singolo nodo [transfermanifest](#syntax) .

### <a name="syntax"></a>Sintassi


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a>Attributi

Nessuna.

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre              | Elementi figlio    |
|-----------------------------|-------------------|
| [transfermanifest](#syntax) | [cartella](#syntax) |



 

## <a name="formdata"></a>FormData

Descrive i dati facoltativi del modulo codificato HTML che possono essere trasferiti con i file. Questo elemento viene aggiunto dal servizio se sceglie di caricare i file come post multiparte. I dati del form, insieme alle informazioni dell'elemento [post](#syntax) , vengono usati per creare l'intestazione post.

Più elementi [FormData](#syntax) possono essere contenuti in un singolo nodo [uploadinfo](#syntax) .

### <a name="syntax"></a>Sintassi


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                      |
|-----------|----------------------------------------------------------------------------------|
| name      | Obbligatorio. Definisce il nome dati del modulo associato a questa sezione del caricamento. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio |
|-----------------------|----------------|
| [uploadinfo](#syntax) | nessuno           |



 

## <a name="htmlui"></a>htmlui

URL della pagina HTML sul lato server da visualizzare quando la procedura guidata viene chiusa. Questo elemento crea una voce di pagina Web preferita nel menu **Preferiti** se l'elemento [preferito](#syntax) è assente e viene specificato il nome descrittivo del sito di caricamento.

### <a name="syntax"></a>Sintassi


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| href      | Obbligatorio. URL della pagina HTML sul lato server da visualizzare quando la procedura guidata viene chiusa. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuna. Testo consentito. |



 

## <a name="imageproperty"></a>imageproperty

Specifica una proprietà di immagine correlata al file. Più elementi [ImageProperty](#syntax) possono essere contenuti in un singolo nodo di [metadati](#syntax) .

### <a name="syntax"></a>Sintassi


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                  |
|-----------|----------------------------------------------|
| id        | Obbligatorio. ID della proprietà specifica. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre      | Elementi figlio         |
|---------------------|------------------------|
| [metadati](#syntax) | Nessuna. Testo consentito. |



 

## <a name="metadata"></a>metadata

Contenitore per elementi e testo che definisce i metadati per il file specifico. Più elementi di [metadati](#syntax) possono essere contenuti in un singolo nodo di [file](#syntax) .

### <a name="syntax"></a>Sintassi


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a>Attributi

Nessuna.

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre  | Elementi figlio           |
|-----------------|--------------------------|
| [file](#syntax) | [imageproperty](#syntax) |



 

## <a name="netplace"></a>netplace

Definisce la destinazione di una posizione di rete creata nella **rete** quando il caricamento è completo. La creazione di una posizione di rete può essere impedita tramite il metodo [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .

### <a name="syntax"></a>Sintassi


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| comment   | Obbligatorio. Commento visualizzato per l'icona del punto di rete quando il cursore si trova su di esso.         |
| href      | Obbligatorio. URL della voce del punto di rete.                                                   |
| name      | Obbligatorio. Nome dell'icona del punto di rete visualizzato nella cartella **risorse di rete** . |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuna. Testo consentito. |



 

## <a name="post"></a>post

URL a cui deve essere inviato il file. Questo elemento viene aggiunto dal servizio quando il trasferimento viene eseguito come post multiparte e, con [FormData](#syntax), viene usato per compilare l'intestazione post. Se il servizio sceglie di eseguire il trasferimento di file utilizzando World Wide Web Distributed Authoring and Versioning (WebDAV), non dovrebbe aggiungere questo elemento. È possibile che più elementi [post](#syntax) siano contenuti in un singolo nodo di [file](#syntax) .

### <a name="syntax"></a>Sintassi


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                    |
|-----------|--------------------------------------------------------------------------------|
| nomefile  | facoltativo. Nome del file inviato.                                   |
| href      | Obbligatorio. URL della cartella di destinazione.                                   |
| name      | Obbligatorio. Definisce il nome dati del modulo associato a questa sezione del post. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre  | Elementi figlio      |
|-----------------|---------------------|
| [file](#syntax) | [FormData](#syntax) |



 

## <a name="resize"></a>resize

Definisce il ridimensionamento e la ricompressione di un file di immagine nel formato JPEG. Se il file di origine è già in formato JPEG ed è minore o uguale alla larghezza e all'altezza specificate, non viene ridimensionato. Se il file di origine non è un file JPEG, viene convertito. È possibile impedire il ridimensionamento, la ricompressione e la conversione del file tramite il metodo [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) . Più elementi di [ridimensionamento](#syntax) possono essere contenuti in un singolo nodo di [file](#syntax) .

### <a name="syntax"></a>Sintassi


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CX        | Obbligatorio. Larghezza dell'immagine, in pixel, dopo il caricamento. Se questo valore è 0, **CX** viene calcolato dal valore **CY** per mantenere le dimensioni relative.  |
| cy        | Obbligatorio. Altezza dell'immagine, in pixel, dopo il caricamento. Se questo valore è 0, **CY** viene calcolato dal valore **CX** per mantenere le dimensioni relative. |
| qualità   | Obbligatorio. Il valore di qualità JPEG, compreso tra 0 e 100, 100 è la qualità più elevata.                                                                            |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre  | Elementi figlio |
|-----------------|----------------|
| [file](#syntax) | Nessuna.          |



 

## <a name="successpage"></a>successpage

Specifica la pagina HTML sul lato server da visualizzare se il caricamento ha esito positivo.

### <a name="syntax"></a>Sintassi


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| href      | Obbligatorio. URL della pagina HTML sul lato server da visualizzare se il caricamento ha esito positivo. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuna. Testo consentito. |



 

## <a name="target"></a>target

Cartella di destinazione specificata in formato Universal Naming Convention (UNC) o come server WebDAV. Il servizio aggiunge questa destinazione per specificare una cartella di destinazione se il trasferimento usa un protocollo WebDAV o file system. Se il servizio sceglie di eseguire il trasferimento di file come post multiparte, non dovrebbe aggiungere questo elemento.

### <a name="syntax"></a>Sintassi


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a>Attributi



| Attributo | Descrizione                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| href      | Obbligatorio. URL della cartella di destinazione. Usare il modulo **https://** per WebDAV o il modulo **\\ \\ \\ condivisione server** per UNC. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuna. Testo consentito. |



 

## <a name="transfermanifest"></a>transfermanifest

Nodo padre del file manifesto di trasferimento.

### <a name="syntax"></a>Sintassi


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a>Attributi

Nessuna.

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre | Elementi figlio                                                    |
|----------------|-------------------------------------------------------------------|
| nessuno           | [filefile](#syntax), [](#syntax) [fileuploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

Contenitore per gli elementi che forniscono informazioni dal sito di caricamento utilizzato nella transazione. Più elementi [uploadinfo](#syntax) possono essere contenuti in un singolo nodo [transfermanifest](#syntax) .

### <a name="syntax"></a>Sintassi


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a>Attributi



| Attributo    | Descrizione                                                                 |
|--------------|-----------------------------------------------------------------------------|
| FriendlyName | Obbligatorio. Nome descrittivo per il sito Web visualizzato nella procedura guidata. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre              | Elementi figlio                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [Preferiti](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax) |



 

 

 



