---
description: Quando si usa un vertex shader programmato, gli elementi aggiornati nel buffer del vertice di destinazione sono controllati dal programma di funzione shader.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Elaborazione Vertex programmabile (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304195"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Elaborazione Vertex programmabile (Direct3D 9)

Quando si usa un vertex shader programmato, gli elementi aggiornati nel buffer del vertice di destinazione sono controllati dal programma di funzione shader. Quando l'applicazione scrive in uno dei registri dei vertici di destinazione, viene aggiornato l'elemento corrispondente all'interno di ogni vertice del buffer del vertice di destinazione. Gli elementi nel buffer del vertice di destinazione che non vengono scritti dall'applicazione non vengono modificati. [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) avrà esito negativo se l'applicazione scrive in elementi che non sono presenti nel buffer del vertice di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer vertici](vertex-buffers.md)
</dt> </dl>

 

 
