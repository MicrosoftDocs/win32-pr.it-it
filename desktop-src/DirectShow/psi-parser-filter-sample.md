---
description: Esempio di filtro del parser PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Esempio di filtro del parser PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569315"
---
# <a name="psi-parser-filter-sample"></a>Esempio di filtro del parser PSI

## <a name="description"></a>Descrizione

Il filtro del parser PSI riceve informazioni specifiche del programma da un flusso di trasporto MPEG-2 ed estrae le informazioni sul programma dalla tabella di associazione di programma (PAT) e dalle tabelle della mappa dei programmi (PMT). Queste informazioni consentono a un'applicazione di configurare il Demultiplexer MPEG-2. Il filtro supporta un'interfaccia personalizzata, [**IMpeg2PsiParser**](impeg2psiparser.md), per il recupero delle informazioni psi.

Questo filtro è progettato per i dispositivi MPEG-2, ad esempio i camcorder IEEE 1394 MPEG-2 e i dispositivi D-VHS. Per ulteriori informazioni, vedere il [driver MSTape](mstape-driver.md) . Per ottenere informazioni sul programma, le origini broadcast della televisione digitale devono usare un filtro TIF.

## <a name="usage"></a>Utilizzo

È possibile testare il filtro del parser PSI in GraphEdit come segue:

1.  Avviare GraphEdit.
2.  Inserire un'origine del trasporto MPEG-2. I camcorder MPEG-2 e i dispositivi D-VHS vengono visualizzati come "dispositivo unità secondaria nastro Microsoft AV/C" nella categoria origini acquisizione video.
3.  Connettere il filtro di origine al filtro MPEG-2 Demultiplexer.
4.  Usare la pagina delle proprietà in Demux per creare un pin di output con un tipo di supporto "MPEG-2 PSI". Questo pin fornirà le sezioni PAT e PMT.
5.  Utilizzare la pagina delle proprietà Demux per eseguire il mapping del PID 0x00 al pin di output. Impostare il tipo di contenuto su "MPEG2 PSI sections".
6.  Connettere il pin di output demux al parser PSI, come illustrato nella figura seguente.

    ![grafico del filtro del parser PSI](images/psi-parser.png)

7.  Eseguire il grafo per inviare i dati PSI al filtro del parser PSI. Quando il filtro decodifica le sezioni PAT, esegue automaticamente il mapping dei PID PMT allo stesso pin di output in Demux, in modo che riceva le sezioni PMT.
8.  Usare la pagina delle proprietà del parser PSI per selezionare un numero di programma. Nell'elenco dei flussi elementari della pagina delle proprietà vengono visualizzati il PID e il tipo di flusso associati a ogni flusso elementare nel programma selezionato. La pagina delle proprietà è progettata per riconoscere i tipi di flusso definiti in ISO/IEC 13818-1.
9.  Immettere il numero PID audio nella casella di modifica **PID audio** e il numero PID video nella casella di modifica **PID video** .
10. Fare clic sul pulsante **Visualizza programma** . Il parser PSI configurerà i pin di output in Demux in modo che corrispondano alle informazioni sul flusso di programma e eseguano il rendering dei pin.

> [!Note]  
> Viene fornita la pagina delle proprietà del parser PSI per semplificare i test e fornire codice di esempio per la configurazione del Demultiplexer MPEG-2. Non è consigliabile utilizzare le applicazioni. Le applicazioni devono configurare demux a livello di codice.

 

Per usare il filtro del parser PSI in un'applicazione, iniziare compilando il grafico di filtro dall'origine MPEG-2 al demux MPEG-2. Il codice per questo passaggio non è illustrato in questo articolo, perché la configurazione esatta del grafo dipende dall'origine.

Creare quindi un pin di output nel Demux per i dati PSI. Map PID 0x00, che è riservato per le sezioni PAT, a questo pin, come illustrato nel codice seguente:


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



Per ulteriori informazioni, vedere [utilizzo di MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md).

Aggiungere il filtro del parser PSI al grafo e connetterlo al pin di output in demux. Eseguire una query sul parser PSI per l'interfaccia [**IMpeg2PsiParser**](impeg2psiparser.md) . A questo punto, eseguire il grafo e \_ attendere \_ gli eventi di modifica del programma EC, che segnalano una nuova sezione Pat o PMT. Questo evento è un evento personalizzato definito dal filtro del parser PSI. Quando si riceve un \_ \_ evento di modifica del programma EC, è possibile ottenere le informazioni PSI disponibili chiamando i metodi **IMpeg2PsiParser** . In questa sezione vengono descritti i metodi necessari più di frequente.

Per ottenere il numero di programmi, usare il metodo [**IMpeg2PsiParser:: GetCountOfPrograms**](impeg2psiparser-getcountofprograms.md) :


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Per ottenere il numero di programma per un programma specifico, usare il metodo [**IMpeg2PsiParser:: GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md) :


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



Il numero di programma viene usato per ottenere le voci PMT per i singoli programmi. Per ottenere il numero di flussi elementari in un programma, usare il metodo [**GetCountOfElementaryStreams**](impeg2psiparser-getcountofelementarystreams.md) :


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Per ogni flusso elementare, il metodo [**IMpeg2PsiParser:: GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) restituisce il PID e il metodo [**IMpeg2PsiParser:: GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) restituisce il tipo di flusso:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



Il PID e il tipo di flusso consentono di configurare nuovi PIN di output in MPEG-2 Demultiplexer. Questo potrebbe richiedere una certa conoscenza dell'origine originale. Ad esempio, ISO/IEC 13818-1 definisce i tipi di flusso 0x80 tramite 0xFF come "utente privato", ma altri standard basati su MPEG-2 possono assegnare altri significati a questi tipi.

Il Demultiplexer MPEG-2 può creare nuovi PIN e nuovi mapping PID durante l'esecuzione del grafo, ma è necessario arrestare il grafo per la connessione dei pin.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Questo esempio viene installato nel percorso seguente: esempi *\[ radice \] SDK* \\ \\ \\ filtri DirectShow multimediali \\ \\ PSIParser.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> </dl>

 

 
