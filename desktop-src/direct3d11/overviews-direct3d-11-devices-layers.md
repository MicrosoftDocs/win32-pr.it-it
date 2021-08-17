---
title: Livelli software
description: Il runtime Direct3D 11 è costruito con livelli, a partire dalle funzionalità di base alla base e creando funzionalità facoltative e assistete dallo sviluppatore nei livelli esterni. In questa sezione vengono descritte le funzionalità di ogni livello.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59d0405d53526b8fb0b93e52fd1a53b5c17839f6c58df919bac335b21ad2477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124362"
---
# <a name="software-layers"></a>Livelli software

Il runtime Direct3D 11 è costruito con livelli, a partire dalle funzionalità di base alla base e creando funzionalità facoltative e assistete dallo sviluppatore nei livelli esterni. In questa sezione vengono descritte le funzionalità di ogni livello.

Come regola generale, i livelli aggiungono funzionalità, ma non modificano il comportamento esistente. Ad esempio, le funzioni di base avranno gli stessi valori restituiti indipendentemente dal livello di debug di cui viene creata un'istanza, anche se è possibile fornire un output di debug aggiuntivo se viene creata un'istanza del livello di debug.

Per creare livelli quando viene creato un dispositivo, chiamare [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e specificare uno o più valori [**D3D11 \_ CREATE DEVICE \_ \_ FLAG.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)

Direct3D 11 offre i livelli di runtime seguenti:

-   [Livello principale](#core-layer)
-   [Livello di debug](#debug-layer)
-   [Argomenti correlati](#related-topics)

## <a name="core-layer"></a>Livello principale

Il livello principale esiste per impostazione predefinita. fornendo un mapping molto sottile tra l'API e il driver di dispositivo, riducendo al minimo il sovraccarico per le chiamate ad alta frequenza. Poiché il livello principale è essenziale per le prestazioni, esegue solo la convalida critica. I livelli rimanenti sono facoltativi.

## <a name="debug-layer"></a>Livello di debug

Il livello di debug offre una convalida estesa dei parametri aggiuntivi e della coerenza, ad esempio la convalida del collegamento dello shader e dell'associazione di risorse, la convalida della coerenza dei parametri e la segnalazione di descrizioni degli errori.

Per creare un dispositivo che supporta il livello di debug, è necessario installare DirectX SDK (per ottenere D3D11SDKLayers.dll) e quindi specificare il flag **D3D11 \_ CREATE \_ DEVICE \_ DEBUG** quando si chiama la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o la funzione [**D3D11CreateDeviceAndSwapChain.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) Se si esegue l'applicazione con il livello di debug abilitato, l'applicazione sarà notevolmente più lenta. Tuttavia, per assicurarsi che l'applicazione non presenti errori e avvisi prima di spedirla, usare il livello di debug. Per altre informazioni, vedere Uso [del livello di debug per eseguire il debug delle app.](using-the-debug-layer-to-test-apps.md)


> [!Note]  
> Per Windows 7 con l'aggiornamento della piattaforma per Windows 7 (KB2670838) o Windows 8.x, per creare un dispositivo che supporta il livello di debug, installare Windows Software Development Kit (SDK) per Windows 8.x per ottenere il1SDKLayers.dll D3D11. \_


> [!Note]  
> Per Windows 10, per creare un dispositivo che supporta il livello di debug, abilitare la funzionalità facoltativa "Strumenti di grafica". Passare al pannello Impostazioni, in Sistema, App & funzionalità, Gestisci funzionalità facoltative, Aggiungi una funzionalità e quindi cercare "Strumenti di grafica".


> [!Note]  
> Per informazioni su come eseguire il debug remoto delle app DirectX, vedere [Debug di app DirectX in modalità remota.](/windows/desktop/direct3dtools/debugging-directx-apps-remotely)

 

In alternativa, è possibile abilitare o disabilitare il flag di debug usando il Pannello di controllo [DirectX](/previous-versions//bb219725(v=vs.85)) incluso come parte di DirectX SDK.

Quando il livello di debug elenca le perdite di memoria, restituisce un elenco di puntatori a interfaccia oggetto insieme ai relativi nomi descrittivi. Il nome descrittivo predefinito è " &lt; senza &gt; nome ". È possibile impostare il nome descrittivo usando il [**metodo ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) e il GUID **WKPDID \_ D3DDebugObjectName** presente in D3Dcommon.h. Ad esempio, per assegnare a pTexture il nome SDKLayer mytexture.jpg, usare il codice seguente:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In genere, è consigliabile compilare queste chiamate dalla versione di produzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 