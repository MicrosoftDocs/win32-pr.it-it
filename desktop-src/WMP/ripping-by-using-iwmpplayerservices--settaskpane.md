---
title: Copia da CD con IWMPPlayerServices::setTaskPane
description: Copia da CD con IWMPPlayerServices::setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player,ripping CD
- Windows Media Player a oggetti, ripping CD
- modello a oggetti, ripping CD
- Windows Media Player ActiveX, ripping CD
- ActiveX controllo, ripping CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, ripping CD
- Windows Media Player Mobile, ripping CD
- Ripping cd, interfaccia IWMPPlayerServices setTaskPane
- ripping di CD, interfaccia IWMPPlayerServices setTaskPane
- Interfaccia IWMPPlayerServices setTaskPane
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2abf53d29284b5da629598e6f23d6dcae78c69c60c23ba07f30445d5252845e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569834"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a>Ripping tramite IWMPPlayerServices::setTaskPane

> [!Note]  
> Questa sezione documenta una funzionalità dei controlli Windows Media Player Serie 9 Windows Media Player 10 ActiveX. È consigliabile usare **l'interfaccia IWMPCdromRip** con le versioni successive. Vedere [Interfaccia IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).

 

È possibile usare il controllo Windows Media Player serie 9 o successive per copiare tracce CD nel computer dell'utente. Questo processo è denominato *ripping* di . A tale scopo, è necessario incorporare il controllo Windows Media Player in modalità remota. Per altre informazioni sulla modalità remota, vedere [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).

Per avviare il processo di ripping, chiamare [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane)passando CopyFromCD? AutoCopy:*valore id* per il parametro *bstrTaskPane,* dove *id* è l'indice dell'unità CD da cui copiare. Questo indice corrisponde all'indice di **un oggetto Cdrom** nell'interfaccia **IWMPCdromCollection** o nell'evento **CdromMediaChange.**

Il codice di esempio seguente è una funzione che avvia il processo di copia di un CD dall'unità CD identificata dall'indice zero. La funzione usa la variabile membro seguente:


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



Il codice seguente illustra il corpo della funzione :


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



Visualizzazione dello stato per l'utente

Quando si esegue la copia da un CD, è possibile recuperare una stringa contenente informazioni sullo stato dell'operazione di copia. A tale scopo, è necessario recuperare prima una playlist contenente elementi multimediali che rappresentano le tracce CD chiamando [IWMPCdrom::get \_ playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist). Come nell'esempio precedente, il codice di esempio seguente funziona con l'indice dell'unità CD zero. Archivia la playlist recuperata nella variabile membro seguente:


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



Il codice seguente illustra il corpo della funzione :


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



Gestire quindi [l'evento IWMPEvents::MediaChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) Questo evento si verifica quando viene derubata una traccia CD. Il **puntatore IDispatch** passato al gestore eventi punta all'interfaccia **IWMPMedia** per la traccia CD. Chiamare **QueryInterface** tramite **IDispatch per** recuperare il puntatore a **IWMPMedia.**

Per rilevare quale traccia CD viene decritto, confrontare il puntatore **IWMPMedia** dell'evento con gli elementi multimediali nella playlist cd chiamando [IWMPMedia::get \_ isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).

Chiamare [IWMPMedia::getItemInfo,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)passando la stringa "Status" come nome dell'elemento. **Lo** stato è un attributo temporaneo impostato Windows Media Player elementi multimediali mentre vengono decompressi da CD. non è disponibile nella libreria.

Il codice di esempio seguente mostra un **gestore dell'evento MediaChange.**


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

[**Guida al controllo del giocatore**](player-control-guide.md)
</dt> <dt>

[**Ripping tramite l'interfaccia IWMPCdromRip**](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




