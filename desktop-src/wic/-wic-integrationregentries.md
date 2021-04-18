---
description: Questo argomento si applica a Windows Vista e versioni successive.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integrazione con raccolta foto di Windows e Esplora risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314885"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Integrazione con raccolta foto di Windows e Esplora risorse

Questo argomento si applica a Windows Vista e versioni successive. Contiene le sezioni seguenti:

-   [Introduzione](#introduction)
-   [Integrazione con l'archivio di proprietà di Windows](#integration-with-the-windows-property-store)
-   [Integrazione con la raccolta foto di Windows](#integration-with-the-windows-photo-gallery)
-   [Integrazione con la cache delle anteprime di Windows](#integration-with-the-windows-thumbnail-cache)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Per abilitare la raccolta foto di Windows e Esplora risorse per visualizzare le anteprime e cercare e aggiornare i metadati delle immagini standard, un codec deve disporre di un'implementazione delle interfacce [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) associate. L'interfaccia IThumbnailProvider viene utilizzata per recuperare le anteprime e popolare la cache delle anteprime e l'interfaccia IPropertyStore viene utilizzata per la ricerca e l'aggiornamento dei metadati associati a un file. A partire da Windows Vista, tutti i tipi di file hanno anteprime e metadati, ma tipi di file diversi richiedono implementazioni diverse di queste interfacce per recuperare o generare le anteprime e i metadati. Il sistema fornisce le implementazioni predefinite di queste interfacce. L'implementazione predefinita di IThumbnailProvider può essere utilizzata per qualsiasi formato di immagine abilitato per Windows Imaging Component (WIC). L'implementazione predefinita di IPropertyStore può essere utilizzata con qualsiasi formato di immagine abilitato per WIC basato su un contenitore Tagged Image File Format (TIFF) o JPEG. Per associare il formato di immagine alle implementazioni predefinite di entrambe le interfacce, è necessario aggiungere solo alcune voci del registro di sistema.

Le voci seguenti indicano alla raccolta foto di Windows e a Esplora risorse che un'estensione di file (. ext) e il tipo MIME associato sono associati a un formato di immagine.

La voce seguente indica a Windows e alle applicazioni che usano il tipo di contenuto (noto anche come tipo MIME) che un file con un'estensione specifica (. ext) è un formato di immagine. Il proprietario del tipo di file deve scegliere un `<image sub type value>` che identifichi in modo univoco il formato di file e il valore del tipo di contenuto deve essere registrato con IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

La voce seguente indica a Windows, Windows Search e alle applicazioni che usano [System. Kind](../properties/props-system-kind.md) che un'estensione di file (. ext) deve essere considerata come un'immagine. In particolare, indica che la proprietà System. Kind dell'estensione del file deve essere impostata su Picture.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a>Integrazione con l'archivio di proprietà di Windows

Talvolta le stesse proprietà dei metadati sono esposte in schemi di metadati diversi, spesso con nomi di proprietà diversi. Quando una di queste proprietà viene aggiornata, ma le altre non lo sono, i metadati all'interno del file possono non essere sincronizzati. Il gestore delle proprietà Photo fornisce l'implementazione predefinita di **IPropertyStore** per le immagini e viene usato dalle applicazioni, nonché dalla raccolta foto di Windows e da Esplora risorse, per garantire che tutti i metadati in un'immagine rimangano sincronizzati e che le proprietà visualizzate dalle applicazioni siano coerenti con quelle visualizzate dalla raccolta foto di Windows e da Esplora risorse. Quando il gestore delle proprietà Photo aggiorna i metadati, verifica che queste proprietà vengano aggiornate in modo coerente in tutti i formati di metadati comuni presenti nel file.

Il gestore delle proprietà Photo deve comprendere il formato del contenitore e come individuare le varie proprietà al suo interno. In generale, il gestore delle proprietà Photo non è in grado di capire come i diversi blocchi di metadati sono disposti in un formato contenitore proprietario. Tuttavia, se i metadati nel formato del contenitore sono disposti allo stesso modo dei metadati in un formato contenitore TIFF o in un formato contenitore JPEG, il gestore delle proprietà Photo può sfruttare tali informazioni per aggiornare i metadati in modo coerente anche nel formato del contenitore.

È possibile registrare questa associazione creando la seguente voce del registro di sistema. Questa voce notifica al gestore della proprietà Photo che il formato del contenitore identificato da questo GUID riconosce gli stessi percorsi del linguaggio di query dei metadati del formato del contenitore con il GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 è il GUID del formato del contenitore TIFF).

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

La voce seguente associa l'implementazione predefinita del gestore delle proprietà Photo di **IPropertyStore** con i file con estensione ". ext". Il primo GUID è l'IID dell'interfaccia **IPropertyStore** e il secondo è il GUID dell'implementazione del gestore delle proprietà Photo.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

I codec che usano un formato proprietario non compatibile con il formato di contenitore TIFF o JPEG devono scrivere la propria implementazione di **IPropertyStore** .

## <a name="integration-with-the-windows-photo-gallery"></a>Integrazione con la raccolta foto di Windows

Raccolta foto di Windows si basa su WIC e può visualizzare qualsiasi formato di immagine abilitato per WIC per cui è installato il codec. Per notificare al sistema che il formato dell'immagine può essere aperto nella raccolta foto di Windows, è necessario creare un'associazione di file creando le voci del registro di sistema seguenti.

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

ProgID è in genere l'estensione del nome file aggiunta con la parola "file". Se, ad esempio, l'estensione del nome file è. txt, ProgID sarà in genere "txtFile".

Per supportare le associazioni di file, potrebbe essere necessario creare altre voci del registro di sistema standard. Tuttavia, poiché the'y non sono specifici di WIC, esulano dall'ambito di questo argomento.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Integrazione con la cache delle anteprime di Windows

Le due voci seguenti indicano che è possibile usare l'implementazione del provider di anteprime WIC standard per recuperare le anteprime dei file con questa estensione. Il primo GUID è l'IID dell'interfaccia [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) , mentre il secondo è il GUID dell'implementazione di sistema standard di questa interfaccia. (Tutte le voci in HLCR \\ . ext \\ ShellEx \\ vengono ripetute in HKCR \\ SystemFileAssociations \\ . ext \\ ShellEx \\ .)

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Voci del registro di sistema specifiche del codificatore](-wic-decoderregentries.md)
</dt> <dt>

[Installazione e registrazione di CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
