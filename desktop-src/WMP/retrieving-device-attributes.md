---
title: Recupero degli attributi del dispositivo
description: Recupero degli attributi del dispositivo
ms.assetid: c553d495-d8fc-4483-a3dc-6679c6b9d1f1
keywords:
- Windows Media Player, dispositivi portatili
- Windows Media Player a oggetti, dispositivi portabili
- modello a oggetti, dispositivi portabili
- Windows Media Player ActiveX, dispositivi portatili
- ActiveX, dispositivi portatili
- Windows Media Player controllo ActiveX dispositivi mobili, dispositivi portatili
- Windows Media Player Dispositivi mobili, dispositivi portatili
- dispositivi portatili, recupero di attributi
- attributi, dispositivi portabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e6ac2794782c728de16f23f88e26d1f458258959e1c3e9e7e490cdf7bf6971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995531"
---
# <a name="retrieving-device-attributes"></a>Recupero degli attributi del dispositivo

Windows Media Player archivia le informazioni sui dispositivi connessi al lettore. Alcuni attributi sono disponibili chiamando singoli metodi di **IWMPSyncDevice**, altri possono essere recuperati usando **IWMPSyncDevice::getItemInfo** e altri possono essere recuperati usando entrambe le tecniche.

Nell'esempio di codice seguente un controllo casella di riepilogo viene riempito con gli attributi disponibili per il dispositivo specificato. La prima parte della funzione recupera le proprietà disponibili usando metodi specifici. La seconda parte della funzione recupera i valori degli attributi usando **IWMPSyncDevice::getItemInfo**. Il parametro della *funzione, lIndex*, è l'indice del dispositivo nella matrice di dispositivi personalizzata a cui punta \_ m ppWMPDevices.


```C++
STDMETHODIMP CMainDlg::ShowDeviceAttributes(long lIndex)
{
    HRESULT hr = S_OK;

    if(!m_ppWMPDevices)
        return S_FALSE;

    // Array of attribute names for devices.
    const TCHAR *szDeviceAttributeNames[16] = {
    _T("Connected"),
    _T("FreeSpace"),
    _T("FriendlyName"),
    _T("LastSyncErrorCount"),
    _T("LastSyncNoFitCount"),
    _T("LastSyncTime"),
    _T("Name"),
    _T("SerialNumber"),
    _T("SupportsAudio"),
    _T("SupportsPhoto"),
    _T("SupportsVideo"),
    _T("SyncIndex"),
    _T("SyncItemCount"),
    _T("SyncPercentComplete"),
    _T("SyncRelationship"),
    _T("TotalSpace")};
    
    // Array of device status strings.
    static const TCHAR *szDeviceStatus[6] = {
    _T("Unknown"),
    _T("Partnership exists"),
    _T("Partnership declined by the user"),
    _T("Partnership with another computer or user"),
    _T("Device only supports manual transfer"),
    _T("New device")};

    // Handle to the list box that displays the information.
    HWND hwndStats = GetDlgItem(IDC_STATS);
    CComBSTR bstrStatistics;  // Contains the display string for each property.
    CComBSTR bstrTemp; // Contains the retrieved value for each property.
    // Retrieve a pointer to the current device.
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]);
    VARIANT_BOOL vbIsConnected = VARIANT_FALSE;
    WMPDeviceStatus  wmpDS = wmpdsUnknown;
    
    SendMessage(hwndStats, LB_RESETCONTENT, 0, 0);

    if(NULL == spDevice.p)
    {
        return E_POINTER;
    }
 
    // Status
    spDevice->get_status(&wmpDS);
    bstrStatistics = "Status: ";
    bstrTemp = szDeviceStatus[wmpDS];
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();
    
    // Connected?
    spDevice->get_connected(&vbIsConnected);
    bstrStatistics = "Connected: ";
    bstrTemp = (vbIsConnected == VARIANT_TRUE)?"True":"False";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics));
    bstrTemp.Empty();
    
    // Device ID
    spDevice->get_deviceId(&bstrTemp);
    bstrStatistics = "Device ID: ";
    bstrStatistics += bstrTemp;

    // Calculate the list box width based on text metrics.
    // This assumes Device ID is likely to be the longest string.
    HDC hDC = GetDC();
    SIZE sizeText = {0, 0};
    GetTextExtentPoint32(hDC, (LPCTSTR)COLE2T(bstrStatistics), bstrStatistics.Length(), &sizeText);
    ReleaseDC(hDC);

    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    SendMessage(hwndStats, LB_SETHORIZONTALEXTENT, sizeText.cx, 0);
    bstrTemp.Empty();

    // Friendly name
    spDevice->get_friendlyName(&bstrTemp);
    bstrStatistics = "Friendly name: ";
    bstrStatistics += bstrTemp;
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrTemp.Empty();

    // Skip a line and label the getItemInfo attributes.
    bstrStatistics = "";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 
    bstrStatistics = "--getItemInfo Attributes--";
    SendMessage(hwndStats, LB_ADDSTRING, 0,(LPARAM)(LPCTSTR)COLE2T(bstrStatistics)); 

    // Show the getItemInfo attributes.
    int iArrayBound = sizeof szDeviceAttributeNames / sizeof szDeviceAttributeNames[0];
    for(int i = 0; i < iArrayBound; i++)
    {
        CComBSTR bstrName(szDeviceAttributeNames[i]);
        CComBSTR bstrVal;
        CComBSTR bstrDisplayString;
       
        hr = spDevice->getItemInfo(bstrName, &bstrVal);
  
        if(FAILED(hr))
        {
             bstrVal.Append("Error");
        }  
        
        bstrName.Append(L": ");
        bstrDisplayString.AppendBSTR(bstrName);
        bstrDisplayString += bstrVal;  
 
        SendMessage(hwndStats, LB_ADDSTRING, 0, (LPARAM)(LPCTSTR)COLE2T(bstrDisplayString));
    }    

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Enumerazione dei dispositivi**](enumerating-devices.md)
</dt> <dt>

[**Interfaccia IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)
</dt> <dt>

[**Uso di dispositivi portatili**](working-with-portable-devices.md)
</dt> </dl>

 

 




