---
description: Windows Vista consente di utilizzare in modo più significativo le immagini di anteprima specifiche dei file rispetto alle versioni precedenti di Windows.
title: Gestori di anteprime
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233189"
---
# <a name="thumbnail-handlers"></a>Gestori di anteprime

Windows Vista consente di utilizzare in modo più significativo le immagini di anteprima specifiche dei file rispetto alle versioni precedenti di Windows. Windows Vista viene usato in tutte le visualizzazioni, nelle finestre di dialogo e per qualsiasi tipo di file che li fornisce. Anche le altre applicazioni possono utilizzare l'anteprima. È stata modificata anche la visualizzazione delle anteprime. A questo punto, è disponibile uno spettro continuo di dimensioni selezionabili dall'utente anziché le dimensioni discrete, ad esempio le icone e le anteprime fornite in Windows XP.

> [!Note]  
> Si potrebbero sentire queste anteprime denominate icone attive.

 

Le anteprime della risoluzione a 32 bit e le dimensioni di 256x256 pixel vengono spesso utilizzate nell'interfaccia utente di Windows Vista. I proprietari del formato di file devono essere preparati per visualizzare le anteprime a tale dimensione. Devono inoltre fornire immagini non statiche per le anteprime che riflettono il contenuto del file specifico. Ad esempio, l'anteprima di un file di testo dovrebbe mostrare una versione in miniatura del documento, incluso il testo.

L'interfaccia [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) è stata introdotta in modo da rendere più semplice e intuitiva la visualizzazione di un'anteprima, quando sarebbe stato usato [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) . Si noti che il codice esistente che usa **IExtractImage** è ancora valido in Windows Vista. Tuttavia, **IExtractImage** non è supportato nel riquadro dei **Dettagli** .

In questo argomento vengono trattati i seguenti temi:

