---
description: Linee guida di implementazione per la serializzazione di IWICDevelopRaw Impostazioni
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Linee guida di implementazione per la serializzazione di IWICDevelopRaw Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119b6377fc8b75aa9763e8141e17ef79832a2aef5f010c2783a412cef0133788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709831"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Linee guida di implementazione per la serializzazione di IWICDevelopRaw Impostazioni

[**L'interfaccia IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) espone le impostazioni che l'applicazione può usare per modificare l'elaborazione dell'immagine RAW. Le impostazioni devono essere serializzate in modo che siano persistenti tra le sessioni. Sebbene questa operazione possa essere eseguita in diversi modi, è consigliabile codificare questi dati in modo coerente con altri metadati.

Di seguito sono riportate alcune linee guida generali per l'implementazione:

-   Qualsiasi impostazione effettuata tramite [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (ad esempio rotazione o bilanciamento del bianco) deve evitare di sovrascrivere l'impostazione della fotocamera o i dati "così come sono", a meno che il tag non venga comunemente usato come "impostazione corrente". Ad esempio, i tag di orientamento EXIF possono essere usati per rendere persistente la rotazione.
-   È preferibile non salvare l'intero file (inclusi i dati pixel del mosaico) ogni volta che viene richiesto di serializzare le impostazioni [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
-   Il processo di serializzazione [**delle impostazioni IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) seguirà in genere questo ordine di eventi. L'applicazione:

    1.  Crea [**un'istanza di IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) in un file RAW.
    2.  Chiama [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) per ottenere un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) per il frame RAW.
    3.  Chiama QueryInterface sull'interfaccia IWICBitmapFrameDecode per l'interfaccia IWICDevelopRaw.
    4.  Chiama [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset)che restituisce un'interfaccia IPropertyBag2 con tutte le proprietà correnti archiviate.

        A questo punto del processo, l'obiettivo è serializzare le impostazioni nell'interfaccia IPropertyBag2 nel file RAW. A tale scopo, è necessario creare un codificatore e così via, come descritto in dettaglio nei passaggi seguenti.

    5.  Crea un [**oggetto IWICBitmapEncoder per**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) il file RAW.
    6.  Chiama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Inizializza**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), passando un nuovo flusso (vuoto) da codificare.
    7.  Chiama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) per creare un nuovo IWICBitmapFrameEncode per il frame RAW.
    8.  Chiama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**inizializza e**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)passa l'interfaccia IPropertyBag2 del passaggio 4.
    9.  Chiama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) con [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) dal frame di immagine RAW del decodificatore.
    10. Chiama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). Il codec serializza quindi le proprietà in IPropertyBag2 dal passaggio 8 nel file . Si presuppone che il metodo più comune per serializzare le proprietà sia scrivendole come metadati nel file .
    11. Chiama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Chiama IStream::Commit sul flusso nel passaggio 6.

    Le impostazioni vengono serializzate nel file .

    Questo metodo comporta il costo della riscrittura dell'intero file RAW ogni volta che le impostazioni vengono serializzate. Questo può essere evitato se si implementa [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) o se il formato del file di immagine supporta XMP o EXIF, perché WIC fornisce [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) per entrambi i formati. Inoltre, se il codec scrive modifiche alla fine del file di immagine, non si finisce per riscrivere l'intero file di immagine.

-   I set di parametri vengono caricati dallo stato serializzato quando l'applicazione imposta l'enumerazione [**WICRawParameterSet.WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) nel [**metodo IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) Il flag [**WICRawParameterSet.WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) fa riferimento all'ultimo set di parametri salvato, pertanto un caricamento con questo flag dovrebbe comportare il ripristino dei parametri all'ultimo stato salvato.
-   Al caricamento iniziale, deve essere caricato l'ultimo set di parametri salvato, se disponibile. In caso contrario, è necessario usare le impostazioni "as-shot" come impostazioni predefinite nelle [**variabili dell'interfaccia IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Queste impostazioni predefinite possono essere caricate anche usando il flag [**WICRawParameterSet.WICAsShotParameterSet.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset)
-   [**L'identificatore WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) deve rappresentare un'impostazione "Auto". Il progettista del codec può scegliere uno degli approcci seguenti per impostare i parametri [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quando viene impostata questa impostazione:

    -   Eseguire un'ottimizzazione algoritmica di alcuni parametri, ad esempio l'esposizione o il colore. Questo è il funzionamento di Auto negli editor di immagini tipici e si basa principalmente sull'analisi dei dati pixel.
    -   Impostare le impostazioni della fotocamera in modo simile al comportamento di un'impostazione automatica. Ciò è utile se l'immagine è stata ripresa con un'impostazione manuale e consente all'utente di eseguire l'override delle impostazioni manuali.
    -   Non eseguire alcuna operazione. Non tutti i controlli devono essere impostati quando si seleziona Auto ed è possibile lasciare invariate le impostazioni.

Gli strumenti di modifica Raccolta foto e Raccolta foto di Windows Live di Windows Vista e altre applicazioni di modifica usano il caricamento automatico dei parametri [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quando l'utente seleziona Correzione automatica per tutte le normali regolazioni del controllo del codec, ad esempio il colore e l'esposizione, per ottenere risultati ottimali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



