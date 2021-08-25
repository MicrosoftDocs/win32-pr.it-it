---
description: L'anti-aliasing a scena completa si riferisce alla sfocatura dei bordi di ogni poligono nella scena quando viene rasterizzata in un singolo passaggio; non è necessario alcun secondo passaggio.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Full-Scene antialiasing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3fdeab18997db57ed1391af97f40f1500e7c326411019ddcb42453e4a68cc7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893991"
---
# <a name="full-scene-antialiasing-direct3d-9"></a>Full-Scene antialiasing (Direct3D 9)

L'anti-aliasing a scena completa si riferisce alla sfocatura dei bordi di ogni poligono nella scena quando viene rasterizzata in un singolo passaggio; non è necessario alcun secondo passaggio. L'anti-aliasing della scena completa, se supportato, influisce solo su triangoli e gruppi di triangoli. Non è possibile eseguire l'antialias delle righe usando i servizi Direct3D. L'anti-aliasing della scena completa viene eseguito in Direct3D usando il multicampionamento in ogni pixel. Quando il multicampionamento è abilitato, tutti i sottocampionamenti di un pixel vengono aggiornati in un unico passaggio, ma quando vengono usati per altri effetti che coinvolgono più passaggi di rendering, l'applicazione può specificare che solo alcuni sottocampionamenti devono essere interessati da un determinato passaggio di rendering. Quest'ultimo approccio consente la simulazione della sfocatura del movimento, degli effetti di messa a fuoco in profondità del campo, della sfocatura reflection e così via.

In entrambi i casi, i vari campioni registrati per ogni pixel vengono sfusi insieme e l'output viene visualizzato sullo schermo. In questo modo è possibile migliorare la qualità dell'immagine dell'anti-aliasing o di altri effetti.

Prima di creare un dispositivo con il metodo [**IDirect3D9::CreateDevice,**](/windows/desktop/api) è necessario determinare se l'anti-aliasing della scena completa è supportato. A tale scopo, chiamare [**il metodo IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) come illustrato nell'esempio di codice seguente.


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



Il primo parametro accettato da [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) è un numero ordinale che indica la scheda di visualizzazione su cui eseguire la query. In questo esempio viene utilizzato D3DADAPTER \_ DEFAULT per specificare la scheda video primaria. Il secondo parametro è un valore del [**tipo enumerato D3DDEVTYPE,**](./d3ddevtype.md) che specifica il tipo di dispositivo. Il terzo parametro specifica il formato della superficie. Il quarto parametro indica a Direct3D se è necessario chiedere informazioni sul multisampling a finestra intera **(TRUE)** o sull'anti-aliasing della scena completa **(FALSE).** Questo esempio usa **FALSE** per indicare a Direct3D che sta indagando sull'anti-aliasing a schermo intero. L'ultimo parametro specifica la tecnica di multicampionamento da testare. Usare un valore del [**tipo enumerato D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md) Questo esempio verifica se sono supportati due livelli di multicampionamento.

Se il dispositivo supporta il livello di multicampionamento che si vuole usare, il passaggio successivo consiste nell'impostare i parametri di presentazione compilando i membri appropriati della struttura [**PARAMETERS D3DPRESENT \_**](d3dpresent-parameters.md) per creare una superficie di rendering multicampionamento. Successivamente, è possibile creare il dispositivo. Il codice di esempio seguente illustra come configurare un dispositivo con una superficie di rendering multicampionamento.


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



Per usare il multicampionamento, il membro SwapEffect di D3DPRESENT \_ PARAMETER deve essere impostato su D3DSWAPEFFECT \_ DISCARD.

L'ultimo passaggio consiste nell'abilitare l'anti-aliasing multisampling chiamando il metodo [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) e impostando D3DRS \_ MULTISAMPLEANTIALIAS su **TRUE.** Dopo aver impostato questo valore **su TRUE,** a qualsiasi rendering verrà applicato il multicampionamento. Potrebbe essere necessario abilitare e disabilitare il multicampionamento, a seconda dell'elemento di cui si esegue il rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Antialias](antialiasing.md)
</dt> </dl>

 

 
