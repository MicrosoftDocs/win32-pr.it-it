---
title: Formati degli Appunti
description: Una finestra può inserire più di un oggetto negli Appunti, ciascuno dei quali rappresenta le stesse informazioni in un formato degli Appunti diverso. Gli utenti non devono essere a conoscenza dei formati degli appunti utilizzati per un oggetto negli Appunti.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- Appunti, formati
- Appunti, Windows
- Appunti, formati standard
- Appunti, formati registrati
- Appunti, formati sintetizzati
- formati degli Appunti standard
- formati degli Appunti registrati
- formati degli Appunti sintetizzati
- formati degli Appunti nel cloud
- formati di cronologia degli Appunti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193ee4cc10c17846d974e50b17a464207026280b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300380"
---
# <a name="clipboard-formats"></a>Formati degli Appunti

Una finestra può inserire più di un oggetto negli Appunti, ciascuno dei quali rappresenta le stesse informazioni in un formato degli Appunti diverso. Gli utenti non devono essere a conoscenza dei formati degli appunti utilizzati per un oggetto negli Appunti.

Negli argomenti seguenti vengono descritti i formati degli Appunti.

-   [Formati degli Appunti standard](#standard-clipboard-formats)
-   [Formati degli Appunti registrati](#registered-clipboard-formats)
-   [Formati degli Appunti privati](#private-clipboard-formats)
-   [Formati di più appunti](#multiple-clipboard-formats)
-   [Formati degli Appunti sintetizzati](#synthesized-clipboard-formats)
-   [Formati di cronologia degli Appunti e degli Appunti nel cloud](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Formati degli Appunti standard

I formati degli Appunti definiti dal sistema sono detti *formati degli Appunti standard*. Questi formati degli Appunti sono descritti in [**formati degli Appunti standard**](standard-clipboard-formats.md).

## <a name="registered-clipboard-formats"></a>Formati degli Appunti registrati

Molte applicazioni utilizzano dati che non possono essere convertiti in un formato degli Appunti standard senza perdita di informazioni. Queste applicazioni possono creare i propri formati degli Appunti. Un formato degli Appunti definito da un'applicazione è denominato [formato degli Appunti registrato](#registered-clipboard-formats). Se, ad esempio, un'applicazione per l'elaborazione di testi ha copiato il testo formattato negli appunti usando un formato di testo standard, le informazioni di formattazione andranno perse. La soluzione consiste nel registrare un nuovo formato degli Appunti, ad esempio RTF (Rich Text Format).

Per registrare un nuovo formato degli Appunti, usare la funzione [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) . Questa funzione accetta il nome del formato e restituisce un Unsigned Integer valore che rappresenta il formato degli Appunti registrato. Per recuperare il nome del formato degli Appunti registrato, passare il valore Unsigned Integer alla funzione [**GetClipboardFormatName**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea) .

Se più di un'applicazione registra un formato degli Appunti con lo stesso nome, il formato degli Appunti viene registrato una sola volta. Entrambe le chiamate alla funzione [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) restituiscono lo stesso valore. In questo modo, due applicazioni diverse possono condividere i dati utilizzando un formato degli Appunti registrato.

## <a name="private-clipboard-formats"></a>Formati degli Appunti privati

Un'applicazione può identificare un formato degli Appunti privati definendo un valore compreso nell'intervallo da **CF \_ PRIVATEFIRST** a **CF \_ PRIVATELAST**. Un'applicazione può utilizzare un formato degli Appunti privato per un formato di dati definito dall'applicazione che non deve essere registrato con il sistema.

Gli handle di dati associati ai formati degli Appunti privati non vengono liberati automaticamente dal sistema. Se le finestre usano formati degli Appunti privati, è possibile usare il messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) per liberare tutte le risorse correlate che non sono più necessarie.

Per ulteriori informazioni sul messaggio [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) , vedere la pagina relativa alla [proprietà degli Appunti](clipboard-operations.md).

Un'applicazione può inserire gli handle di dati negli appunti definendo un formato privato compreso nell'intervallo da **CF \_ GDIOBJFIRST** a **CF \_ GDIOBJLAST**. Quando si utilizzano valori in questo intervallo, l'handle di dati non è un handle per un oggetto Windows Graphics Device Interface (GDI), ma è un handle allocato dalla funzione [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) con il \_ flag GMEM mobile. Quando gli Appunti vengono svuotati, il sistema elimina automaticamente l'oggetto usando la funzione [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

## <a name="multiple-clipboard-formats"></a>Formati di più appunti

Una finestra può inserire più di un oggetto Appunti negli Appunti, ciascuno dei quali rappresenta le stesse informazioni in un formato degli Appunti diverso. Quando si inseriscono informazioni negli Appunti, la finestra deve fornire i dati nel maggior numero di formati possibile. Per conoscere il numero di formati attualmente utilizzati negli Appunti, chiamare la funzione [**CountClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats) .

I formati degli appunti che contengono la maggior parte delle informazioni devono essere inseriti prima negli Appunti, seguiti da formati meno descrittivi. Una finestra che incolla le informazioni dagli Appunti in genere recupera un oggetto Appunti nel primo formato riconosciuto. Poiché i formati degli Appunti vengono enumerati nell'ordine in cui vengono inseriti negli Appunti, il primo formato riconosciuto è anche quello più descrittivo.

Si supponga, ad esempio, che un utente copi il testo con stile da un documento di elaborazione testi. La finestra contenente il documento potrebbe inserire prima i dati negli Appunti in un formato registrato, ad esempio RTF. Successivamente, la finestra inserisce i dati negli Appunti in un formato meno descrittivo, ad esempio testo (**\_ testo CF**).

Quando il contenuto degli Appunti viene incollato in un'altra finestra, la finestra Recupera i dati nel formato più descrittivo che riconosce. Se la finestra riconosce il formato RTF, i dati corrispondenti vengono incollati nel documento. In caso contrario, i dati di testo vengono incollati nel documento e le informazioni di formattazione vengono perse.

## <a name="synthesized-clipboard-formats"></a>Formati degli Appunti sintetizzati

Il sistema converte in modo implicito i dati tra determinati formati degli Appunti: se una finestra richiede dati in un formato non presente negli Appunti, il sistema converte un formato disponibile nel formato richiesto. Il sistema può convertire i dati come indicato nella tabella seguente.



| Formato degli Appunti     | Formato di conversione    |
|----------------------|----------------------|
| **\_bitmap CF**       | **\_DIB CF**          |
| **\_bitmap CF**       | **\_DIBV5 CF**        |
| **\_DIB CF**          | **\_bitmap CF**       |
| **\_DIB CF**          | **\_tavolozza CF**      |
| **\_DIB CF**          | **\_DIBV5 CF**        |
| **\_DIBV5 CF**        | **\_bitmap CF**       |
| **\_DIBV5 CF**        | **\_DIB CF**          |
| **\_DIBV5 CF**        | **\_tavolozza CF**      |
| **\_ENHMETAFILE CF**  | **\_METAFILEPICT CF** |
| **\_METAFILEPICT CF** | **\_ENHMETAFILE CF**  |
| **\_OEMTEXT CF**      | **\_testo CF**         |
| **\_OEMTEXT CF**      | **\_UNICODETEXT CF**  |
| **\_testo CF**         | **\_OEMTEXT CF**      |
| **\_testo CF**         | **\_UNICODETEXT CF**  |
| **\_UNICODETEXT CF**  | **\_OEMTEXT CF**      |
| **\_UNICODETEXT CF**  | **\_testo CF**         |



 

Se il sistema fornisce una conversione automatica dei tipi per un particolare formato degli Appunti, non vi è alcun vantaggio per inserire i formati di conversione negli Appunti.

Se il sistema fornisce una conversione automatica dei tipi per un particolare formato degli Appunti e si chiama [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) per enumerare i formati di dati degli Appunti, il sistema enumera prima di tutto il formato negli Appunti, seguito dai formati in cui può essere convertito.

Quando si copiano le bitmap, è preferibile inserire il formato **CF \_ DIB** o **CF \_ DIBV5** negli Appunti. Ciò è dovuto al fatto che i colori in una bitmap dipendente dal dispositivo (**\_ bitmap CF**) sono relativi alla tavolozza di sistema, che può cambiare prima che la bitmap venga incollata. Se il formato **CF \_ DIB** o **CF \_ DIBV5** è negli Appunti e una finestra richiede il formato **di \_ bitmap CF** , il sistema esegue il rendering della bitmap indipendente dal dispositivo (DIB) utilizzando la tavolozza corrente in quel momento.

Se si inserisce il formato della **\_ bitmap CF** negli Appunti (e non **nella \_ DIB**), il sistema esegue il rendering del formato di visualizzazione **\_ DIB** o **CF \_ DIBV5** per gli Appunti non appena gli Appunti vengono chiusi. In questo modo si garantisce che la tavolozza corretta venga utilizzata per generare la DIB. Se si inserisce il formato **CF \_ DIBV5** con le informazioni sullo spazio dei colori della bitmap negli Appunti, il sistema convertirà i bit bitmap dallo spazio dei colori della bitmap allo spazio colore sRGB quando si richiede la presenza di **\_ DIB** o **\_ DIBV5 CF** . Se viene richiesto **CF \_ DIBV5** quando negli Appunti non sono presenti informazioni sullo spazio colore, il sistema restituisce le informazioni sullo spazio dei colori di sRGB nella struttura [**BITMAPV5HEADER**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) . Le conversioni tra gli altri formati degli appunti si verificano su richiesta.

Se gli Appunti contengono dati nel formato **della \_ tavolozza CF** , l'applicazione deve utilizzare le funzioni [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) e [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) per realizzare tutti gli altri dati negli Appunti rispetto a tale tavolozza logica.

Esistono due formati degli Appunti per i metafile: **CF \_ ENHMETAFILE** e **CF \_ METAFILEPICT**. Specificare **CF \_ ENHMETAFILE** per i metafile avanzati e **CF \_ METAFILEPICT** per i metafile di Windows.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Formati di cronologia degli Appunti e degli Appunti nel cloud

Alcune versioni di Windows includono [Appunti cloud](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard), che conservano una cronologia degli elementi di dati degli Appunti recenti e possono sincronizzarli tra i dispositivi dell'utente.
Se non si desidera che i dati inseriti nell'applicazione negli Appunti vengano inclusi nella cronologia degli Appunti o sincronizzati con altri dispositivi, l'applicazione può controllare questo comportamento inserendo i dati in alcuni [formati degli Appunti registrati](#registered-clipboard-formats) i cui nomi sono noti al sistema Windows:

- **ExcludeClipboardContentFromMonitorProcessing** : inserire i dati negli Appunti in questo formato per impedire che tutti i formati degli Appunti siano inclusi nella cronologia degli Appunti o sincronizzati con gli altri dispositivi dell'utente.
- **CanIncludeInClipboardHistory** : inserire un valore **[DWORD](../WinProg/windows-data-types.md)** serializzato pari a zero negli Appunti in questo formato per evitare che tutti i formati degli Appunti siano inclusi nella cronologia degli Appunti oppure inserire un valore di uno per richiedere esplicitamente che l'elemento degli Appunti venga incluso nella cronologia degli Appunti. Questa operazione non influisce sulla sincronizzazione con gli altri dispositivi dell'utente.
- **CanUploadToCloudClipboard** : inserire un valore **[DWORD](../WinProg/windows-data-types.md)** serializzato pari a zero negli Appunti in questo formato per evitare che tutti i formati degli Appunti vengano sincronizzati con gli altri dispositivi dell'utente oppure inserire un valore di uno per richiedere esplicitamente che l'elemento degli Appunti venga sincronizzato con altri dispositivi. Questa operazione non influisce sulla cronologia degli Appunti del dispositivo locale.

Come per gli altri formati degli Appunti registrati, è necessario usare la funzione [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) per ottenere un valore Unsigned Integer che identifichi ognuno dei 3 formati precedenti.