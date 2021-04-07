---
description: Impostazioni dei campi DVINFO nel driver MSDV
ms.assetid: f0723da5-4f53-4f83-a657-ae42815a784e
title: Impostazioni dei campi DVINFO nel driver MSDV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4205a680833b0e2f8c6be2dc4cb65faa60515867
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746666"
---
# <a name="dvinfo-field-settings-in-the-msdv-driver"></a>Impostazioni dei campi DVINFO nel driver MSDV

Questa sezione descrive il modo in cui il driver MSDV compila la struttura [**DVinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .

La `DVINFO` struttura definisce il blocco di formato per le connessioni pin tra Msdv e altri filtri. Per impostazione predefinita, il filtro della barra di divisione DV viene usato durante l'acquisizione da un dispositivo DV e il filtro Mux DV viene usato durante la trasmissione al dispositivo. Tuttavia, le applicazioni possono fornire filtri personalizzati, quindi è utile comprendere il modo in cui MSDV popola il `DVINFO` blocco di formato.

La `DVINFO` struttura contiene le informazioni seguenti:

-   Due pacchetti di origine audio ausiliari (AAUX), per il primo e il secondo blocco audio.
-   Due pacchetti di controllo del codice sorgente AAUX, per il primo e il secondo blocco audio.
-   Un pacchetto di origine video ausiliario (VAUX).
-   Un pacchetto di controllo del codice sorgente VAUX.

Ogni frame in un flusso DV contiene i Pack AAUX e VAUX. Tuttavia, il `DVINFO` blocco di formato è statico e viene usato solo per stabilire la connessione del PIN. Quando il driver MSDV si connette, non esamina i pacchetti AAUX o VAUX nel flusso. USA invece un set di valori predefiniti, in base alle caratteristiche seguenti del dispositivo DV:

-   Indica se il dispositivo supporta un formato utente (DVCR) o un formato Professional (DVCPRO)
-   Tipo di segnale
-   Indica se il formato è NTSC o PAL. Se il dispositivo non riporta queste informazioni, MSDV per impostazione predefinita è le impostazioni NTSC.

Una volta avviato il flusso, è responsabilità dei filtri in modalità utente, ad esempio la barra di divisione DV, esaminare il contenuto effettivo di ogni frame DV. Poiché le informazioni possono essere modificate dal frame al frame, potrebbe essere necessario eseguire una modifica del formato dinamico per il filtro. Se, ad esempio, la frequenza audio viene modificata, il filtro potrebbe dover rinegoziare il tipo audio.

Se si acquisisce un file DV di tipo 1, la `DVINFO` struttura viene scritta nel file come formato di flusso (' strF '). Questi dati vengono ricavati direttamente dal blocco di formato fornito da MSDV. Come indicato, il contenuto effettivo del flusso potrebbe essere diverso. È responsabilità dell'applicazione esaminare i Pack AAUX e VAUX in ogni frame.

Negli argomenti seguenti è possibile trovare le tabelle che elencano tutti i campi usati da MSDV.

-   [Pacchetto di origine (AS) AAUX](aaux-source--as--pack.md)
-   [Pack del controllo del codice sorgente AAUX (ASC)](aaux-source-control--asc--pack.md)
-   [Pacchetto di origine (VS) VAUX](vaux-source--vs--pack.md)
-   [Pack del controllo del codice sorgente (VSC) di VAUX](vaux-source-control--vsc--pack.md)

Quando si leggono queste tabelle, consultare le specifiche seguenti:

-   IEC 61834
-   314M SMPTE
-   SMPTE 370

In ogni tabella la prima colonna restituisce il codice del campo, seguito dal numero di bit (tra parentesi). Le colonne rimanenti forniscono i valori dei campi. Molti dei campi AAUX e VAUX non sono rilevanti per la connessione pin, nel qual caso MSDV imposta un valore fittizio. Il valore numerico dell'intero Pack è elencato nella parte inferiore di ogni tabella.

Le note successive a ogni tabella forniscono ulteriori informazioni sui campi selezionati. Per descrizioni complete, vedere le specifiche. Inoltre, alcuni campi non hanno lo stesso significato in SMPTE 314M/SMPTE 370, come avviene in IEC 61834.

> [!Note]  
> Attualmente, DirectShow non supporta i formati DVCPRO. I valori elencati per i formati DVCPRO sono definiti per un uso futuro.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dati DV nel formato di file AVI](dv-data-in-the-avi-file-format.md)
</dt> <dt>

[Driver MSDV](msdv-driver.md)
</dt> </dl>

 

 



