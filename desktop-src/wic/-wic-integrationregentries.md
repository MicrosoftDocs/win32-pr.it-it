---
description: Questo argomento si applica a Windows Vista e versioni successive.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integrazione con Windows Raccolta foto e Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e20b690e2640fb40830721f1c6a3211641d81311724be2c70efae3781171e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549441"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Integrazione con Windows Raccolta foto e Windows Explorer

Questo argomento si applica a Windows Vista e versioni successive. Contiene le sezioni seguenti:

-   [Introduzione](#introduction)
-   [Integrazione con il Windows Archivio proprietà](#integration-with-the-windows-property-store)
-   [Integrazione con il Windows Raccolta foto](#integration-with-the-windows-photo-gallery)
-   [Integrazione con la cache Windows anteprima](#integration-with-the-windows-thumbnail-cache)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Per consentire a Windows Raccolta foto e Windows Explorer di visualizzare le anteprime e cercare e aggiornare i metadati dell'immagine standard, un codec deve avere un'implementazione delle interfacce [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) associate. L'interfaccia IThumbnailProvider viene usata per recuperare le anteprime e popolare la cache delle anteprime e l'interfaccia IPropertyStore viene usata per la ricerca e l'aggiornamento dei metadati associati a un file. A Windows Vista, tutti i tipi di file hanno anteprime e metadati, ma tipi di file diversi richiedono implementazioni diverse di queste interfacce per recuperare o generare le anteprime e i metadati. Il sistema fornisce implementazioni predefinite di queste interfacce. L'implementazione predefinita di IThumbnailProvider può essere usata per qualsiasi Windows di immagine abilitata per wic (WiC). L'implementazione predefinita di IPropertyStore può essere usata con qualsiasi formato di immagine abilitato per WIC basato su un contenitore Tagged Image File Format (TIFF) o JPEG. Per associare il formato immagine alle implementazioni predefinite di entrambe queste interfacce, è necessario aggiungere solo alcune voci del Registro di sistema.

Le voci seguenti indicano al Windows Raccolta foto e Windows Explorer che un'estensione di file (con estensione ext) e il tipo MIME associato sono associati a un formato immagine.

La voce seguente indica Windows e le applicazioni che usano il tipo di contenuto (noto anche come tipo mime) che un file con una determinata estensione (con estensione ext) è un formato di immagine. Il proprietario del tipo di file deve scegliere un che identifichi in modo univoco il formato di file e questo valore del tipo di contenuto `<image sub type value>` deve essere registrato con IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

La voce seguente indica Windows, Windows ricerca e applicazioni che usano [System.Kind](../properties/props-system-kind.md) che un'estensione di file (con estensione ext) deve essere considerata un'immagine. In particolare, indica che la proprietà System.Kind dell'estensione di file deve essere impostata su Immagine.

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

## <a name="integration-with-the-windows-property-store"></a>Integrazione con il Windows Archivio proprietà

A volte le stesse proprietà dei metadati vengono esposte in schemi di metadati diversi, spesso con nomi di proprietà diversi. Quando una di queste proprietà viene aggiornata, ma le altre non lo sono, i metadati all'interno del file possono non essere sincronizzati. Il gestore della proprietà photo fornisce l'implementazione predefinita di **IPropertyStore** per le immagini e viene usato dalle applicazioni, nonché da Windows Raccolta foto e Windows Explorer per garantire che tutti i metadati in un'immagine rimangano sincronizzati e che le proprietà visualizzate dalle applicazioni siano coerenti con quelle visualizzate da esplora Windows Raccolta foto e Windows. Quando il gestore delle proprietà della foto aggiorna i metadati, assicura che queste proprietà siano aggiornate in modo coerente in tutti i formati di metadati comuni presenti nel file.

Il gestore delle proprietà della foto deve comprendere il formato del contenitore e come individuare le varie proprietà al suo interno. In generale, non è possibile che il gestore delle proprietà della foto sappia come vengono disposti i vari blocchi di metadati in un formato di contenitore proprietario. Tuttavia, se i metadati nel formato del contenitore sono disposti allo stesso modo dei metadati in un formato contenitore TIFF o JPEG, il gestore delle proprietà della foto può sfruttare tale conoscenza per aggiornare i metadati in modo coerente anche nel formato del contenitore.

È possibile registrare questa associazione creando la voce del Registro di sistema seguente. Questa voce notifica al gestore della proprietà photo che il formato del contenitore identificato da questo GUID comprende gli stessi percorsi del linguaggio di query dei metadati del formato del contenitore con GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 è il GUID per il formato del contenitore TIFF.

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

La voce seguente associa l'implementazione predefinita di **IPropertyStore** del gestore della proprietà photo ai file con estensione ".ext". Il primo GUID è l'IID **dell'interfaccia IPropertyStore** e il secondo è il GUID dell'implementazione del gestore della proprietà foto.

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

I codec che usano un formato proprietario non compatibile con il formato del contenitore TIFF o JPEG devono scrivere la propria **implementazione di IPropertyStore.**

## <a name="integration-with-the-windows-photo-gallery"></a>Integrazione con il Windows Raccolta foto

Windows Raccolta foto è basato su WIC e può visualizzare qualsiasi formato di immagine abilitato per WIC per cui è installato il codec. Per notificare al sistema che il formato dell'immagine può essere aperto in Windows Raccolta foto, è necessario creare un'associazione di file creando le voci del Registro di sistema seguenti.

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

ProgID è in genere l'estensione del nome file aggiunta con la parola "file". Ad esempio, se l'estensione del nome file è .txt, progID sarà in genere "txtfile".

Potrebbero essere necessarie altre voci del Registro di sistema standard per supportare le associazioni di file. tuttavia, poiché l'y non è specifico di WIC, non sono nell'ambito di questo argomento.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Integrazione con la cache Windows delle anteprime

Le due voci seguenti indicano che l'implementazione del provider di anteprime WIC standard può essere usata per recuperare le anteprime per i file con questa estensione. Il primo GUID è l'IID [dell'interfaccia IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e il secondo è il GUID dell'implementazione di sistema standard di questa interfaccia. Tutte le voci in HLCR \\ .ext ShellEx vengono ripetute \\ in \\ HKCR \\ SystemFileAssociations \\ .ext \\ \\ ShellEx.

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

[Voci del Registro di sistema specifiche del codificatore](-wic-decoderregentries.md)
</dt> <dt>

[Installazione e registrazione codec](-wic-codecinstallandreg.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
