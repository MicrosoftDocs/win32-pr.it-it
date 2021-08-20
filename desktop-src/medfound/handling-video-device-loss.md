---
description: Questo argomento descrive come rilevare la perdita di dispositivi quando si usa un dispositivo di acquisizione video.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Gestione della perdita di dispositivi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6219518d3018aae5600e66387363bbd71e29e72b83174b370bf25377c8c6b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878953"
---
# <a name="handling-video-device-loss"></a>Gestione della perdita di dispositivi video

Questo argomento descrive come rilevare la perdita di dispositivi quando si usa un dispositivo di acquisizione video. Contiene le sezioni seguenti:

-   [Registrarsi per la notifica del dispositivo](#register-for-device-notification)
-   [Ottenere il collegamento simbolico del dispositivo](#get-the-symbolic-link-of-the-device)
-   [Gestire WM \_ DEVICECHANGE](/windows)
-   [Annullare la registrazione per la notifica](#unregister-for-notification)
-   [Argomenti correlati](#related-topics)

## <a name="register-for-device-notification"></a>Registrarsi per la notifica del dispositivo

Prima di iniziare l'acquisizione dal dispositivo, chiamare la [**funzione RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) per eseguire la registrazione per le notifiche del dispositivo. Eseguire la registrazione per la classe di dispositivo **KSCATEGORY \_ CAPTURE,** come illustrato nel codice seguente.


```C++
#include <Dbt.h>
#include <ks.h>
#include <ksmedia.h>

HDEVNOTIFY  g_hdevnotify = NULL;

BOOL RegisterForDeviceNotification(HWND hwnd)
{
    DEV_BROADCAST_DEVICEINTERFACE di = { 0 };
    di.dbcc_size = sizeof(di);
    di.dbcc_devicetype  = DBT_DEVTYP_DEVICEINTERFACE;
    di.dbcc_classguid  = KSCATEGORY_CAPTURE; 

    g_hdevnotify = RegisterDeviceNotification(
        hwnd,
        &di,
        DEVICE_NOTIFY_WINDOW_HANDLE
        );

    if (g_hdevnotify == NULL)
    {
        return FALSE;
    }

    return TRUE;
}
```



## <a name="get-the-symbolic-link-of-the-device"></a>Ottenere il collegamento simbolico del dispositivo

Enumerare i dispositivi video nel sistema, come descritto in [Enumerazione dei dispositivi di acquisizione video.](enumerating-video-capture-devices.md) Scegliere un dispositivo dall'elenco e quindi eseguire una query sull'oggetto attivazione per l'attributo [MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ SYMBOLIC \_ LINK,](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) come illustrato nel codice seguente.


```C++
WCHAR      *g_pwszSymbolicLink = NULL;
UINT32     g_cchSymbolicLink = 0;

HRESULT GetSymbolicLink(IMFActivate *pActivate)
{
    return pActivate->GetAllocatedString(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
        &g_pwszSymbolicLink,
        &g_cchSymbolicLink
        );
}
```



## <a name="handle-wm_devicechange"></a>Gestire WM \_ DEVICECHANGE

Nel ciclo di messaggi restare in ascolto dei [**messaggi \_ DEVICECHANGE DI WM.**](../devio/wm-devicechange.md) Il *parametro del messaggio lParam* è un puntatore a una struttura DEV BROADCAST [**\_ \_ HDR.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr)


```C++
    case WM_DEVICECHANGE:
        if (lParam != 0)
        {
            HRESULT hr = S_OK;
            BOOL bDeviceLost = FALSE;

            hr = CheckDeviceLost((PDEV_BROADCAST_HDR)lParam, &bDeviceLost);

            if (FAILED(hr) || bDeviceLost)
            {
                CloseDevice();

                MessageBox(hwnd, L"Lost the capture device.", NULL, MB_OK);
            }
        }
        return TRUE;
```



Confrontare quindi il messaggio di notifica del dispositivo con il collegamento simbolico del dispositivo, come indicato di seguito:

1.  Controllare il **membro \_ dbch devicetype** della [**struttura DEV BROADCAST \_ \_ HDR.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) Se il valore è **DBT \_ DEVTYP \_ DEVICEINTERFACE,** eseguire il cast del puntatore della struttura a una [**struttura DEV BROADCAST \_ \_ DEVICEINTERFACE.**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a)
2.  Confrontare il **membro dbcc \_ name** di questa struttura con il collegamento simbolico del dispositivo.


```C++
HRESULT CheckDeviceLost(DEV_BROADCAST_HDR *pHdr, BOOL *pbDeviceLost)
{
    DEV_BROADCAST_DEVICEINTERFACE *pDi = NULL;

    if (pbDeviceLost == NULL)
    {
        return E_POINTER;
    }

    *pbDeviceLost = FALSE;
    
    if (g_pSource == NULL)
    {
        return S_OK;
    }
    if (pHdr == NULL)
    {
        return S_OK;
    }
    if (pHdr->dbch_devicetype != DBT_DEVTYP_DEVICEINTERFACE)
    {
        return S_OK;
    }

    // Compare the device name with the symbolic link.

    pDi = (DEV_BROADCAST_DEVICEINTERFACE*)pHdr;

    if (g_pwszSymbolicLink)
    {
        if (_wcsicmp(g_pwszSymbolicLink, pDi->dbcc_name) == 0)
        {
            *pbDeviceLost = TRUE;
        }
    }

    return S_OK;
}
```



## <a name="unregister-for-notification"></a>Annullare la registrazione per la notifica

Prima della chiusura dell'applicazione, chiamare [**UnregisterDeviceNotification per**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) annullare la registrazione per le notifiche del dispositivo/


```C++
void OnClose(HWND /*hwnd*/)
{
    if (g_hdevnotify)
    {
        UnregisterDeviceNotification(g_hdevnotify);
    }

    PostQuitMessage(0);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md)
</dt> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 