-   [Processi di anteprima](#thumbnail-processes)
-   [Dimensioni e cache delle anteprime](#thumbnail-cache-and-sizing)
-   [Sovrimpressioni anteprima](#thumbnail-overlays)
-   [Aree di visualizzazione delle anteprime](#thumbnail-adornments)
-   [Registrazione del gestore di anteprime](#registering-your-thumbnail-handler)
-   [Argomenti correlati](#related-topics)

## <a name="thumbnail-processes"></a>Processi di anteprima

I gestori, inclusi i gestori di anteprime, vengono eseguiti per impostazione predefinita in un processo separato. È possibile forzare l'esecuzione in-process del gestore passando un valore **null** come contesto di associazione in una chiamata a [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) come illustrato di seguito:


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



Per impostazione predefinita, è anche possibile rifiutare esplicitamente l'esecuzione out-of-process impostando la voce DisableProcessIsolation nel registro di sistema, come illustrato in questo esempio. L'identificatore di classe (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} è il CLSID per le implementazioni di [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>Dimensioni e cache delle anteprime

Quando è necessaria un'anteprima, Windows controlla prima di tutto la cache delle anteprime per l'immagine. L'estrazione dell'anteprima viene chiamata se l'immagine non viene trovata nella cache. Viene anche chiamato quando l'ora dell'Ultima modifica dell'immagine è successiva a quella della copia nella cache.

Le immagini di anteprima in questa cache vengono archiviate in un set di dimensioni discrete. Tutte le dimensioni vengono specificate in pixel.

-   32x32
-   96x96
-   256x256
-   1024x1024

> [!Note]  
> Questi valori sono soggetti a modifiche. Il codice non deve presupporre che vengano sempre utilizzate dimensioni specifiche.

 

Se un'immagine non è quadrata, non è necessario riempirla manualmente. Windows è responsabile del rispetto delle proporzioni originali e del riempimento dell'immagine a una dimensione quadrata.

Quando viene richiesta un'immagine di una determinata dimensione, a meno che non venga rilevata una corrispondenza esatta, Windows Vista recupera sempre l'immagine più grande successiva e la ridimensiona fino alla dimensione richiesta. Le dimensioni di un'immagine non vengono mai ridimensionate come nel caso delle versioni precedenti di Windows.

Nella tabella seguente vengono forniti alcuni esempi della relazione tra le dimensioni richieste e le dimensioni disponibili.



| Dimensioni massime dell'immagine fornite | Dimensioni richieste dall'estrattore | Fornire                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156x120                        | 256x256                         | 156x120 (non riempire, mantenere le proporzioni) |
| 2048x1024                      | 256x256                         | con dimensioni 256x128 (non riempire, mantenere le proporzioni) |



 

È possibile dichiarare un punto di interruzione come parte della voce dell'ID programma dell'app associata nel registro di sistema. Al di sotto di questa dimensione, le anteprime non vengono usate.

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

La voce ThumbnailCutoff è uno dei \_ valori DWORD reg.

| Valore | Cambio data | HighDPI sensibile |
|-------|--------|-------------------|
| 0     | 32x32  | Sì               |
| 1     | 16x16  | Sì               |
| 2     | 48x48  | Sì               |
| 3     | 16x16  | Sì               |


Una sensibilità di punti per pollice (dpi) elevata indica che le dimensioni in pixel dell'anteprima vengono regolate automaticamente per il valore dpi maggiore. Ad esempio, un'immagine di 32x32 a 96 dpi sarà un'immagine 40x40 a 120 dpi.

Se la voce ThumbnailCutoff non è specificata, il valore predefinito di cutoff è 20x20 (non con distinzione dpi).

## <a name="thumbnail-overlays"></a>Sovrimpressioni anteprima

Le sovrapposizioni di anteprime, una piccola immagine visualizzata sull'angolo inferiore destro dell'anteprima, offrono agli sviluppatori la possibilità di applicare l'identificazione del marchio alle anteprime. Le sovrimpressioni vengono dichiarate nel registro di sistema come parte della voce dell'ID programma dell'app associata, come illustrato di seguito:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

La voce TypeOverlay contiene un \_ valore reg SZ interpretato nel modo seguente:

-   Se il valore è un riferimento a una risorsa (un file con estensione **ico** incorporato nella dll) `ISVComponent.dll,-155` , ad esempio, tale immagine viene usata come sovrapposizione per i file con l'estensione di tale file. Si noti che in questo esempio **155** è l'ID resouce e se la dll non è presente in un percorso standard, ad esempio **C:/Windows/system32**, il percorso completo è obbligatorio anziché solo il nome della dll.
-   Se il valore è una stringa vuota, non viene applicata alcuna sovrapposizione all'immagine.
-   Se il valore non è presente, viene utilizzata l'icona predefinita dell'applicazione associata.

Le sovrimpressioni per le anteprime devono essere fornite solo tramite questo meccanismo e applicate da Windows. Non applicare sovrapposizioni.

## <a name="thumbnail-adornments"></a>Aree di visualizzazione delle anteprime

Le aree di visualizzazione, ad esempio le ombreggiature, vengono applicate alle anteprime basate sul tema attualmente selezionato dell'utente. Le aree di strumenti sono fornite da Windows; non crearli manualmente. Windows potrebbe modificare l'aspetto di particolari aree di specializzazione in qualsiasi momento, pertanto se si ha la proprietà si rischia di non essere sincronizzati con il sistema. È possibile che le anteprime si trovino in un punto qualsiasi.

Le aree di visualizzazione potenziali sono dichiarate nel registro di sistema come parte della voce dell'ID programma dell'app associata, come illustrato di seguito:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

La voce relativa al trattamento contiene uno dei \_ valori DWORD reg seguenti:



| Valore | Significato         |
|-------|-----------------|
| 0     | Nessun ornamento    |
| 1     | Ombreggiatura     |
| 2     | Bordo foto    |
| 3     | Pignoni video |


Per impostazione predefinita, un'ombreggiatura viene applicata alle immagini.

## <a name="registering-your-thumbnail-handler"></a>Registrazione del gestore di anteprime

La registrazione di un gestore di anteprime è basata sulle associazioni di file standard.

Il GUID dell'estensione della shell del gestore di anteprime è `E357FCCD-A995-4576-B01F-234630154E96` .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[Compilazione di gestori di anteprime](building-thumbnail-providers.md)
</dt> <dt>

[Linee guida per gestore anteprime](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



