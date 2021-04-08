---
title: Abilitazione di PnP per i dispositivi
description: Abilitazione di PnP per i dispositivi
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media Gestione dispositivi, dispositivi PnP
- Dispositivi Gestione dispositivi, PnP
- Guida per programmatori, dispositivi PnP
- provider di servizi, dispositivi PnP
- creazione di provider di servizi, dispositivi PnP
- Dispositivi PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855890"
---
# <a name="enabling-pnp-for-devices"></a>Abilitazione di PnP per i dispositivi

Windows Media Gestione dispositivi monitora le notifiche relative all'arrivo e alla rimozione dei dispositivi che annunciano un'interfaccia del dispositivo lettore audio portatile. All'arrivo di un dispositivo di questo tipo, Windows Media Gestione dispositivi esegue una query su un parametro di dispositivo denominato *WMDMSPCLSID* per l'ID di classe del provider di servizi responsabile del dispositivo. Windows Media Gestione dispositivi chiama [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) su questo provider di servizi per creare un oggetto dispositivo, esposto all'applicazione come oggetto [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .

Un provider di servizi può gestire dispositivi PnP o dispositivi non PnP. non è in grado di gestire entrambi i tipi.

Per consentire a un dispositivo di usare il meccanismo precedente (e quindi abilitare le notifiche di arrivo e rimozione per il dispositivo in Windows Media Gestione dispositivi applicazioni), devono essere soddisfatti i requisiti seguenti:

-   Il driver di dispositivo di questo dispositivo deve annunciare l'interfaccia del dispositivo Windows Media Gestione dispositivi Portable Audio Player. Il GUID per questa interfaccia del dispositivo è definito come segue:

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Un dispositivo non deve annunciare questa interfaccia se il dispositivo annuncia l'interfaccia del volume (definita come VolumeClassGuid o GUID \_ DEVINTERFACE \_ volume in winioctl. h). Se il dispositivo annuncia l'interfaccia del volume, è già abilitato per la funzionalità PnP in Windows Media Gestione dispositivi.

     

    -AND/OR-

    È necessario creare una nuova sottochiave del registro di sistema per il provider di servizi nella sottochiave HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Media Gestione dispositivi \\ KnownDevices. Questa chiave deve avere il nome del provider di servizi e deve avere le due voci di \_ valore reg SZ seguenti:

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   Il dispositivo deve avere un parametro di dispositivo denominato WMDMSPCLSID. Il valore di questo parametro deve essere impostato come CLSID del provider di servizi in un formato stringa. Per altre informazioni sui parametri del dispositivo, vedere [parametri del dispositivo](device-parameters.md).

    > [!Note]  
    > Il valore del parametro deve essere CLSID, non il ProgID del provider di servizi.

     

-   Il provider di servizi per questo dispositivo deve implementare l'interfaccia IMDServiceProvider2.
-   La chiave del provider di servizi in HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows Media Gestione dispositivi \\ plugins \\ SP \\ spName deve contenere il valore DWORD seguente
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




