---
description: Questo argomento presenta la decodifica progressiva e come usare la decodifica progressiva nelle applicazioni.
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: Cenni preliminari sulla decodifica progressiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a409a337ecd3852a50cb5ca1a410ebd32c7f3226c79aacca20b10733e214fbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118710046"
---
# <a name="progressive-decoding-overview"></a>Cenni preliminari sulla decodifica progressiva

Questo argomento presenta la decodifica progressiva e come usare la decodifica progressiva nelle applicazioni. Fornisce inoltre linee guida per la creazione di codec che supportano la decodifica progressiva.

In questo argomento sono contenute le sezioni seguenti.

-   [Introduzione](#introduction)
-   [Che cos'è la decodifica progressiva?](#what-is-progressive-decoding)
-   [Supporto della decodifica progressiva in Windows 7](#progressive-decoding-support-in-windows-7)
-   [Decodifica progressiva JPEG](#jpeg-progressive-decoding)
-   [Decodifica progressiva PNG/GIF](#pnggif-progressive-decoding)
    -   [Decodifica progressiva PNG](#png-progressive-decoding)
    -   [Decodifica progressiva GIF](#gif-progressive-decoding)
-   [Decodifica progressiva nelle applicazioni](#progressive-decoding-in-applications)
-   [Supporto codec personalizzato per la decodifica progressiva](#custom-codec-support-for-progressive-decoding)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

La decodifica progressiva consente di decodificare ed eseguire il rendering incrementale di parti di un'immagine prima del termine del download dell'intera immagine. Questa funzionalità migliora notevolmente l'esperienza dell'utente durante la visualizzazione di immagini da Internet, perché l'utente non deve attendere il download dell'intera immagine prima di poter iniziare la decodifica. Gli utenti possono visualizzare un'anteprima dell'immagine con i dati disponibili molto prima che venga scaricata l'intera immagine. Questa funzionalità è essenziale per qualsiasi applicazione usata per visualizzare immagini da Internet o da origini dati con larghezza di banda limitata.

Il Windows Imaging Component (WIC) in Windows 7 supporta la decodifica progressiva dei formati di immagine più diffusi, ad esempio JPEG, PNG e GIF. WIC supporta anche tutti i codec non Microsoft abilitati per WIC che implementano la decodifica progressiva. La codifica progressiva non è supportata nella versione corrente di WIC. Questo argomento descrive la decodifica progressiva in Windows 7 e la procedura per abilitare la decodifica progressiva nelle applicazioni.

## <a name="what-is-progressive-decoding"></a>Che cos'è la decodifica progressiva?

La decodifica progressiva è la possibilità di decodificare in modo incrementale parti di un'immagine da un file di immagine incompleto. La decodifica tradizionale richiede un file di immagine completo prima di poter iniziare la decodifica. La decodifica progressiva inizia dopo il download di un livello progressivo di un'immagine. Il decodificatore esegue un passaggio di decodifica sul livello progressivo corrente dell'immagine. Esegue quindi più passaggi di decodifica sull'immagine quando viene scaricato ogni livello progressivo. Ogni passaggio di decodifica rivela più dell'immagine fino a quando l'immagine non viene scaricata e decodificata completamente. Il numero di passaggi necessari per decodificare un'immagine completa dipende dal formato del file di immagine e dal processo di codifica usato per creare l'immagine.

Le immagini devono essere codificate in modo specifico per implementare la decodifica progressiva, ma non tutti i formati di immagine la supportano. L'elenco seguente riepiloga i requisiti per l'uso della decodifica progressiva.

-   Il file di immagine deve supportare la decodifica progressiva. La maggior parte dei formati di immagine non supporta la decodifica progressiva, anche se i formati di immagine più diffusi SONO JPEG, PNG e GIF.
-   Il file di immagine deve essere codificato come immagine progressiva. I file di immagine che non sono stati creati con la codifica delle immagini progressive non possono implementare la decodifica progressiva, anche nei casi in cui il formato di file la supporterebbe in altro modo.
-   Deve essere disponibile un codec che supporta la decodifica progressiva. Se un codec non supporta la decodifica progressiva, un'immagine codificata come immagine progressiva verrà decodificata come immagine tradizionale.

## <a name="progressive-decoding-support-in-windows-7"></a>Supporto della decodifica progressiva in Windows 7

Windows 7 offre codec predefiniti che supportano la decodifica progressiva per i formati di immagine JPEG, PNG e GIF. Ognuno di questi Windows 7 codec esegue più passaggi di decodifica su un'immagine. Ogni passaggio corrisponde a un determinato livello e a una parte dell'immagine decodificata, con la fine di ottenere un'immagine completamente decodificata.

Ogni formato di immagine gestisce la decodifica progressiva in modo diverso. Nella tabella seguente vengono fornite informazioni sul numero di livelli progressivi e sul metodo di decodifica supportato dai formati di Windows 7. 

| Formato immagine | Numero di livelli progressivi supportati | Metodo di decodifica progressiva |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | Definito dall'immagine                       | Risoluzione crescente       |
| PNG          | 7                                      | Interlacciamento                 |
| GIF          | 4                                      | Interlacciamento                 |



 

Inoltre, la decodifica progressiva può essere implementata nei codec fornendo il supporto per interfacce e metodi progressivi. Se la decodifica progressiva non è supportata in un codec, devono essere restituiti i messaggi di errore appropriati se questi metodi vengono chiamati.

## <a name="jpeg-progressive-decoding"></a>Decodifica progressiva JPEG

La decodifica progressiva JPEG presenta i dati delle immagini a risoluzioni sempre più elevate per ogni livello, fino a quando non è disponibile l'immagine a risoluzione completa. Ogni livello dell'immagine è impostato per fornire un livello di risoluzione diverso. Quando diventano disponibili livelli progressivi, l'immagine viene visualizzata con risoluzioni più elevate, fino a quando l'immagine con risoluzione completa non viene risolta.

Il numero di livelli disponibili e la risoluzione impostata a ogni livello dipendono interamente dal file JPEG codificato. Le due immagini seguenti mostrano un esempio di decodifica progressiva JPEG a due livelli progressivi.

![esempi di decodifica progressiva jpeg](graphics/Progressive_JPEG_Comparison.jpg)

L'immagine a sinistra viene decodificata al livello progressivo 0. L'immagine a destra viene decodificata completamente dopo cinque livelli progressivi.

## <a name="pnggif-progressive-decoding"></a>Decodifica progressiva PNG/GIF

La decodifica progressiva PNG e GIF usano un metodo di decodifica progressiva interlacciata. Il processo di decodifica per entrambi i formati è molto simile.

### <a name="png-progressive-decoding"></a>Decodifica progressiva PNG

I file di immagine PNG forniscono sette livelli progressivi per la decodifica, come descritto nella specifica PNG. La decodifica progressiva PNG viene implementata decodificando un modello di pixel specificato in ogni passaggio del decodificatore. Il modello nella tabella seguente della specifica PNG viene replicato nell'intera immagine. Ogni numero rappresenta il livello progressivo in cui verrà decodificato il pixel corrispondente.



|  &nbsp;  |  &nbsp;   |  &nbsp;   |  &nbsp;   |   &nbsp;  |  &nbsp;   |  &nbsp;   | &nbsp;    |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

Dalla tabella precedente è possibile determinare i pixel che verranno decodificati con ogni passaggio del decodificatore. A differenza del codec GIF Windows 7, il codec PNG Windows 7 replica il pixel più a sinistra disponibile su una riga di scansione per popolare i pixel vuoti.

Le immagini seguenti mostrano un esempio del codec di Windows 7 PNG a tre livelli progressivi.

![esempi di decodifica progressiva png](graphics/PNG_Progressive_Comparison.jpg)

L'immagine in alto a sinistra mostra un'immagine PNG decodificata al livello progressivo 0. L'immagine in alto a destra mostra la stessa immagine PNG decodificata al livello progressivo 3. L'immagine inferiore mostra la stessa immagine completamente decodificata dopo 7 livelli progressivi.

### <a name="gif-progressive-decoding"></a>Decodifica progressiva GIF

I file di immagine GIF offrono quattro livelli progressivi per la decodifica, come descritto nella specifica GIF. Ogni passaggio popola determinate righe all'interno di un'immagine, producendo un'immagine completa dopo il quarto passaggio. La tabella seguente della specifica GIF mostra quali righe di analisi vengono decodificate da ogni passaggio del decodificatore. 

| Numero di livello/numero di passaggio | Righe di analisi popolate   | Riga di analisi iniziale |
|---------------------------|------------------------|--------------------|
| 1                         | Ogni ottava riga di analisi | 0                  |
| 2                         | Ogni ottava riga di analisi | 4                  |
| 3                         | Ogni quarta riga di analisi | 2                  |
| 4                         | Ogni seconda riga di analisi | 1                  |



 

Anche se i codec possono specificare il contenuto di pixel vuoti a qualsiasi livello specifico, il codec GIF Windows popola le righe di analisi vuote replicando le righe di analisi popolate sopra la riga di analisi vuota.

## <a name="progressive-decoding-in-applications"></a>Decodifica progressiva nelle applicazioni

L'interfaccia di decodifica progressiva principale è [**l'interfaccia IWICProgressiveLevelControl.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) Per ottenere un riferimento all'interfaccia, eseguire una query su un frame di immagine ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) per **IWICProgressiveLevelControl.** È quindi possibile accedere ai metodi progressivi dall'interfaccia .

Il codice seguente fornisce un esempio per l'uso della decodifica progressiva nelle applicazioni.


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
               if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```



Il codice precedente fornisce le funzionalità di base necessarie per implementare la decodifica progressiva nella maggior parte delle applicazioni. Usando il codice, è possibile accedere ai livelli progressivi quando i dati pixel dell'immagine diventano disponibili. La [**funzione SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel) blocca l'esecuzione fino a quando il livello richiesto non è disponibile.

## <a name="custom-codec-support-for-progressive-decoding"></a>Supporto codec personalizzato per la decodifica progressiva

Gli sviluppatori di codec possono scegliere di implementare [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) se i formati di immagine supportano la decodifica progressiva. Il supporto per la decodifica progressiva non è un requisito per l'individuazione e l'arbitraggio da parte del WiC. Tuttavia, la decodifica progressiva migliora notevolmente l'esperienza utente e l'implementazione deve essere considerata, se possibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Compressione digitale e codifica di immagini Continuous-Tone immagini fisse - Requisiti e linee guida](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[Formato di interscambio di file JPEG](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[Specifica GIF89a](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[Portable Network Graphics (PNG) Specification and Extensions](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 



