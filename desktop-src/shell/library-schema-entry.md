---
description: I file di descrizione della libreria sono file XML che definiscono le librerie.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Schema Descrizione libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bebbd7ed168cd977530ccfeb0b319c33142687
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104981063"
---
# <a name="library-description-schema"></a>Schema Descrizione libreria

I file di descrizione della libreria sono file XML che definiscono le librerie. Le librerie aggregano gli elementi da percorsi di archiviazione locali e remoti in una singola visualizzazione in Esplora risorse. I file di descrizione della libreria seguono lo schema della descrizione della libreria e vengono salvati come \* file con estensione library-ms.

In questo argomento sono incluse le sezioni seguenti:

-   [Panoramica dello schema di descrizione della libreria](#overview-of-the-library-description-schema)
-   [Controllo delle versioni dello spazio dei nomi](#namespace-versioning)
-   [Esempio di un file di descrizione della libreria](#example-of-a-library-description-file)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Panoramica dello schema di descrizione della libreria

Le librerie contengono file archiviati in uno o più percorsi di archiviazione. Le librerie non archiviano effettivamente questi file; al contrario, monitorano le cartelle che contengono i file e consentono agli utenti di accedere ai file e disporli in modi diversi. Ad esempio, un utente può avere file musicali in più cartelle in un disco rigido locale e anche in un disco rigido esterno. Utilizzando la **libreria musicale**, l'utente può accedere a tutti i file contemporaneamente e ordinarli tutti in base al nome dell'artista o al titolo dell'album come singolo gruppo.

Lo schema di descrizione della libreria è costituito da tre parti principali, descritte nella tabella seguente:



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informazioni generali sulla libreria | Informazioni sulla libreria, ad esempio nome, proprietario, versione, icona, che Esplora risorse può usare quando Visualizza la libreria a un utente.                   |
| Proprietà libreria          | Una o più proprietà che descrivono la libreria. Queste proprietà personalizzate sono specifiche della libreria.                                                     |
| Percorsi di libreria           | Uno o più connettori di ricerca che identificano i percorsi di archiviazione da includere nella libreria. Ognuno di questi percorsi può avere anche un set univoco di proprietà. |



 

I file di libreria in Windows 7 sono archiviati nella cartella nota FOLDERID \_ Libraries. Per impostazione predefinita, la \_ cartella FOLDERID Libraries si trova in% UserProfile% \\ AppData \\ roaming \\ Microsoft \\ Windows \\ Libraries.

## <a name="namespace-versioning"></a>Controllo delle versioni dello spazio dei nomi

Le versioni del formato di file della descrizione della libreria ( \* . Library-MS) vengono rilevate modificando lo spazio dei nomi. Per Windows 7, il formato del file è lo spazio dei nomi predefinito seguente: https://schemas.microsoft.com/windows/2009/library .

Le versioni del contenuto della libreria, tuttavia, vengono rilevate usando l' [<version>](schema-library-version.md) elemento in un file di descrizione della libreria specifico.

## <a name="example-of-a-library-description-file"></a>Esempio di un file di descrizione della libreria

Di seguito è riportato un esempio di un file di descrizione della libreria che definisce una raccolta per i file di documento.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elemento folderType (schema della libreria)](schema-library-foldertype.md)
</dt> <dt>

[Elemento iconReference (schema della libreria)](schema-library-iconreference.md)
</dt> <dt>

[Elemento isLibraryPinned (schema della libreria)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (schema della libreria)](schema-librarydescription.md)
</dt> <dt>

[Elemento Name (schema della libreria)](schema-library-name.md)
</dt> <dt>

[Elemento ownerSID (schema della libreria)](schema-library-ownersid.md)
</dt> <dt>

[Elemento Property (schema della libreria)](schema-library-property.md)
</dt> <dt>

[Elemento propertyStore (schema della libreria)](schema-library-propertystore.md)
</dt> <dt>

[Elemento searchConnectorDescription (schema della libreria)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Elemento searchConnectorDescriptionList (schema della libreria)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Elemento templateInfo (schema della libreria)](schema-library-templateinfo.md)
</dt> <dt>

[Elemento Version (schema della libreria)](schema-library-version.md)
</dt> <dt>

[Cerca nello schema di descrizione del connettore](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
