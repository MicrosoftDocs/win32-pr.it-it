---
description: 'In VBR (Peak-Constrained Variable Bit Rate) il contenuto viene codificato in base a una velocità in bit e a valori di picco specificati: una velocità in bit massima e una finestra del buffer di picco.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Peak-Constrained di velocità in bit variabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b97361c6d4ac8cefd33b223157347e450252691cab024e167862f50c7aac0fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737668"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a>Peak-Constrained di velocità in bit variabile

Nella frequenza di bit variabile con vincoli di picco (VBR) il contenuto viene codificato in base a una velocità in bit e a valori di picco *specificati:* una velocità in bit di picco e una finestra del buffer di picco. Questi valori di picco sono detti anche valori *di bucket con perdita di picco.* Il file è codificato in modo da essere conforme a un buffer descritto dai valori di picco, in modo che la velocità in bit media complessiva del flusso sia uguale o inferiore al valore della velocità in bit media specificato.

In genere, la velocità in bit massima è piuttosto elevata. Il codificatore garantisce che il valore della velocità in bit media specificato venga mantenuto per la durata del flusso (velocità in bit media >= (dimensione totale del flusso in bit/durata del flusso in secondi).) Si consideri l'esempio seguente: si configura un flusso con una velocità in bit media di 16.000 bit al secondo, una velocità in bit massima di 48.000 bit al secondo e una finestra di picco del buffer di 3.000 (3 secondi). La dimensione del buffer usato per il flusso è di 144.000 bit (48.000 bit al secondo 3 secondi) come determinato dai valori di \* picco. Il codificatore comprime i dati in modo che siano conformi a tale buffer. Inoltre, la velocità in bit media del flusso deve essere 16.000 o inferiore. Se il codificatore deve creare campioni di grandi dimensioni per gestire un segmento complesso di contenuto, può sfruttare le grandi dimensioni del buffer. Tuttavia, altre parti del flusso devono essere codificate a una velocità in bit inferiore per portare la media al livello specificato. La codifica VBR con limiti di picco è utile per i dispositivi di riproduzione con una capacità del buffer limitata e vincoli di velocità dei dati. Un esempio comune è la codifica usata per i DVD quando la decodifica viene eseguita da un chip in un dispositivo, in cui è necessario considerare le limitazioni hardware.

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a>Configurazione del codificatore per Peak-Constrained VBR

La funzione VBR con vincoli di picco è simile alla funzione [VBR](unconstrained-variable-bit-rate--vbr--encoding.md) non vincolata, in quanto è limitata a una velocità in bit media per la durata del flusso. Inoltre, la funzione VBR con vincoli di picco è conforme a un buffer di picco. Questo buffer viene descritto usando una velocità in bit di picco e una finestra del buffer di picco. Questa modalità usa due passaggi di codifica e offre al codificatore la flessibilità necessaria per codificare singoli campioni rispettando le limitazioni di picco.

La configurazione del codificatore viene impostata tramite i valori delle proprietà. Queste proprietà sono definite in wmcodecdsp.h. Le proprietà di configurazione devono essere impostate sul codificatore prima di negoziare il tipo di supporto di output. Per informazioni su come impostare le proprietà nel codificatore, vedere [Configurazione del codificatore.](configuring-the-encoder.md) In base ai valori di proprietà specificati, è possibile enumerare i tipi di output VBR supportati e selezionare quello richiesto nel codificatore [Media Foundation transform](media-foundation-transforms.md) (MFT) in base alla velocità in bit media.

Per questo tipo di codifica è necessario impostare le proprietà seguenti:

-   Specificare la modalità di codifica VBR impostando la proprietà MFPKEY \_ VBRENABLED su VARIANT \_ TRUE.
-   Impostare MFPKEY PASSESUSED su 2 perché la modalità VBR con limiti di picco \_ usa due passaggi di codifica.
-   Impostare MFPKEY RMAX per specificare la velocità in bit massima e \_ MFPKEY \_ BMAX per specificare la finestra del buffer di picco.
-   Durante l'enumerazione del tipo di supporto di output, controllare l'attributo [**MF \_ MT AUDIO \_ \_ AVG BYTES PER \_ \_ \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o l'attributo [**MF MT \_ \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md) (per i flussi video) dei tipi di supporti di output disponibili e scegliere un tipo di supporto di output con la velocità in bit media più vicina alla velocità in bit media desiderata che si vuole mantenere nel contenuto codificato. Per altre informazioni sulla selezione del tipo di supporto di output, vedere [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).

> [!Note]  
> È consigliabile impostare la velocità in bit massima almeno due volte la velocità in bit media. Impostando la frequenza di picco su un valore inferiore, il codificatore potrebbe codificare il contenuto come CBR a due passi invece che come vbR con limiti di picco.

 

Per ottenere il valore della finestra del buffer impostato dal codificatore, chiamare **IWMCodecLeakyBucket::GetBufferSizeBits**, definito in wmcodecifaces.h, wmcodecdspuuid.lib, dopo la sessione di codifica. Per aggiungere il supporto vbr non vincolato per i flussi, è necessario impostare questo valore nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (valori di bucket con perdita di picco) nell'oggetto di configurazione del flusso durante la configurazione del profilo ASF.

L'esempio di codice seguente modifica il metodo SetEncodingType della classe di esempio CEncoder per configurare la modalità VBR con limiti di picco. Per informazioni su questa classe, vedere Codice di esempio [del codificatore.](encoder-example-code.md) Per informazioni sulle macro helper usate in questo esempio, vedere Using the Media Foundation Code Examples.


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

[Modello di buffer del bucket di perdita](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[Come creare una topologia per la codifica Two-Pass Windows supporti](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



