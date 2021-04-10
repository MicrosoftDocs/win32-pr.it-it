---
description: Questa tabella esegue il mapping dei membri di una dichiarazione D3DVERTEXELEMENT9 a un codice FVF.
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: Mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124479"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a>Mapping tra una dichiarazione Direct3D e i codici FVF (Direct3D 9)

Questa tabella esegue il mapping dei membri di una Dichiarazione [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) a un codice FVF.



| Tipo di dati             | Utilizzo                      | Indice di utilizzo | FVF                       |
|-----------------------|----------------------------|-------------|---------------------------|
| \_FLOAT3 D3DDECLTYPE   | \_Posizione D3DDECLUSAGE     | 0           | D3DFVF \_ XYZ               |
| \_Float4 D3DDECLTYPE   | \_Posizione D3DDECLUSAGE    | 0           | \_XYZRHW D3DFVF            |
| D3DDECLTYPE \_ floatn   | \_BLENDWEIGHT D3DDECLUSAGE  | 0           | \_XYZBN D3DFVF             |
| \_UBYTE4 D3DDECLTYPE   | \_BLENDINDICES D3DDECLUSAGE | 0           | D3DFVF \_ XYZB (nWeights + 1) |
| \_FLOAT3 D3DDECLTYPE   | D3DDECLUSAGE \_ normale       | 0           | D3DFVF \_ normale            |
| \_FLOAT1 D3DDECLTYPE   | \_PSIZE D3DDECLUSAGE        | 0           | \_PSIZE D3DFVF             |
| \_D3DCOLOR D3DDECLTYPE | \_Colore D3DDECLUSAGE        | 0           | D3DFVF \_ diffuse           |
| \_D3DCOLOR D3DDECLTYPE | \_Colore D3DDECLUSAGE        | 1           | D3DFVF \_ speculare          |
| \_Float D3DDECLTYPE   | \_TEXCOORD D3DDECLUSAGE     | n           | D3DFVF \_ TEXCOORDSIZEm (n)  |
| \_FLOAT3 D3DDECLTYPE   | \_Posizione D3DDECLUSAGE     | 1           | N/D                       |
| \_FLOAT3 D3DDECLTYPE   | D3DDECLUSAGE \_ normale       | 1           | N/D                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione vertici](vertex-declaration.md)
</dt> </dl>

 

 



