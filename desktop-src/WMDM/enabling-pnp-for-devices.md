---
title: Abilitazione di PnP per i dispositivi
description: Abilitazione di PnP per i dispositivi
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Gestione dispositivi multimediali, dispositivi PnP
- Gestione dispositivi, dispositivi PnP
- guida alla programmazione, dispositivi PnP
- provider di servizi, dispositivi PnP
- creazione di provider di servizi, dispositivi PnP
- Dispositivi PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e574aa0d5462c2fcbb0592e9d3faaf927cd7e5213e6eec3d8e7f016eabfb7abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584999"
---
# <a name="enabling-pnp-for-devices"></a>Abilitazione di PnP per i dispositivi

Windows Gestione dispositivi multimediali monitora le notifiche di arrivo e rimozione dei dispositivi che annunciano un'interfaccia del dispositivo Lettore audio portatile. All'arrivo di un dispositivo di questo tipo, Windows Gestione dispositivi multimediali esegue una query su un parametro del dispositivo denominato *WMDMSPCLSID* per l'ID di classe del provider di servizi responsabile del dispositivo. Windows Gestione dispositivi multimediali chiama [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) su questo provider di servizi per creare un oggetto dispositivo, esposto all'applicazione come [**oggetto IWMDMDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)

Un provider di servizi può gestire dispositivi PnP o dispositivi non PnP; non può gestire entrambi i tipi.

Perché un dispositivo funzioni con il meccanismo precedente e quindi abiliti le notifiche di arrivo e rimozione per il dispositivo nelle applicazioni di Windows Media Device Manager, devono essere soddisfatti i requisiti seguenti:

-   Il driver di dispositivo di questo dispositivo deve annunciare l'Windows dispositivo lettore audio portatile di Gestione dispositivi multimediali. Il GUID per questa interfaccia di dispositivo è definito come:

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Un dispositivo non deve annunciare questa interfaccia se il dispositivo annuncia l'interfaccia volume (definita come VolumeClassGuid o GUID \_ DEVINTERFACE \_ VOLUME in winioctl.h). Se il dispositivo annuncia l'interfaccia del volume, è già abilitato per PnP in Windows Gestione dispositivi multimediali.

     

    -AND/OR-

    È necessario creare una nuova sottochiave del Registro di sistema per il provider di servizi all'interno della sottochiave HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Media Device Manager \_ \\ \\ \\ \\ KnownDevices. Questa chiave deve avere il nome del provider di servizi e deve avere le due voci di valore \_ reg SZ seguenti:

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   Il dispositivo deve avere un parametro del dispositivo denominato WMDMSPCLSID. Il valore di questo parametro deve essere impostato come CLSID del provider di servizi in formato stringa. Per altre informazioni sui parametri del dispositivo, vedere [Parametri del dispositivo.](device-parameters.md)

    > [!Note]  
    > Il valore del parametro deve essere il CLSID, non il ProgID del provider di servizi.

     

-   Il provider di servizi per questo dispositivo deve implementare l'interfaccia IMDServiceProvider2.
-   La chiave del provider di servizi in HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Media Device Manager \_ \\ \\ \\ \\ \\ Plugins SPName deve contenere \\ il valore DWORD seguente
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




