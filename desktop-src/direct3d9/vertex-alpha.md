---
description: I dati Alpha possono essere forniti nei dati dei vertici. Per abilitare il vertice Alpha, impostare D3DRS \_ DIFFUSEMATERIALSOURCE su D3DMCS \_ COLOR1 in modo che il runtime Direct3D accetti il valore diffuso dal colore diffuso anziché dal materiale.
ms.assetid: 2b0d842d-ee7d-4633-846d-96697153adc7
title: Alfa vertice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f661c013e324a0bf209b4faca41d1974a41e81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123999"
---
# <a name="vertex-alpha-direct3d-9"></a>Alfa vertice (Direct3D 9)

I dati Alpha possono essere forniti nei dati dei vertici. Per abilitare il vertice Alpha, impostare D3DRS \_ DIFFUSEMATERIALSOURCE su D3DMCS \_ COLOR1 in modo che il runtime Direct3D accetti il valore diffuso dal colore diffuso anziché dal materiale.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



Quindi, fornire i valori alfa nel colore diffuso. La funzione AddAlphaToASphere aggiunge Alfa ai vertici di una sfera. Di seguito è riportato un esempio di come fornire le informazioni Alpha alla funzione.


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



Questa è l'aspetto della funzione.


```
 
void AddAlphaToASphere(D3DLVERTEX* pVertices, DWORD dwNumRings, D3DCOLOR lightcolor)
{
    WORD x, y;
    // rings around
    for( y=0; y < dwNumRings; y++ )
        for( x=0; x < (dwNumRings*2)+1; x++ )
            (pVertices++)->color = lightcolor;

    // top and bottom
    (pVertices++)->color = lightcolor;
    (pVertices++)->color = lightcolor;
}
```



AddAlphaToASphere modifica semplicemente il membro di colore di ogni vertice, che è di tipo D3DLVERTEX, per includere le informazioni alfa.

D3DLVERTEX ha un aspetto simile al seguente.


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



Disegno della sfera,


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



Restituisce una sfera trasparente che usa il vertice Alpha.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 



