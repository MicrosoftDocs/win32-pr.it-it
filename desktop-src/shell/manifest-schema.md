---
description: Questi elementi costituiscono l'XML Schema utilizzato nel manifesto del trasferimento guidato pubblicazione Web e Ordinamento stampa online.
title: Trasferire lo schema del manifesto
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 30324e32e1bd841423318a37eb1472d673ffc53c6e745f54f9398cec73138239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858857"
---
# <a name="transfer-manifest-schema"></a>Trasferire lo schema del manifesto

Questi elementi costituiscono l'XML Schema utilizzato nel manifesto del trasferimento guidato pubblicazione Web e Ordinamento stampa online.

Gli elementi seguenti sono definiti per il manifesto di trasferimento.

-   [cancelledpage](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [pagina di errore](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [Preferito](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [file](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [Filelist](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [Cartella](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [elenco cartelle](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [dati modulo](#syntax)
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
-   [Metadati](#syntax)
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
-   [Ridimensionare](#syntax)
    -   [Sintassi](#syntax)
    -   [Attributes (Attributi)](#attributes)
    -   [Informazioni sull'elemento](#element-information)
-   [pagina di operazione riuscita](#syntax)
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

Specifica la pagina HTML lato server da visualizzare prima della chiusura della procedura guidata quando l'utente fa clic sul **pulsante** Annulla.

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
| href      | Obbligatorio. URL della pagina HTML lato server da visualizzare quando l'utente fa clic sul **pulsante** Annulla. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Nessuno           |



 

## <a name="failurepage"></a>pagina di errore

Specifica la pagina HTML lato server da visualizzare se il caricamento non riesce.

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
| [uploadinfo](#syntax) | Nessuno. Il testo è consentito. |



 

## <a name="favorite"></a>Preferito

Indica alla procedura guidata di creare una voce del sito Web preferita nel menu **Preferiti** per l'URL specificato. Se questo elemento non viene specificato, al suo posto viene usato l'elemento [htmlui.](#syntax)

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
| comment   | Obbligatorio. Commento associato alla **voce Preferiti.**         |
| href      | Obbligatorio. URL della voce **Preferiti.**                          |
| name      | Obbligatorio. Nome dell'URL visualizzato nel menu **Preferiti.** |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuno. Il testo è consentito. |



 

## <a name="file"></a>file

Descrive un singolo file da copiare. Più [elementi di file](#syntax) possono essere contenuti in un singolo nodo [filelist.](#syntax)

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
| Contenttype | facoltativo. Tipo MIME del file.                                                                                                                                         |
| destination | Obbligatorio. Percorso suggerito per il file dopo il caricamento. Questo percorso è relativo all'URL di destinazione del sito di caricamento. Il sito di caricamento può modificare questo valore in base alle esigenze. |
| estensione   | facoltativo. Estensione di file del file.                                                                                                                               |
| id          | Obbligatorio. Indice numerico del file.                                                                                                                                   |
| size        | facoltativo. Dimensioni del file, in byte.                                                                                                                                    |
| source      | Obbligatorio. Percorso file system completo per il file.                                                                                                                            |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre      | Elementi figlio                                          |
|---------------------|---------------------------------------------------------|
| [Filelist](#syntax) | [metadati,](#syntax) [post,](#syntax) [ridimensionamento](#syntax) |



 

## <a name="filelist"></a>Filelist

Contenitore per gli elementi che descrivono i file da copiare. Più [elementi filelist](#syntax) possono essere contenuti in un singolo [nodo transfermanifest.](#syntax)

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

Descrive una cartella in cui vengono archiviati i file. Più [elementi cartella](#syntax) possono essere contenuti in un singolo nodo [folderlist.](#syntax)

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
| destination | Obbligatorio. Percorso suggerito per la cartella dopo il caricamento. Questo percorso è relativo all'URL di destinazione del sito di caricamento. Il sito di caricamento può modificare questo valore in base alle esigenze. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio |
|-----------------------|----------------|
| [elenco cartelle](#syntax) | Nessuno           |



 

## <a name="folderlist"></a>elenco cartelle

Contenitore per gli elementi che descrivono i file da copiare. Più [elementi folderlist](#syntax) possono essere contenuti in un singolo [nodo transfermanifest.](#syntax)

### <a name="syntax"></a>Sintassi


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a>Attributi

Nessuno.

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre              | Elementi figlio    |
|-----------------------------|-------------------|
| [transfermanifest](#syntax) | [Cartella](#syntax) |



 

## <a name="formdata"></a>dati modulo

Descrive i dati facoltativi del modulo con codifica HTML che possono essere trasferiti con i file. Questo elemento viene aggiunto dal servizio se sceglie di caricare i file come post in più parti. I dati del modulo, insieme alle informazioni [dell'elemento post,](#syntax) vengono usati per creare l'intestazione post.

Più [elementi formdata](#syntax) possono essere contenuti in un singolo [nodo uploadinfo.](#syntax)

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
| name      | Obbligatorio. Definisce il nome dei dati del modulo associato a questa sezione del caricamento. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Nessuno           |



 

## <a name="htmlui"></a>htmlui

URL della pagina HTML sul lato server da visualizzare quando la procedura guidata viene chiusa. Questo elemento crea una voce di pagina [](#syntax) Web preferita nel **menu** Preferiti se l'elemento preferito è assente e viene specificato il nome descrittivo del sito di caricamento.

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
| [uploadinfo](#syntax) | Nessuno. Il testo è consentito. |



 

## <a name="imageproperty"></a>imageproperty

Specifica una proprietà dell'immagine relativa al file. Più [elementi imageproperty](#syntax) possono essere contenuti in un singolo [nodo di](#syntax) metadati.

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
| [Metadati](#syntax) | Nessuno. Il testo è consentito. |



 

## <a name="metadata"></a>metadata

Contenitore per elementi e testo che definiscono i metadati per il file specifico. Più [elementi](#syntax) di metadati possono essere contenuti in un singolo [nodo di file.](#syntax)

### <a name="syntax"></a>Sintassi


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a>Attributi

Nessuno.

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre  | Elementi figlio           |
|-----------------|--------------------------|
| [file](#syntax) | [imageproperty](#syntax) |



 

## <a name="netplace"></a>netplace

Definisce la destinazione per una posizione di rete creata in Risorse **di** rete al termine del caricamento. La creazione di una posizione di rete può essere impedita tramite il [**metodo IPublishingWizard::Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize)

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
| comment   | Obbligatorio. Commento visualizzato per l'icona del luogo di rete quando il cursore è posizionato su di essa.         |
| href      | Obbligatorio. URL della voce del luogo di rete.                                                   |
| name      | Obbligatorio. Nome dell'icona del luogo di rete visualizzata nella **cartella Risorse di** rete. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuno. Il testo è consentito. |



 

## <a name="post"></a>post

URL in cui deve essere pubblicato il file. Questo elemento viene aggiunto dal servizio quando il trasferimento viene eseguito come post in più parti e, con [formdata](#syntax), viene usato per compilare l'intestazione post. Se il servizio sceglie di eseguire il trasferimento di file World Wide Web WebDAV (Distributed Authoring and Versioning), non deve aggiungere questo elemento. Più [elementi post](#syntax) possono essere contenuti in un singolo nodo di [file.](#syntax)

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
| name      | Obbligatorio. Definisce il nome dei dati del modulo associato a questa sezione del post. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre  | Elementi figlio      |
|-----------------|---------------------|
| [file](#syntax) | [dati modulo](#syntax) |



 

## <a name="resize"></a>resize

Definisce il ridimensionamento e la ricompressione di un file di immagine in formato JPEG. Se il file di origine è già in formato JPEG ed è minore o uguale alla larghezza e all'altezza specificate, non viene ridimensionato. Se il file di origine non è un file JPEG, viene convertito. Il ridimensionamento, la ricompressione e la conversione del file possono essere impediti tramite il [**metodo IPublishingWizard::Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) Più [elementi di](#syntax) ridimensionamento possono essere contenuti in un singolo nodo di [file.](#syntax)

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
| Cx        | Obbligatorio. Larghezza dell'immagine, in pixel, dopo il caricamento. Se questo valore è 0, **cx** viene calcolato dal valore **cy** per mantenere le dimensioni relative.  |
| cy        | Obbligatorio. Altezza dell'immagine, in pixel, dopo il caricamento. Se questo valore è 0, **cy** viene calcolato dal valore **cx** per mantenere le dimensioni relative. |
| qualità   | Obbligatorio. Valore di qualità JPEG, compreso tra 0 e 100, con 100 come qualità più elevata.                                                                            |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre  | Elementi figlio |
|-----------------|----------------|
| [file](#syntax) | Nessuno.          |



 

## <a name="successpage"></a>pagina di operazione riuscita

Specifica la pagina HTML lato server da visualizzare se il caricamento ha esito positivo.

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
| href      | Obbligatorio. URL della pagina HTML lato server da visualizzare se il caricamento ha esito positivo. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuno. Il testo è consentito. |



 

## <a name="target"></a>target

Cartella di destinazione specificata in Universal Naming Convention (UNC) o come server WebDAV. Il servizio aggiunge questa destinazione per specificare una cartella di destinazione se il trasferimento usa un protocollo WebDAV file system destinazione. Se il servizio sceglie di eseguire il trasferimento di file come post in più parti, non deve aggiungere questo elemento.

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
| href      | Obbligatorio. URL della cartella di destinazione. Usare il **https://** per WebDAV o il modulo **\\ \\ di \\ condivisione server** per UNC. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre        | Elementi figlio         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Nessuno. Il testo è consentito. |



 

## <a name="transfermanifest"></a>transfermanifest

Nodo padre del file manifesto di trasferimento.

### <a name="syntax"></a>Sintassi


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a>Attributi

Nessuno.

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre | Elementi figlio                                                    |
|----------------|-------------------------------------------------------------------|
| Nessuno           | [filelist,](#syntax) [folderlist,](#syntax) [uploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

Contenitore per gli elementi che forniscono informazioni dal sito di caricamento usato nella transazione. Più [elementi uploadinfo](#syntax) possono essere contenuti in un singolo [nodo transfermanifest.](#syntax)

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
| Friendlyname | Obbligatorio. Nome descrittivo del sito Web visualizzato nella procedura guidata. |



 

### <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre              | Elementi figlio                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax) |



 

 

 



