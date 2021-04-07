---
description: Linee guida di implementazione per la serializzazione delle impostazioni di IWICDevelopRaw
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Linee guida di implementazione per la serializzazione delle impostazioni di IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48cdc78f68e6d63ee7870b9296ae4cfa4f85547a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758294"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Linee guida di implementazione per la serializzazione delle impostazioni di IWICDevelopRaw

L'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) espone le impostazioni che possono essere utilizzate dall'applicazione per modificare l'elaborazione dell'immagine non elaborata. Le impostazioni devono essere serializzate in modo che vengano mantenute tra le sessioni. Sebbene questa operazione possa essere eseguita in diversi modi, è consigliabile codificare i dati in modo coerente con altri metadati.

Di seguito sono riportate alcune linee guida generali per l'implementazione:

-   Tutte le impostazioni effettuate tramite [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , ad esempio rotazione o bilanciamento del bianco, devono evitare la sovrascrittura delle impostazioni della fotocamera o dei dati "come-shot", a meno che il tag non venga comunemente utilizzato come "impostazione corrente". Ad esempio, è possibile usare i tag di orientamento EXIF per la rotazione permanente.
-   È preferibile non dover salvare l'intero file (inclusi i dati del pixel mosaico) ogni volta che viene richiesta la serializzazione delle impostazioni di [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .
-   Il processo di serializzazione delle impostazioni di [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) seguirà in genere questo ordine di eventi. L'applicazione:

    1.  Crea un'istanza di un [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) in un file non elaborato.
    2.  Chiama [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) per ottenere un [**IWICBITMAPFRAMEDECODE**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) per il frame non elaborato.
    3.  Chiama QueryInterface sull'interfaccia IWICBitmapFrameDecode per l'interfaccia IWICDevelopRaw.
    4.  Chiama [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), che restituisce un'interfaccia IPropertyBag2 con tutte le proprietà correnti archiviate.

        A questo punto del processo, l'obiettivo è quello di serializzare le impostazioni nell'interfaccia IPropertyBag2 nel file non elaborato. A tale scopo, è necessario ruotare un codificatore e così via, che viene descritto in dettaglio nei passaggi seguenti.

    5.  Crea un [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) per il file non elaborato.
    6.  Chiama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), passando un nuovo flusso (vuoto) da codificare.
    7.  Chiama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) per creare un nuovo IWICBitmapFrameEncode per il frame non elaborato.
    8.  Chiama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)e passa l'interfaccia IPropertyBag2 del passaggio 4.
    9.  Chiama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) con [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) dal frame dell'immagine non elaborata del decodificatore.
    10. Chiama [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). Il codec serializza quindi le proprietà in IPropertyBag2 dal passaggio 8 al file. Il metodo più comune per la serializzazione delle proprietà si presuppone che vengano scritti come metadati nel file.
    11. Chiama [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Chiama IStream:: commit nel flusso nel passaggio 6.

    Le impostazioni vengono serializzate nel file.

    Questo metodo implica il costo della riscrittura dell'intero file non elaborato ogni volta che vengono serializzate le impostazioni. Questa operazione può essere evitata se si implementa [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) o se il formato di file di immagine supporta XMP o EXIF, perché WIC fornisce [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) per entrambi questi formati. Inoltre, se il codec scrive le modifiche alla fine del file di immagine, l'intero file di immagine non verrà riscritto.

-   I set di parametri vengono caricati dallo stato serializzato quando l'applicazione imposta l'enumerazione [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) nel metodo [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) . Il flag [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) fa riferimento al set di parametri Last-saved, quindi un carico con questo flag dovrebbe comportare il ripristino dei parametri per l'ultimo stato salvato.
-   Al caricamento iniziale è necessario caricare il set di parametri Last-saved, se disponibile. In caso contrario, le impostazioni "As-shot" devono essere usate come impostazioni predefinite nelle variabili di interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . È anche possibile caricare queste impostazioni come-shot usando il flag [**WICRawParameterSet. WICAsShotParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) .
-   L'identificatore [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) è progettato per rappresentare un'impostazione "auto". In progettazione codec è possibile scegliere uno degli approcci seguenti per impostare i parametri [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quando viene effettuata questa impostazione:

    -   Eseguire un'ottimizzazione algoritmica di alcuni parametri, ad esempio l'esposizione o il colore. Questo è il modo in cui le funzioni automatiche negli editor di immagini tipiche sono basate principalmente sull'analisi dei dati in pixel.
    -   Impostare le impostazioni della fotocamera in modo analogo al comportamento di un'impostazione automatica. Questa operazione è utile se l'immagine è stata scattata in un'impostazione manuale e consente all'utente di eseguire l'override delle impostazioni manuali.
    -   Non eseguire alcuna operazione. Non è necessario impostare tutti i controlli quando è selezionata l'opzione auto ed è possibile lasciare invariate le impostazioni.

La raccolta foto di Windows Vista e gli strumenti di modifica della raccolta foto di Windows Live e altre applicazioni di modifica usano il caricamento automatico dei parametri [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quando l'utente seleziona correzione automatica per tutte le normali regolazioni del controllo codec, ad esempio il colore e l'esposizione, per ottenere risultati ottimali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida per WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



