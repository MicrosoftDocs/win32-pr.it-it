---
description: Windows Vista usa immagini di anteprima specifiche del file rispetto alle versioni precedenti di Windows.
title: Gestori di anteprime
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 66641be49f8d118abc24c1a9a3fc8452fdacb51894452689276d87c910774d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675713"
---
# <a name="thumbnail-handlers"></a>Gestori di anteprime

Windows Vista usa immagini di anteprima specifiche del file rispetto alle versioni precedenti di Windows. Windows Vista li usa in tutte le visualizzazioni, nelle finestre di dialogo e per qualsiasi tipo di file che le fornisce. Anche altre applicazioni possono usare l'anteprima. È stata modificata anche la visualizzazione dell'anteprima. È ora disponibile una gamma continua di dimensioni selezionabili dall'utente anziché le dimensioni discrete, ad esempio icone e anteprime fornite in Windows XP.

> [!Note]  
> Queste anteprime possono essere chiamate icone in tempo reale.

 

Le anteprime con risoluzione a 32 bit e grandi fino a 256x256 pixel vengono spesso usate nell'interfaccia utente Windows Vista. I proprietari del formato di file devono essere preparati a visualizzare le anteprime a tale dimensione. Devono anche fornire immagini non statiche per le anteprime che riflettono il contenuto del file specifico. Ad esempio, l'anteprima di un file di testo dovrebbe mostrare una versione in miniatura del documento, incluso il testo.

