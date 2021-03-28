---
title: Livelli software
description: Il runtime di Direct3D 11 viene costruito con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori nei livelli esterni. In questa sezione vengono descritte le funzionalità di ogni livello.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516804"
---
# <a name="software-layers"></a>Livelli software

Il runtime di Direct3D 11 viene costruito con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori nei livelli esterni. In questa sezione vengono descritte le funzionalità di ogni livello.

Come regola generale, i livelli aggiungono funzionalità, ma non modificano il comportamento esistente. Le funzioni di base, ad esempio, avranno gli stessi valori restituiti indipendentemente dal livello di debug di cui viene creata un'istanza, sebbene sia possibile fornire un output di debug aggiuntivo se viene creata un'istanza del livello debug.

Per creare livelli quando viene creato un dispositivo, chiamare [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) e fornire uno o più valori di [**\_ flag di creazione del \_ dispositivo \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .

Direct3D 11 fornisce i livelli di runtime seguenti:

-   [Livello principale](#core-layer)
-   [Livello di debug](#debug-layer)
-   [Argomenti correlati](#related-topics)

## <a name="core-layer"></a>Livello principale

Il livello principale esiste per impostazione predefinita. fornire un mapping molto sottile tra l'API e il driver di dispositivo, riducendo al minimo l'overhead per le chiamate ad alta frequenza. Poiché il livello principale è essenziale per le prestazioni, viene eseguita solo la convalida critica. I livelli rimanenti sono facoltativi.

## <a name="debug-layer"></a>Livello di debug

Il livello di debug fornisce la convalida estesa di parametri e coerenza, ad esempio la convalida del collegamento shader e dell'associazione di risorse, la convalida della coerenza dei parametri e la segnalazione delle descrizioni degli errori.

Per creare un dispositivo che supporta il livello di debug, è necessario installare DirectX SDK (per ottenere D3D11SDKLayers.dll), quindi specificare il flag di debug per la creazione di un **\_ \_ dispositivo \_ d3d11** quando si chiama la funzione [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o la funzione [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) . Se si esegue l'applicazione con il livello di debug abilitato, l'applicazione sarà sostanzialmente più lenta. Tuttavia, per assicurarsi che l'applicazione sia pulita da errori e avvisi prima della spedizione, utilizzare il livello debug. Per altre informazioni, vedere [uso del livello di debug per eseguire il debug delle app](using-the-debug-layer-to-test-apps.md).


> [!Note]  
> Per Windows 7 con aggiornamento della piattaforma per Windows 7 (KB2670838) o Windows 8. x, per creare un dispositivo che supporta il livello di debug, installare Windows Software Development Kit (SDK) per Windows 8. x per ottenere D3D11 \_1SDKLayers.dll.


> [!Note]  
> Per Windows 10, per creare un dispositivo che supporta il livello di debug, abilitare la funzionalità facoltativa "strumenti di grafica". Passare al pannello impostazioni, in sistema, app & funzionalità, Gestisci funzionalità facoltative, aggiungere una funzionalità, quindi cercare "strumenti di grafica".


> [!Note]  
> Per informazioni su come eseguire il debug di app DirectX in modalità remota, vedere [debug di app DirectX in modalità remota](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).

 

In alternativa, è possibile abilitare o disabilitare il flag di debug usando il [Pannello di controllo DirectX](/previous-versions//bb219725(v=vs.85)) incluso in DirectX SDK.

Quando il livello di debug elenca le perdite di memoria, viene restituito un elenco di puntatori dell'interfaccia oggetto insieme ai relativi nomi descrittivi. Il nome descrittivo predefinito è " &lt; senza nome &gt; ". È possibile impostare il nome descrittivo usando il metodo [**ID3D11DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) e il GUID **WKPDID \_ D3DDebugObjectName** in D3Dcommon. h. Ad esempio, per assegnare un nome a pTexture con il nome SDKLayer mytexture.jpg, usare il codice seguente:


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



In genere, è necessario compilare queste chiamate fuori dalla versione di produzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 