---
description: Questo argomento descrive come rilevare la perdita di un dispositivo quando si usa un dispositivo di acquisizione video.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Gestione della perdita di dispositivi video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d083ebeb1203b0bba49a63745f62a4dff6b231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308771"
---
# <a name="handling-video-device-loss"></a><span data-ttu-id="85706-103">Gestione della perdita di dispositivi video</span><span class="sxs-lookup"><span data-stu-id="85706-103">Handling Video Device Loss</span></span>

<span data-ttu-id="85706-104">Questo argomento descrive come rilevare la perdita di un dispositivo quando si usa un dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="85706-104">This topic describes how to detect device loss when using a video capture device.</span></span> <span data-ttu-id="85706-105">Contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="85706-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="85706-106">Registra per la notifica del dispositivo</span><span class="sxs-lookup"><span data-stu-id="85706-106">Register For Device Notification</span></span>](#register-for-device-notification)
-   [<span data-ttu-id="85706-107">Ottenere il collegamento simbolico del dispositivo</span><span class="sxs-lookup"><span data-stu-id="85706-107">Get the Symbolic Link of the Device</span></span>](#get-the-symbolic-link-of-the-device)
-   [<span data-ttu-id="85706-108">Gestisci \_ DEVICECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="85706-108">Handle WM\_DEVICECHANGE</span></span>](/windows)
-   [<span data-ttu-id="85706-109">Annulla registrazione per notifica</span><span class="sxs-lookup"><span data-stu-id="85706-109">Unregister For Notification</span></span>](#unregister-for-notification)
-   [<span data-ttu-id="85706-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85706-110">Related topics</span></span>](#related-topics)

## <a name="register-for-device-notification"></a><span data-ttu-id="85706-111">Registra per la notifica del dispositivo</span><span class="sxs-lookup"><span data-stu-id="85706-111">Register For Device Notification</span></span>

<span data-ttu-id="85706-112">Prima di iniziare l'acquisizione dal dispositivo, chiamare la funzione [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) per registrarsi per le notifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85706-112">Before you start capturing from the device, call the [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) function to register for device notifications.</span></span> <span data-ttu-id="85706-113">Eseguire la registrazione per la classe del dispositivo di **\_ acquisizione KSCATEGORY** , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="85706-113">Register for the **KSCATEGORY\_CAPTURE** device class, as shown in the following code.</span></span>


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



## <a name="get-the-symbolic-link-of-the-device"></a><span data-ttu-id="85706-114">Ottenere il collegamento simbolico del dispositivo</span><span class="sxs-lookup"><span data-stu-id="85706-114">Get the Symbolic Link of the Device</span></span>

<span data-ttu-id="85706-115">Enumerare i dispositivi video nel sistema, come descritto in [enumerazione dei dispositivi di acquisizione video](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="85706-115">Enumerate the video devices on the system, as described in [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span> <span data-ttu-id="85706-116">Scegliere un dispositivo dall'elenco e quindi eseguire una query sull'oggetto attivazione per il [ \_ tipo di \_ origine attributo MF DEVSOURCE VidCap attributo di \_ \_ \_ \_ \_ collegamento simbolico](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="85706-116">Choose a device from the list, and then query the activation object for the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute, as shown in the following code.</span></span>


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



## <a name="handle-wm_devicechange"></a><span data-ttu-id="85706-117">Gestisci \_ DEVICECHANGE WM</span><span class="sxs-lookup"><span data-stu-id="85706-117">Handle WM\_DEVICECHANGE</span></span>

<span data-ttu-id="85706-118">Nel ciclo di messaggi, ascoltare i messaggi [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="85706-118">In your message loop, listen for [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) messages.</span></span> <span data-ttu-id="85706-119">Il parametro del messaggio *lParam* è un puntatore a una struttura [**HDR per dev \_ broadcast \_**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="85706-119">The *lParam* message parameter is a pointer to a [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span>


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



<span data-ttu-id="85706-120">Confrontare quindi il messaggio di notifica del dispositivo con il collegamento simbolico del dispositivo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="85706-120">Next, compare the device notification message against the symbolic link of your device, as follows:</span></span>

1.  <span data-ttu-id="85706-121">Controllare il **membro \_ DeviceType di dbch** della struttura dello [**sviluppatore \_ broadcast \_ HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="85706-121">Check the **dbch\_devicetype** member of the [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="85706-122">Se il valore è **DBT \_ DEVTYP \_ DEVICEINTERFACE**, eseguire il cast del puntatore della struttura a una struttura [**\_ \_ DEVICEINTERFACE dev broadcast**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) .</span><span class="sxs-lookup"><span data-stu-id="85706-122">If the value is **DBT\_DEVTYP\_DEVICEINTERFACE**, cast the structure pointer to a [**DEV\_BROADCAST\_DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) structure.</span></span>
2.  <span data-ttu-id="85706-123">Confrontare il membro **DBCC \_ Name** della struttura con il collegamento simbolico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85706-123">Compare the **dbcc\_name** member of this structure to the symbolic link of the device.</span></span>


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



## <a name="unregister-for-notification"></a><span data-ttu-id="85706-124">Annulla registrazione per notifica</span><span class="sxs-lookup"><span data-stu-id="85706-124">Unregister For Notification</span></span>

<span data-ttu-id="85706-125">Prima della chiusura dell'applicazione, chiamare [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) per annullare la registrazione per le notifiche del dispositivo/</span><span class="sxs-lookup"><span data-stu-id="85706-125">Before the application exits, call [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) to unregister for device notifications/</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="85706-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85706-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85706-127">Enumerazione dei dispositivi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="85706-127">Enumerating Video Capture Devices</span></span>](enumerating-video-capture-devices.md)
</dt> <dt>

[<span data-ttu-id="85706-128">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="85706-128">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
