---
description: Imposta la proprietà pin
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Imposta la proprietà pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401151"
---
# <a name="pin-property-set"></a>Imposta la proprietà pin

Il set di proprietà pin restituisce la categoria pin per un pin in un filtro. La categoria viene impostata dal filtro durante la creazione del PIN. la categoria indica il tipo di dati che il PIN viene recapitato o riceve da questo pin.



|                   |                      |
|-------------------|----------------------|
| GUID set di proprietà | **\_Pin AMPROPSETID** |



 



| ID proprietà                   | Descrizione                      |
|-------------------------------|----------------------------------|
| **\_categoria pin \_ AMPROPERTY** | Specifica la categoria di un PIN. |



 

DirectShow definisce le categorie di pin seguenti nel file di intestazione UUIDs. h.



| GUID categoria                     | Descrizione                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PIN \_ categoria \_ ANALOGVIDEOIN**  | Pin di input del filtro di acquisizione che accetta analogie e lo Digitalizza.                                                                                                                                                                                                                                                     |
| **\_ \_ blocca acquisizione categoria**        | Pin di acquisizione.                                                                                                                                                                                                                                                                                                            |
| **\_categoria pin \_ CC**             | Pin che fornisce dati di didascalia chiusi dalla riga 21.                                                                                                                                                                                                                                                                      |
| **PIN \_ categoria \_ EDS**            | Pin che fornisce servizi dati estesi (riga 21, anche campi).                                                                                                                                                                                                                                                            |
| **PIN \_ categoria \_ NABTS**          | Pin che fornisce dati standard Videotext nord-americani.                                                                                                                                                                                                                                                                   |
| **\_anteprima categoria \_ pin**        | Pin di anteprima.                                                                                                                                                                                                                                                                                                            |
| **BLOCCA \_ categoria \_ ancora**          | Pin che fornisce un'immagine ancora. Il pin di acquisizione del filtro deve essere connesso prima della connessione del Pin Still-Image.                                                                                                                                                                                                    |
| **\_televideo categoria \_ pin**       | Pin che fornisce il televideo (una variante di didascalia chiusa).                                                                                                                                                                                                                                                                   |
| **Aggiungi \_ \_ timecode categoria**       | Pin che fornisce i dati del timecode.                                                                                                                                                                                                                                                                                            |
| **PIN \_ categoria \_ VBI**            | Pin che fornisce dati dell'intervallo di spazi vuoti verticali.                                                                                                                                                                                                                                                                          |
| **PIN \_ categoria \_ VIDEOPORT**      | Pin di output del video da connettere al pin di input zero nel [mixer della sovrimpressione](overlay-mixer-filter.md).                                                                                                                                                                                                                    |
| **PIN \_ categoria \_ VIDEOPORT \_ VBI** | Pin da connettere a [VBI Surface allocator](vbi-surface-allocator.md), il filtro VBI Surface allocator, necessario per allocare la memoria video corretta per elementi come le sovrimpressioni dei sottotitoli codificati negli scenari in cui viene usata una porta video. Gli scenari PCI, IEEE 1394 e USB non utilizzano questo filtro. |
| **\_acquisizione PINNAME video \_ CC \_**   | Codice PIN per la didascalia di hardware chiuso                                                                                                                                                                                                                                                                                  |



 

Questa proprietà è di sola lettura.

### <a name="example-code"></a>Codice di esempio

Il codice seguente illustra come verificare se un pin supporta questo set di proprietà e, in tal caso, come ottenere la categoria di pin:


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> Questo esempio usa la funzione [SafeRelease](../medfound/saferelease.md) per rilasciare i puntatori a interfaccia.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti PIN per i filtri di acquisizione](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> <dt>

[Utilizzo delle categorie pin](working-with-pin-categories.md)
</dt> </dl>

 

 