[**L'interfaccia IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) è stata introdotta per rendere più semplice e semplice fornire un'anteprima rispetto al passato, quando sarebbe stato invece usato [**IExtractImage.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) Si noti che il codice esistente che usa **IExtractImage** è ancora valido in Windows Vista. Tuttavia, **IExtractImage** non è supportato nel **riquadro Dettagli.**

In questo argomento vengono trattati i seguenti temi:

-   [Processi di anteprima](#thumbnail-processes)
-   [Cache e ridimensionamento delle anteprime](#thumbnail-cache-and-sizing)
-   [Sovrimpressione delle anteprime](#thumbnail-overlays)
-   [Aree di controllo dell'anteprima](#thumbnail-adornments)
-   [Registrazione del gestore delle anteprime](#registering-your-thumbnail-handler)
-   [Argomenti correlati](#related-topics)

## <a name="thumbnail-processes"></a>Processi di anteprima

I gestori, inclusi i gestori di anteprime, vengono eseguiti per impostazione predefinita in un processo separato. È possibile forzare l'esecuzione in-process del gestore passando un valore **NULL** come contesto di associazione in una chiamata a [**IShellItem::BindToHandler,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) come illustrato di seguito:


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



È anche possibile rifiutare esplicitamente l'esecuzione del processo per impostazione predefinita impostando la voce DisableProcessIsolation nel Registro di sistema, come illustrato in questo esempio. L'identificatore di classe (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} è il CLSID per le implementazioni [**IThumbnailProvider.**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a>Cache e ridimensionamento delle anteprime

Quando è necessaria un'anteprima, Windows prima controlla la cache delle anteprime per l'immagine. L'estrattore di anteprime viene chiamato se l'immagine non viene trovata nella cache. Viene chiamato anche quando l'ora dell'ultima modifica dell'immagine è successiva a quella della copia nella cache.

Le immagini di anteprima in questa cache vengono archiviate in un set di dimensioni discrete. Tutte le dimensioni sono espresse in pixel.

-   32x32
-   96x96
-   256x256
-   1024x1024

> [!Note]  
> Questi valori sono soggetti a modifiche. Il codice non deve presupporre che verranno sempre usate dimensioni particolari.

 

Se un'immagine non è quadrata, non è consigliabile riempire manualmente l'immagine. Windows è responsabile del rispetto delle proporzioni originali e della spaziatura interna dell'immagine su una dimensione quadrata.

Quando viene richiesta un'immagine di una determinata dimensione, a meno che non venga trovata una corrispondenza esatta, Windows Vista recupera sempre l'immagine più grande successiva e la ridimensiona fino alle dimensioni richieste. Le dimensioni di un'immagine non vengono mai ridotte, come nelle versioni precedenti di Windows.

Nella tabella seguente vengono forniti alcuni esempi della relazione tra le dimensioni richieste e le dimensioni disponibili.



| Dimensioni massime dell'immagine specificate | Dimensioni richieste dall'estrattore | L'utente fornisce                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| 156x120                        | 256x256                         | 156x120 (non riempire, mantenere le proporzioni) |
| 2048x1024                      | 256x256                         | 256x128 (non riempire, mantenere le proporzioni) |



 

È possibile dichiarare un punto di taglio come parte della voce id programma dell'app associata nel registro. Al di sotto di queste dimensioni, le anteprime non vengono usate.

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

La voce ThumbnailCutoff è uno di questi valori \_ DWORD REG.

| Valore | Taglio | Sensibilità HighDPI |
|-------|--------|-------------------|
| 0     | 32x32  | Sì               |
| 1     | 16x16  | Sì               |
| 2     | 48x48  | Sì               |
| 3     | 16x16  | Sì               |


La sensibilità elevata dei punti per pollice (dpi) indica che le dimensioni in pixel dell'anteprima vengono regolate automaticamente in base al valore dpi maggiore. Ad esempio, un'immagine 32x32 a 96 dpi sarebbe un'immagine di 40x40 a 120 dpi.

Se la voce ThumbnailCutoff non è specificata, il valore predefinito è 20x20 (senza distinzione tra dpi).

## <a name="thumbnail-overlays"></a>Sovrimpressione delle anteprime

Le sovrimpressione di anteprima, una piccola immagine visualizzata nell'angolo inferiore destro dell'anteprima, offrono agli sviluppatori la possibilità di applicare l'identificazione del marchio alle anteprime. Le sovrimpressione vengono dichiarate nel Registro di sistema come parte della voce dell'ID programma dell'app associata, come illustrato di seguito:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

La voce TypeOverlay contiene un valore \_ REG SZ interpretato come segue:

-   Se il valore è un riferimento a una risorsa (un file con estensione **ico** incorporato nella DLL), ad esempio , tale immagine viene usata come sovrimpressione per i file con tale `ISVComponent.dll,-155` estensione. Si noti che in questo **esempio, 155** è l'ID della risorsa e se la DLL non è presente in un percorso standard (ad esempio **C:/Windows/System32),** è necessario il percorso completo anziché solo il nome della DLL.
-   Se il valore è una stringa vuota, all'immagine non viene applicata alcuna sovrimpressione.
-   Se il valore non è presente, viene usata l'icona predefinita dell'applicazione associata.

Le sovrimpressione per le anteprime devono essere fornite solo tramite questo meccanismo e applicate Windows. Non applicare le sovrimpressione manualmente.

## <a name="thumbnail-adornments"></a>Aree di controllo dell'anteprima

Le aree di controllo, ad esempio le ombreggiature, vengono applicate alle anteprime in base al tema attualmente selezionato dell'utente. Le aree di controllo vengono fornite Windows; non crearli manualmente. Windows possibile modificare l'aspetto di particolari aree di controllo in qualsiasi momento, quindi se si è proprietari si rischia di non essere sincronizzati con il sistema. Le anteprime potrebbero essere datate o non aggiornate.

Le potenziali aree di controllo vengono dichiarate nel Registro di sistema come parte della voce dell'ID programma dell'app associata, come illustrato di seguito:

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

La voce Treatment contiene uno di questi valori \_ DWORD REG:



| Valore | Significato         |
|-------|-----------------|
| 0     | Nessuna area di controllo    |
| 1     | Ombreggiatura     |
| 2     | Bordo foto    |
| 3     | Spongets video |


Per impostazione predefinita, alle immagini viene applicata un'ombreggiatura.

## <a name="registering-your-thumbnail-handler"></a>Registrazione del gestore delle anteprime

La registrazione di un gestore di anteprime si basa sulle associazioni di file standard.

Il GUID per l'estensione shell del gestore anteprime è `E357FCCD-A995-4576-B01F-234630154E96` .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[Creazione di gestori di anteprime](building-thumbnail-providers.md)
</dt> <dt>

[Linee guida per i gestori di anteprime](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



