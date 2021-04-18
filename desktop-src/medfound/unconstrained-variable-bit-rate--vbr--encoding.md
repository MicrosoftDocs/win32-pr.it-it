---
description: Codifica della velocità in bit variabile non vincolata
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Codifica della velocità in bit variabile non vincolata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310181"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a>Codifica della velocità in bit variabile non vincolata

Nella modalità di codifica VBR (variable bit rate) non vincolata, il contenuto viene codificato in base alla massima qualità possibile mantenendo una velocità in bit specificata.

La codifica VBR non vincolata usa due sessioni di codifica. Quando si usa la codifica VBR non vincolata, si specifica una velocità in bit per il flusso, come si farebbe con la [codifica della velocità in bit costante](constant-bit-rate-encoding.md). Tuttavia, il codificatore usa questo valore solo come velocità in bit media per il flusso e codifica in modo che la qualità sia il più elevata possibile mantenendo la media. I singoli campioni prodotti dal codificatore variano in base alle dimensioni senza limiti di buffer espliciti. Tuttavia, la velocità in bit media durante la sessione di codifica e la durata del flusso non devono superare il valore specificato dall'utente. La velocità in bit effettiva in qualsiasi punto del flusso codificato può variare considerevolmente dal valore medio. Non viene impostata una finestra del buffer per la codifica VBR non vincolata. Al contrario, il codificatore calcola la dimensione della finestra del buffer necessaria in base ai requisiti degli esempi codificati. Ciò significa che non esiste alcun limite per le dimensioni dei singoli campioni nel flusso, purché la velocità in bit media sia minore o uguale al valore impostato.

Il vantaggio della codifica VBR non vincolata consiste nel fatto che il flusso compresso ha la qualità massima possibile rimanendo all'interno di una larghezza di banda media prevedibile. Usare questa impostazione quando è necessario specificare una larghezza di banda, ma le fluttuazioni intorno alla larghezza di banda specificata sono accettabili; ad esempio, per i file locali o solo per il download.

Lo svantaggio di questa modalità di codifica è che il codificatore può impostare la finestra del buffer su qualsiasi valore necessario dopo la codifica, senza alcun controllo sulle dimensioni del buffer. Nella maggior parte dei casi, se non si è interessati alla dimensione del buffer o alla coerenza di utilizzo della larghezza di banda, è consigliabile usare la [codifica della velocità in bit della variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md) .

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a>Configurazione del codificatore per VBR non vincolato

La configurazione del codificatore viene impostata tramite i valori delle proprietà. Queste proprietà sono definite in wmcodecdsp. h. Prima di negoziare il tipo di supporto di output, è necessario impostare le proprietà di configurazione nel codificatore. Per informazioni su come impostare le proprietà nel codificatore, vedere [configurazione del codificatore](configuring-the-encoder.md). In base ai valori di proprietà specificati, è possibile enumerare i tipi di output VBR supportati e selezionare quello richiesto nel codificatore [Media Foundation trasformazione](media-foundation-transforms.md) (MFT) in base alla velocità media in bit.

Nell'elenco seguente vengono illustrate le proprietà che è necessario impostare per questo tipo di codifica:

-   Specificare la modalità di codifica VBR impostando la \_ Proprietà MFPKEY VBRENABLED su Variant \_ true.
-   Impostare MFPKEY \_ PASSESUSED su 2 perché la modalità VBR non vincolata usa due sessioni di codifica.
-   Durante l'enumerazione del tipo di supporto di output, controllare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) (per i flussi video) dei tipi di supporti di output disponibili. Scegliere un tipo di supporto di output con la velocità in bit media più vicina alla velocità in bit media desiderata che il codificatore deve gestire nel contenuto codificato. Per ulteriori informazioni sulla selezione del tipo di supporto di output, vedere [Media Type Negotiation sul codificatore](media-type-negotiation-on-the-encoder.md).

Per ottenere il valore della finestra del buffer impostato dal codificatore, chiamare **IWMCodecLeakyBucket:: GetBufferSizeBits**, definito in wmcodecifaces. h e wmcodecdspuuid. lib, dopo la sessione di codifica. Per aggiungere il supporto VBR non vincolato per i flussi, è necessario impostare questo valore nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valori di bucket a perdita media) nell'oggetto di configurazione del flusso durante la configurazione del profilo ASF.

Il codice seguente modifica il metodo SetEncodingType della classe di esempio CEncoder per configurare la modalità VBR non vincolata. Per informazioni su questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md). Per informazioni sulle macro helper usate in questo esempio, vedere uso degli esempi di codice Media Foundation.


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
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

 

 



