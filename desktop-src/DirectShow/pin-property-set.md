---
description: Impostare la proprietà Pin
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Impostare la proprietà Pin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d143d980de7f2a634deecb2c3f06509854ac5a50fbe120da279cce3ad97be1e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316101"
---
# <a name="pin-property-set"></a>Impostare la proprietà Pin

Il set di proprietà pin restituisce la categoria del segnaposto per un segnaposto in un filtro. La categoria viene impostata dal filtro quando crea il segnaposto. la categoria indica il tipo di dati che il pin viene recapitato o ricevuto da questo pin.



| Etichetta | Valore |
|-------------------|----------------------|
| GUID set di proprietà | **AMPROPSETID \_ Pin** |



 



| ID proprietà                   | Descrizione                      |
|-------------------------------|----------------------------------|
| **CATEGORIA PIN AMPROPERTY \_ \_** | Specifica la categoria di un segnaposto. |



 

DirectShow definisce le categorie di pin seguenti nel file di intestazione Uuids.h.



| GUID categoria                     | Descrizione                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PIN \_ CATEGORY \_ ANALOGVIDEOIN**  | Pin di input del filtro di acquisizione che accetta l'analogia e lo digitalizza.                                                                                                                                                                                                                                                     |
| **ACQUISIZIONE \_ DI CATEGORIE DI \_ PIN**        | Pin di acquisizione.                                                                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY \_ CC**             | Aggiungere i dati dei sottotitoli codificati dalla riga 21.                                                                                                                                                                                                                                                                      |
| **PIN \_ CATEGORY \_ EDS**            | Aggiunta di Extended Data Services (riga 21, campi pari).                                                                                                                                                                                                                                                            |
| **PIN \_ CATEGORY \_ NABTS**          | Aggiungere i dati di Videotext Standard dell'America del Nord.                                                                                                                                                                                                                                                                   |
| **ANTEPRIMA \_ CATEGORIA \_ PIN**        | Pin di anteprima.                                                                                                                                                                                                                                                                                                            |
| **CATEGORIA \_ PIN \_ ANCORA**          | Segnaposto che fornisce un'immagine fissa. Il pin di acquisizione del filtro deve essere connesso prima che il pin dell'immagine fissa sia connesso.                                                                                                                                                                                                    |
| **TELETEXT \_ CATEGORIA \_ PIN**       | Pin che fornisce teletext (una variante di sottotitoli codificati).                                                                                                                                                                                                                                                                   |
| **PIN \_ CATEGORY \_ TIMECODE**       | Pin che fornisce i dati del timecode.                                                                                                                                                                                                                                                                                            |
| **CATEGORIA \_ DI PIN \_ VBI**            | Aggiungere i dati dell'intervallo di blanking verticale.                                                                                                                                                                                                                                                                          |
| **PIN \_ CATEGORY \_ VIDEOPORT**      | Pin di output video da collegare al pin di input zero nella scheda [Overlay Mixer](overlay-mixer-filter.md).                                                                                                                                                                                                                    |
| **CATEGORIA \_ PIN \_ VIDEOPORT \_ VBI** | Pin da collegare all'allocatore di superficie [VBI,](vbi-surface-allocator.md)il filtro dell'allocatore di superficie VBI necessario per allocare la memoria video corretta per elementi come le sovrimpressione di sottotitoli codificati negli scenari in cui viene usata una porta video. Gli scenari PCI, IEEE 1394 e USB non usano questo filtro. |
| **PINNAME \_ VIDEO \_ CC \_ CAPTURE**   | Pin di sezione hardware per sottotitoli codificati                                                                                                                                                                                                                                                                                  |



 

Questa proprietà è di sola lettura.

### <a name="example-code"></a>Codice di esempio

Il codice seguente illustra come verificare se un pin supporta questo set di proprietà e, in tal caso, come ottenere la categoria del pin:


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
> Questo esempio usa la [funzione SafeRelease](../medfound/saferelease.md) per rilasciare i puntatori a interfaccia.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti dei pin per i filtri di acquisizione](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Set di proprietà](property-sets.md)
</dt> <dt>

[Uso delle categorie di aggiunta](working-with-pin-categories.md)
</dt> </dl>

 

 
