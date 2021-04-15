---
description: L'anti-aliasing della scena completa si riferisce alla sfocatura dei bordi di ogni poligono nella scena in quanto viene rasterizzato in un singolo passaggio. non è necessario alcun secondo passaggio.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Anti-aliasing di Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520913"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Anti-aliasing di Full-Scene (Direct3D 9)

L'anti-aliasing della scena completa si riferisce alla sfocatura dei bordi di ogni poligono nella scena in quanto viene rasterizzato in un singolo passaggio. non è necessario alcun secondo passaggio. L'anti-aliasing della scena completa, quando supportato, interessa solo triangoli e gruppi di triangoli. Non è possibile eseguire l'anti-aliasing delle righe usando i servizi Direct3D. L'anti-aliasing della scena completa viene eseguito in Direct3D usando il campionamento multiplo su ogni pixel. Quando è abilitato il campionamento multiplo, tutti i sottocampionati di un pixel vengono aggiornati in un unico passaggio, ma se usati per altri effetti che coinvolgono più passaggi di rendering, l'applicazione può specificare che solo alcuni sottocampionamenti devono essere interessati da un determinato passaggio di rendering. Questo secondo approccio consente di simulare la sfocatura del movimento, gli effetti sullo stato attivo della profondità dei campi, la sfocatura della reflection e così via.

In entrambi i casi, i vari esempi registrati per ogni pixel vengono combinati e restituiti sullo schermo. Ciò consente di migliorare la qualità dell'immagine dell'anti-aliasing o di altri effetti.

Prima di creare un dispositivo con il metodo [**IDirect3D9:: CreateDevice**](/windows/desktop/api) , è necessario determinare se l'anti-aliasing a scena completa è supportato. A tale scopo, chiamare il metodo [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) , come illustrato nell'esempio di codice riportato di seguito.


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



Il primo parametro che [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accetta è un numero ordinale che indica l'adattatore di visualizzazione su cui eseguire la query. Questo esempio USA D3DADAPTER \_ default per specificare la scheda di visualizzazione principale. Il secondo parametro è un valore del tipo enumerato [**D3DDEVTYPE**](./d3ddevtype.md) , che specifica il tipo di dispositivo. Il terzo parametro specifica il formato della superficie. Il quarto parametro indica a Direct3D se richiedere informazioni sul multisampling a finestra completa (**true**) o sull'anti-aliasing della scena completa (**false**). Questo esempio usa **false** per indicare a Direct3D che è in grado di richiedere l'anti-aliasing della scena completa. L'ultimo parametro specifica la tecnica di campionamento multiplo che si desidera testare. Usare un valore del tipo enumerato di [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) . In questo esempio viene testato per verificare se sono supportati due livelli di multicampionamento.

Se il dispositivo supporta il livello di multicampionamento che si vuole usare, il passaggio successivo consiste nell'impostare i parametri di presentazione compilando i membri appropriati della struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) per creare una superficie di rendering multicampionamento. Successivamente, è possibile creare il dispositivo. Il codice di esempio seguente illustra come configurare un dispositivo con una superficie di rendering multicampionamento.


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



Per usare il campionamento multiplo, il membro SwapEffect del \_ parametro D3DPRESENT deve essere impostato su D3DSWAPEFFECT \_ Ignora.

L'ultimo passaggio consiste nell'abilitare l'anti-aliasing multicampionamento chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e impostando D3DRS \_ MULTISAMPLEANTIALIAS su **true**. Dopo aver impostato questo valore su **true**, a tutti i rendering a cui è applicato il campionamento multiplo. Potrebbe essere necessario abilitare e disabilitare il campionamento multiplo, a seconda di ciò che si sta eseguendo il rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Anti-aliasing](antialiasing.md)
</dt> </dl>

 

 
