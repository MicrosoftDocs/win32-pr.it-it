---
description: Il metodo IDirect3DDevice9::SetStreamSource associa un vertex buffer a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive.
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Impostazione dell'origine del flusso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91bd760b23204de2c6ccd313b164ac7536c7db2d3e2da26d7e40b7d98daa60a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044239"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Impostazione dell'origine del flusso (Direct3D 9)

Il metodo [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) associa un vertex buffer a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive. I riferimenti effettivi ai dati del flusso non si verificano fino a quando non viene chiamato un metodo di disegno, ad esempio [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Un flusso è definito come una matrice uniforme di dati del componente, in cui ogni componente è costituito da uno o più elementi che rappresentano una singola entità, ad esempio posizione, normale, colore e così via. Il parametro Stride specifica le dimensioni del componente, in byte.

Il codice seguente illustra l'impostazione dell'origine del flusso e il disegno del relativo contenuto. La variabile \_ pVB g è un LPDIRECT3DVERTEXBUFFER9 che contiene dati sui vertici.


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



Per altre informazioni su questo codice, vedere l'esercitazione seguente: [Esercitazione 3: Uso delle matrici](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive di rendering](rendering-primitives.md)
</dt> </dl>

 

 
