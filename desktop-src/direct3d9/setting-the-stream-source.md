---
description: "Il metodo IDirect3DDevice9:: SetStreamSource associa un buffer vertex a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive."
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Impostazione dell'origine del flusso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521913"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Impostazione dell'origine del flusso (Direct3D 9)

Il metodo [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) associa un buffer vertex a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive. I riferimenti effettivi ai dati del flusso non si verificano fino a quando non viene chiamato un metodo di disegno, ad esempio [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Un flusso viene definito come una matrice uniforme di dati del componente, dove ogni componente è costituito da uno o più elementi che rappresentano una singola entità, ad esempio posizione, normale, colore e così via. Il parametro stride specifica la dimensione, in byte, del componente.

Il codice seguente illustra l'impostazione dell'origine del flusso e il disegno del relativo contenuto. La \_ variabile g pVB è un LPDIRECT3DVERTEXBUFFER9 che contiene i dati dei vertici.


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



Per ulteriori informazioni su questo codice, vedere l'esercitazione [3: utilizzo di matrici](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitive di rendering](rendering-primitives.md)
</dt> </dl>

 

 
