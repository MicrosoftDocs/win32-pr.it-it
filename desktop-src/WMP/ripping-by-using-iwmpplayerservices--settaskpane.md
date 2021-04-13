---
title: Copia da CD con IWMPPlayerServices::setTaskPane
description: Copia da CD con IWMPPlayerServices::setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, interfaccia setTaskPane di IWMPPlayerServices
- ripping di CDs, interfaccia setTaskPane di IWMPPlayerServices
- Interfaccia setTaskPane di IWMPPlayerServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104472382"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Estrazione tramite IWMPPlayerServices:: setTaskPane

> [!Note]  
> Questa sezione documenta una funzionalità dei controlli ActiveX Windows Media Player 9 e Windows Media Player 10. Si consiglia di usare l'interfaccia **IWMPCdromRip** con versioni successive. Vedere [interfaccia IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).

 

È possibile utilizzare il controllo Windows Media Player 9 Series o versione successiva per copiare tracce di CD nel computer dell'utente. Questo processo è denominato *estrazione*. A tale scopo, è necessario incorporare il controllo Media Player Windows in modalità remota. Per ulteriori informazioni sulla modalità remota, vedere [la pagina relativa alla comunicazione remota del controllo Media Player di Windows](remoting-the-windows-media-player-control.md).

Per avviare il processo di strappo, chiamare [IWMPPlayerServices:: setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passando il CopyFromCD? AutoCopy: valore *ID* per il parametro *bstrTaskPane* , dove *ID* è l'indice dell'unità CD da cui eseguire la copia. Questo indice corrisponde all'indice di un oggetto **CDROM** nell'interfaccia **IWMPCdromCollection** o dell'evento **CdromMediaChange** .

Il codice di esempio seguente è una funzione che avvia il processo di estrazione di un CD dall'unità CD identificata dall'indice zero. La funzione usa la variabile membro seguente:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



Il codice seguente illustra il corpo della funzione:


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



Visualizzazione dello stato dell'utente

Quando si esegue la copia da un CD, è possibile recuperare una stringa contenente informazioni sullo stato relative all'operazione di copia. A tale scopo, è necessario innanzitutto recuperare una playlist contenente elementi multimediali che rappresentano le tracce CD chiamando [IWMPCdrom:: Get \_ playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist). Come nell'esempio precedente, il codice di esempio seguente funziona con l'indice di unità CD zero. Archivia la playlist recuperata nella variabile membro seguente:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



Il codice seguente illustra il corpo della funzione:


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



Quindi, gestire l'evento [IWMPEvents:: MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) . Questo evento si verifica quando viene rilevata una traccia del CD. Il puntatore **IDispatch** passato al gestore eventi punta all'interfaccia **IWMPMedia** per la traccia del CD. Chiamare **QueryInterface** tramite **IDispatch** per recuperare il puntatore a **IWMPMedia**.

Per individuare la traccia del CD da estrarre, confrontare il puntatore **IWMPMedia** dall'evento con gli elementi multimediali nella playlist CD chiamando [IWMPMedia:: Get \_ identico](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).

Chiamare [IWMPMedia:: GetItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passando la stringa "status" come nome dell'elemento. **Lo stato** è un attributo temporaneo impostato da Windows Media Player su elementi multimediali mentre vengono ricopiati dal CD; non è disponibile dalla libreria.

Il codice di esempio seguente mostra un gestore dell'evento **MediaChange** .


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interfaccia IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interfaccia IWMPEvents**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[**Interfaccia IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interfaccia IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[**Interfaccia IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Guida al controllo del lettore**](player-control-guide.md)
</dt> <dt>

[**Ripping mediante l'interfaccia IWMPCdromRip**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




