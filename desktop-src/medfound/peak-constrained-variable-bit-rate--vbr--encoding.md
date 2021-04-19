---
description: 'Nella velocità in bit della variabile con vincoli di picco (VBR), il contenuto viene codificato in base a una velocità in bit e a valori di picco specificati: una velocità in bit massima e una finestra del buffer di picco.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Codifica della velocità in bit della variabile Peak-Constrained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309040"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Codifica della velocità in bit della variabile Peak-Constrained

Nella velocità in bit della variabile con vincoli di picco (VBR), il contenuto viene codificato in base a una velocità in bit e a *valori di picco* specificati: una velocità in bit massima e una finestra del buffer di picco. Questi valori di picco sono detti anche *valori di bucket per perdite di picco*. Il file è codificato per essere conforme a un buffer descritto dai valori di picco, in modo che la velocità in bit media complessiva del flusso sia uguale o inferiore al valore di velocità in bit medio specificato.

In genere, la velocità in bit di picco è piuttosto elevata. Il codificatore garantisce che il valore di velocità in bit medio specificato venga mantenuto per la durata del flusso (velocità in bit media >= (dimensione del flusso totale in bit/durata del flusso in secondi)). Si consideri l'esempio seguente: si configura un flusso con una velocità in bit media di 16.000 bit al secondo, una velocità in bit di picco di 48.000 bit al secondo e una finestra buffer di picco di 3.000 (3 secondi). Le dimensioni del buffer utilizzato per il flusso sono di 144.000 bit (48.000 bit al secondo \* 3 secondi) come determinato dai valori di picco. Il codificatore comprime i dati in modo che siano conformi a tale buffer. Inoltre, la velocità in bit media del flusso deve essere inferiore a 16.000. Se il codificatore deve creare campioni di grandi dimensioni per gestire un segmento complesso di contenuto, può sfruttare i vantaggi della dimensione del buffer di grandi dimensioni. Tuttavia, altre parti del flusso devono essere codificate a una velocità in bit più bassa per abbassare la media fino al livello specificato. La codifica VBR con vincoli di picco è utile per la riproduzione di dispositivi con una capacità di buffer finita e vincoli di velocità dati. Un esempio comune è la codifica usata per i DVD quando la decodifica viene eseguita da un chip in un dispositivo, in cui sono presenti limitazioni hardware che devono essere prese in considerazione.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Configurazione del codificatore per Peak-Constrained VBR

Il numero di VBR con vincoli di picco è simile a quello di [VBR non vincolato](unconstrained-variable-bit-rate--vbr--encoding.md) , perché è limitato a una velocità in bit media per la durata del flusso. Inoltre, la funzionalità VBR con vincoli di picco è conforme a un buffer di picco. Questo buffer viene descritto utilizzando una velocità in bit massima e una finestra del buffer di picco. Questa modalità usa due sessioni di codifica e fornisce alla flessibilità del codificatore la modalità di codifica dei singoli campioni rispettando al massimo le limitazioni.

La configurazione del codificatore viene impostata tramite i valori delle proprietà. Queste proprietà sono definite in wmcodecdsp. h. Prima di negoziare il tipo di supporto di output, è necessario impostare le proprietà di configurazione nel codificatore. Per informazioni su come impostare le proprietà nel codificatore, vedere [configurazione del codificatore](configuring-the-encoder.md). In base ai valori di proprietà specificati, è possibile enumerare i tipi di output VBR supportati e selezionare quello richiesto nel codificatore [Media Foundation trasformazione](media-foundation-transforms.md) (MFT) in base alla velocità media in bit.

È necessario impostare il seguente proprietàdei di questo tipo di codifica:

-   Specificare la modalità di codifica VBR impostando la \_ Proprietà MFPKEY VBRENABLED su Variant \_ true.
-   Impostare MFPKEY \_ PASSESUSED su 2 perché la modalità VBR con vincoli di picco usa due sessioni di codifica.
-   Impostare MFPKEY \_ Rmax per specificare la velocità in bit di picco e impostare MFPKEY \_ BMAX per specificare la finestra del buffer di picco.
-   Durante l'enumerazione del tipo di supporto di output, controllare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) (per i flussi video) dei tipi di supporti di output disponibili e scegliere un tipo di supporto di output con la velocità in bit media più vicina alla velocità in bit media desiderata che il codificatore deve gestire nel contenuto codificato. Per ulteriori informazioni sulla selezione del tipo di supporto di output, vedere [Media Type Negotiation sul codificatore](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> È consigliabile impostare la velocità in bit massima su almeno il doppio della velocità in bit media. Impostando la velocità di picco su un valore inferiore, il codificatore può codificare il contenuto come CBR a due passaggi invece che con il picco di VBR.

 

Per ottenere il valore della finestra del buffer impostato dal codificatore, chiamare **IWMCodecLeakyBucket:: GetBufferSizeBits**, definito in wmcodecifaces. h, wmcodecdspuuid. lib, dopo la sessione di codifica. Per aggiungere il supporto VBR non vincolato per i flussi, è necessario impostare questo valore nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (Peak Leaky Bucket Values) nell'oggetto di configurazione del flusso durante la configurazione del profilo ASF.

Nell'esempio di codice seguente viene modificato il metodo SetEncodingType della classe di esempio CEncoder per configurare la modalità VBR con vincoli di picco. Per informazioni su questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md). Per informazioni sulle macro helper usate in questo esempio, vedere uso degli esempi di codice Media Foundation.


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di codifica ASF](asf-encoding-types.md)
</dt> <dt>

[Modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Come creare una topologia per la codifica Two-Pass Windows Media](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



