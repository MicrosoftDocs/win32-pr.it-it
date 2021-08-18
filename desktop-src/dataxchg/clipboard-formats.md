---
title: Formati degli Appunti
description: Una finestra può inserire più oggetti negli Appunti, ognuno dei quali rappresenta le stesse informazioni in un formato diverso. Gli utenti non devono essere a conoscenza dei formati degli Appunti usati per un oggetto negli Appunti.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- Appunti, formati
- Appunti, finestre
- Appunti, formati standard
- Appunti, formati registrati
- Appunti, formati sintetizzati
- formati degli Appunti standard
- formati degli Appunti registrati
- Formati degli Appunti sintetizzati
- formati degli Appunti cloud
- Formati della cronologia degli Appunti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6bd2dc9dda8c8ccecd164123af68865005d9d28d328ce5489abf23926113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991341"
---
# <a name="clipboard-formats"></a>Formati degli Appunti

Una finestra può inserire più oggetti negli Appunti, ognuno dei quali rappresenta le stesse informazioni in un formato diverso. Gli utenti non devono essere a conoscenza dei formati degli Appunti usati per un oggetto negli Appunti.

Negli argomenti seguenti vengono descritti i formati degli Appunti.

-   [Formati degli Appunti standard](#standard-clipboard-formats)
-   [Formati degli Appunti registrati](#registered-clipboard-formats)
-   [Formati degli Appunti privati](#private-clipboard-formats)
-   [Più formati degli Appunti](#multiple-clipboard-formats)
-   [Formati degli Appunti sintetizzati](#synthesized-clipboard-formats)
-   [Formati degli Appunti cloud e della cronologia degli Appunti](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Formati degli Appunti standard

I formati degli Appunti definiti dal sistema sono detti *formati degli Appunti standard.* Questi formati degli Appunti sono descritti in [**Formati standard degli Appunti**](standard-clipboard-formats.md).

## <a name="registered-clipboard-formats"></a>Formati degli Appunti registrati

Molte applicazioni funzionano con dati che non possono essere convertiti in un formato degli Appunti standard senza perdita di informazioni. Queste applicazioni possono creare formati di Appunti personalizzati. Un formato degli Appunti definito da un'applicazione è detto [formato degli Appunti registrato.](#registered-clipboard-formats) Ad esempio, se un'applicazione di elaborazione testi copiasse testo formattato negli Appunti usando un formato di testo standard, le informazioni di formattazione andrebbero perse. La soluzione consiste nel registrare un nuovo formato degli Appunti, ad esempio RTF (Rich Text Format).

Per registrare un nuovo formato degli Appunti, usare la [**funzione RegisterClipboardFormat.**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) Questa funzione accetta il nome del formato e restituisce un valore intero senza segno che rappresenta il formato degli Appunti registrato. Per recuperare il nome del formato degli Appunti registrato, passare il valore intero senza segno alla [**funzione GetClipboardFormatName.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea)

Se più di un'applicazione registra un formato degli Appunti con esattamente lo stesso nome, il formato degli Appunti viene registrato una sola volta. Entrambe le chiamate [**alla funzione RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) restituiscono lo stesso valore. In questo modo, due applicazioni diverse possono condividere i dati usando un formato degli Appunti registrato.

## <a name="private-clipboard-formats"></a>Formati degli Appunti privati

Un'applicazione può identificare un formato degli Appunti privato definendo un valore nell'intervallo **CF \_ PRIVATEFIRST** **tramite CF \_ PRIVATELAST.** Un'applicazione può usare un formato degli Appunti privato per un formato dati definito dall'applicazione che non deve essere registrato nel sistema.

Gli handle di dati associati ai formati degli Appunti privati non vengono liberati automaticamente dal sistema. Se le finestre usano formati degli Appunti privati, è possibile usare il messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) per liberare tutte le risorse correlate che non sono più necessarie.

Per altre informazioni sul messaggio [**WM \_ DESTROYCLIPBOARD,**](wm-destroyclipboard.md) vedere [Proprietà degli Appunti](clipboard-operations.md).

Un'applicazione può inserire handle di dati negli Appunti definendo un formato privato nell'intervallo **CF \_ GDIOBJFIRST** tramite **CF \_ GDIOBJLAST.** Quando si usano valori in questo intervallo, l'handle di dati non è un handle per un oggetto Windows Graphics Device Interface (GDI), ma è un handle allocato dalla funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con il flag GMEM \_ MOVEABLE. Quando gli Appunti vengono svuotati, il sistema elimina automaticamente l'oggetto usando la [**funzione GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)

## <a name="multiple-clipboard-formats"></a>Più formati degli Appunti

Una finestra può inserire più di un oggetto Appunti negli Appunti, ognuno dei quali rappresenta le stesse informazioni in un formato diverso. Quando si inserisce informazioni negli Appunti, la finestra deve fornire i dati nel maggior numero possibile di formati. Per scoprire quanti formati sono attualmente usati negli Appunti, chiamare la [**funzione CountClipboardFormats.**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats)

I formati degli Appunti che contengono la maggior parte delle informazioni devono essere inseriti prima negli Appunti, seguiti da formati meno descrittivi. Una finestra che incolla le informazioni dagli Appunti recupera in genere un oggetto Appunti nel primo formato riconosciuto. Poiché i formati degli Appunti vengono enumerati nell'ordine in cui vengono inseriti negli Appunti, anche il primo formato riconosciuto è il più descrittivo.

Si supponga, ad esempio, che un utente copie il testo con stile da un documento di elaborazione di testo. La finestra contenente il documento potrebbe inserire prima i dati negli Appunti in un formato registrato, ad esempio RTF. Successivamente, la finestra inserirà i dati negli Appunti in un formato meno descrittivo, ad esempio testo (**CF \_ TEXT**).

Quando il contenuto degli Appunti viene incollato in un'altra finestra, la finestra recupera i dati nel formato più descrittivo riconosciuto. Se la finestra riconosce RTF, i dati corrispondenti vengono incollati nel documento. In caso contrario, i dati di testo vengono incollati nel documento e le informazioni di formattazione andranno perse.

## <a name="synthesized-clipboard-formats"></a>Formati degli Appunti sintetizzati

Il sistema converte in modo implicito i dati tra determinati formati degli Appunti: se una finestra richiede dati in un formato non presente negli Appunti, il sistema converte un formato disponibile nel formato richiesto. Il sistema può convertire i dati come indicato nella tabella seguente.



| Formato degli Appunti     | Formato di conversione    |
|----------------------|----------------------|
| **CF \_ BITMAP**       | **CF \_ DIB**          |
| **CF \_ BITMAP**       | **CF \_ DIBV5**        |
| **CF \_ DIB**          | **CF \_ BITMAP**       |
| **CF \_ DIB**          | **RIQUADRO \_ CF**      |
| **CF \_ DIB**          | **CF \_ DIBV5**        |
| **CF \_ DIBV5**        | **CF \_ BITMAP**       |
| **CF \_ DIBV5**        | **CF \_ DIB**          |
| **CF \_ DIBV5**        | **RIQUADRO \_ CF**      |
| **CF \_ ENHMETAFILE**  | **CF \_ METAFILEPICT** |
| **CF \_ METAFILEPICT** | **CF \_ ENHMETAFILE**  |
| **CF \_ OEMTEXT**      | **CF \_ TEXT**         |
| **CF \_ OEMTEXT**      | **CF \_ UNICODETEXT**  |
| **CF \_ TEXT**         | **CF \_ OEMTEXT**      |
| **CF \_ TEXT**         | **CF \_ UNICODETEXT**  |
| **CF \_ UNICODETEXT**  | **CF \_ OEMTEXT**      |
| **CF \_ UNICODETEXT**  | **CF \_ TEXT**         |



 

Se il sistema fornisce una conversione automatica del tipo per un particolare formato degli Appunti, non è vantaggioso inserire i formati di conversione negli Appunti.

Se il sistema fornisce una conversione automatica del tipo per un particolare formato degli Appunti e si chiama [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) per enumerare i formati di dati degli Appunti, il sistema enumera innanzitutto il formato che si trova negli Appunti, seguito dai formati in cui può essere convertito.

Quando si copiano bitmap, è meglio inserire il formato **\_ CF DIB** o **CF \_ DIBV5** negli Appunti. Ciò è dovuto al fatto che i colori in una bitmap dipendente dal dispositivo (**CF \_ BITMAP**) sono relativi alla tavolozza di sistema, che può cambiare prima che la bitmap venga incollata. Se il formato **\_ CF DIB** o **CF \_ DIBV5** è negli Appunti e una finestra richiede il formato **CF \_ BITMAP,** il sistema esegue il rendering della bitmap indipendente dal dispositivo (DIB) usando la tavolozza corrente in quel momento.

Se si posiziona il formato **CF \_ BITMAP** negli Appunti (e non in **CF \_ DIB),** il sistema esegue il rendering del formato CF **\_ DIB** o **CF \_ DIBV5** non appena gli Appunti vengono chiusi. In questo modo si garantisce l'uso del riquadro corretto per generare il dib. Se si posiziona il formato **\_ CF DIBV5** con le informazioni sullo spazio colore della bitmap negli Appunti, il sistema convertirà i bit bitmap dallo spazio colore bitmap allo spazio colore sRGB quando viene richiesto **CF \_ DIB** o **CF \_ DIBV5.** Se **CF \_ DIBV5** viene richiesto quando non sono presenti informazioni sullo spazio colore negli Appunti, il sistema restituisce informazioni sullo spazio colore sRGB nella [**struttura BITMAPV5HEADER.**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) Le conversioni tra altri formati degli Appunti vengono eseguite su richiesta.

Se gli Appunti contengono dati nel formato **CF \_ PALETTE,** l'applicazione deve usare le funzioni [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) per realizzare qualsiasi altro dato negli Appunti rispetto a tale riquadro logico.

Esistono due formati degli Appunti per i metafile: **CF \_ ENHMETAFILE** e **CF \_ METAFILEPICT**. Specificare **CF \_ ENHMETAFILE** per i metafile migliorati e **CF \_ METAFILEPICT** per Windows metafile.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Formati di Cronologia Appunti e Appunti cloud

Alcune versioni di Windows [includono Gli Appunti cloud](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard), che mantiene una cronologia degli elementi di dati recenti degli Appunti e può sincronizzarlo tra i dispositivi dell'utente.
Se non si vuole che i dati inseriti dall'applicazione negli Appunti siano inclusi nella cronologia degli Appunti o [](#registered-clipboard-formats) sincronizzati con altri dispositivi, l'applicazione può controllare questo comportamento inserendo i dati in determinati formati di Appunti registrati i cui nomi sono noti al sistema Windows:

- **ExcludeClipboardContentFromMonitorProcessing:** inserire tutti i dati negli Appunti in questo formato per impedire che tutti i formati degli Appunti vengano inclusi nella cronologia degli Appunti o sincronizzati con gli altri dispositivi dell'utente.
- **CanIncludeInClipboardHistory:** inserire un valore **[DWORD](../WinProg/windows-data-types.md)** serializzato pari a zero negli Appunti in questo formato per impedire che tutti i formati degli Appunti vengano inclusi nella cronologia degli Appunti o inserire un valore pari a uno per richiedere in modo esplicito che l'elemento degli Appunti venga incluso nella cronologia degli Appunti. Ciò non influisce sulla sincronizzazione con gli altri dispositivi dell'utente.
- **CanUploadToCloudClipboard:** inserire un valore **[DWORD](../WinProg/windows-data-types.md)** serializzato pari a zero negli Appunti in questo formato per impedire la sincronizzazione di tutti i formati degli Appunti con gli altri dispositivi dell'utente oppure inserire un valore pari a uno per richiedere in modo esplicito che l'elemento degli Appunti venga sincronizzato con altri dispositivi. Ciò non influisce sulla cronologia degli Appunti del dispositivo locale.

Come per altri formati di Appunti registrati, è necessario usare la funzione [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) per ottenere un valore intero senza segno che identifica ognuno dei tre formati precedenti.