---
description: Quando si usa un vertex shader programmato, gli elementi aggiornati nel buffer dei vertici di destinazione vengono controllati dal programma di funzione shader.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Elaborazione di vertici programmabili (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ee1e781aa811d8d85a8865bdf07a8811e26d027f6d385b40126a8321172a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118591"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Elaborazione di vertici programmabili (Direct3D 9)

Quando si usa un vertex shader programmato, gli elementi aggiornati nel buffer dei vertici di destinazione vengono controllati dal programma di funzione shader. Quando l'applicazione scrive in uno dei registri vertici di destinazione, l'elemento corrispondente all'interno di ogni vertice del vertex buffer di destinazione viene aggiornato. Gli elementi nel vertex buffer di destinazione non scritti nell'applicazione non vengono modificati. [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) avrà esito negativo se l'applicazione scrive in elementi non presenti nel vertex buffer di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex Buffer](vertex-buffers.md)
</dt> </dl>

 

 
