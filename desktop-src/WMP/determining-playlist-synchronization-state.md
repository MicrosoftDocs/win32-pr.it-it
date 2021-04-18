---
title: Determinazione dello stato di sincronizzazione della playlist
description: Determinazione dello stato di sincronizzazione della playlist
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Media Player di Windows, playlist di sincronizzazione
- Modello a oggetti di Windows Media Player, playlist di sincronizzazione
- modello a oggetti, playlist di sincronizzazione
- Windows Media Player Mobile, playlist di sincronizzazione
- Controllo ActiveX di Windows Media Player, playlist di sincronizzazione
- Controllo ActiveX Windows Media Player Mobile, playlist di sincronizzazione
- Controllo ActiveX, playlist di sincronizzazione
- playlist, sincronizzazione
- playlist di metafile, sincronizzazione
- Playlist di Windows Media Metafile, sincronizzazione
- dispositivi portatili, determinazione dello stato della playlist di sincronizzazione
- playlist di sincronizzazione, stato di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299377"
---
# <a name="determining-playlist-synchronization-state"></a>Determinazione dello stato di sincronizzazione della playlist

Windows Media Player 10 o versioni successive utilizza l'attributo **SyncState** per contenere informazioni sul fatto che un file multimediale digitale specifico sia stato copiato in un dispositivo portatile e, in caso di errore, se la copia non è riuscita perché la memoria del dispositivo non è sufficiente.

Nell'esempio di codice seguente viene creata una funzione che recupera queste informazioni da un file multimediale digitale. La funzione accetta i parametri seguenti:

-   *pMedia*. Puntatore a un'interfaccia **IWMPMedia** che rappresenta il file multimediale digitale da ispezionare.
-   *lPsIndex*. Indice di partnership del dispositivo corrente.
-   *pulOnDevice*. Puntatore a una variabile **Long** che riceve il valore che indica se il file multimediale digitale è stato copiato nel dispositivo.
-   *pulDidNotFit*. Puntatore a una variabile **Long** che riceve il valore che indica se l'operazione di copia non è riuscita perché la memoria del dispositivo non è sufficiente.

Le informazioni contenute nell'attributo **SyncState** sono codificate in modo bit per bit. È possibile osservare come questa funzione viene usata nel codice di esempio nell' [enumerazione degli elementi multimediali](enumerating-the-media-items.md).


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPMedia3::getItemInfoByType**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[**Gestione delle playlist di sincronizzazione**](managing-synchronization-playlists.md)
</dt> <dt>

[**Attributo SyncState**](syncstate-attribute.md)
</dt> </dl>

 

 




