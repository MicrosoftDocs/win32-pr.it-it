---
description: Esempio di filtro del parser PSI
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Esempio di filtro del parser PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de960d36900a417212cdd34ac795b504d4ad073ccd61619ffad110d5fe125fad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747926"
---
# <a name="psi-parser-filter-sample"></a>Esempio di filtro del parser PSI

## <a name="description"></a>Descrizione

Il filtro psi parser riceve informazioni specifiche del programma (PSI) da un flusso di trasporto MPEG-2 ed estrae le informazioni sul programma da Program Association Table (PAT) e Program Map Tables (PMT). Queste informazioni consentono a un'applicazione di configurare mpeg-2 Demultiplexer. Il filtro supporta un'interfaccia personalizzata, [**IMpeg2PsiParser,**](impeg2psiparser.md)per il recupero delle informazioni PSI.

Questo filtro è progettato per i dispositivi MPEG-2, ad esempio IEEE 1394 videocamere MPEG-2 e dispositivi D-VHS. Per [altre informazioni, vedere Driver MSTape.](mstape-driver.md) Le fonti di trasmissione tv digitale devono usare un filtro TIF per ottenere informazioni sul programma.

## <a name="usage"></a>Utilizzo

È possibile testare il filtro del parser PSI in GraphEdit come segue:

1.  Avviare GraphEdit.
2.  Inserire un'origine di trasporto MPEG-2. I videocamere MPEG-2 e i dispositivi D-VHS vengono visualizzati come "Microsoft AV/C Tape Subunit Device" (Dispositivo sottounità nastro AV/C Microsoft) nella categoria Video Capture Sources (Origini di acquisizione video).
3.  Connessione filtro di origine al filtro MPEG-2 Demultiplexer.
4.  Usare la pagina delle proprietà nel demux per creare un pin di output con un tipo di supporto "MPEG-2 PSI". Questo pin consegnerà le sezioni PAT e PMT.
5.  Usare la pagina delle proprietà demux per eseguire il mapping dei 0x00 PID al pin di output. Impostare il tipo di contenuto su "MPEG2 PSI Sections" (Sezioni PSI MPEG2).
6.  Connessione pin di output demux al parser PSI, come illustrato nel diagramma seguente.

    ![Grafico del filtro del parser psi](images/psi-parser.png)

7.  Eseguire il grafo per eseguire il feed dei dati PSI al filtro del parser PSI. Durante la decodifica delle sezioni PAT, il filtro esegue automaticamente il mapping dei PIN PMT allo stesso pin di output sul demux, in modo che riceva le sezioni PMT.
8.  Usare la pagina delle proprietà Parser PSI per selezionare un numero di programma. L'elenco dei flussi elementari nella pagina delle proprietà mostrerà il PID e il tipo di flusso associati a ogni flusso elementare nel programma selezionato. La pagina delle proprietà è progettata per riconoscere i tipi di flusso definiti in ISO/IEC 13818-1.
9.  Immettere il numero PID audio nella casella **di modifica PID audio** e il numero PID video nella casella di modifica **PID** video.
10. Fare clic **sul pulsante Visualizza** programma. Il parser PSI configurerà i pin di output sul demux in modo che corrispondano alle informazioni del flusso del programma ed eseguirà il rendering dei pin.

> [!Note]  
> La pagina delle proprietà parser PSI viene fornita per semplificare i test e fornire codice di esempio che configura il demultiplexer MPEG-2. Non è consigliabile usare le applicazioni. Le applicazioni devono configurare il demux a livello di codice.

 

Per usare il filtro del parser PSI in un'applicazione, iniziare creando il grafico dei filtri dall'origine MPEG-2 al demux MPEG-2. Il codice per questo passaggio non viene visualizzato qui, perché la configurazione esatta del grafo dipenderà dall'origine.

Creare quindi un pin di output sul demux per i dati PSI. Eseguire il mapping 0x00 PID, riservato per le sezioni PAT, a questo pin, come illustrato nel codice seguente:


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



Per altre informazioni, vedere [Using the MPEG-2 Demultiplexer (Uso del demultiplexer MPEG-2).](using-the-mpeg-2-demultiplexer.md)

Aggiungere il filtro del parser PSI al grafo e connetterlo al pin di output sul demux. Eseguire una query sul parser PSI per [**l'interfaccia IMpeg2PsiParser.**](impeg2psiparser.md) Eseguire ora il grafico e attendere gli eventi EC \_ PROGRAM \_ CHANGED, che segnalano una nuova sezione PAT o PMT. Questo evento è un evento personalizzato definito dal filtro del parser PSI. Quando si riceve un evento EC PROGRAM CHANGED, è possibile ottenere le informazioni PSI disponibili \_ \_ chiamando i metodi **IMpeg2PsiParser.** Questa sezione descrive i metodi che saranno necessari più spesso.

Per ottenere il numero di programmi, usare il [**metodo IMpeg2PsiParser::GetCountOfPrograms:**](impeg2psiparser-getcountofprograms.md)


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Per ottenere il numero di programma per un programma specifico, usare il [**metodo IMpeg2PsiParser::GetRecordProgramNumber:**](impeg2psiparser-getrecordprogramnumber.md)


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



Il numero di programma viene usato per ottenere le voci PMT per i singoli programmi. Per ottenere il numero di flussi elementari in un programma, usare il [**metodo GetCountOfElementaryStreams:**](impeg2psiparser-getcountofelementarystreams.md)


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Per ogni flusso elementare, il metodo [**IMpeg2PsiParser::GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) restituisce il PID e il metodo [**IMpeg2PsiParser::GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) restituisce il tipo di flusso:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



Il PID e il tipo di flusso consentono di configurare nuovi pin di output nel demultiplexer MPEG-2. Questa operazione può richiedere una certa conoscenza dell'origine originale. Ad esempio, ISO/IEC 13818-1 definisce i tipi di flusso da 0x80 a 0xFF come "privato dell'utente", ma altri standard basati su MPEG-2 possono assegnare altri significati a questi tipi.

Il demultiplexer MPEG-2 può creare nuovi pin e nuovi mapping PID mentre il grafo è in esecuzione, ma è necessario arrestare il grafo per connettere i segnaposto.

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Questo esempio viene installato nel percorso seguente: *\[ SDK Root \]* Samples Multimedia DirectShow Filters \\ \\ \\ \\ \\ PSIParser.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> </dl>

 

 
