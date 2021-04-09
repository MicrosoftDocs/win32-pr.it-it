---
description: L'interfaccia IDirect3DDevice9 supporta l'elaborazione dei vertici in software e hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Elaborazione dei dati dei vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876818"
---
# <a name="processing-vertex-data-direct3d-9"></a>Elaborazione dei dati dei vertici (Direct3D 9)

L'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) supporta l'elaborazione dei vertici in software e hardware. In generale, le funzionalità del dispositivo per l'elaborazione dei vertici hardware e software non sono identiche. Le funzionalità hardware sono variabili, a seconda della scheda di visualizzazione e del driver, mentre le funzionalità software sono fisse.

I flag seguenti controllano il comportamento di elaborazione dei vertici per i dispositivi HAL (Hardware Abstraction Layer) e di riferimento.

-   D3DCREATE \_ software \_ VERTEXPROCESSING
-   \_VERTEXPROCESSING hardware \_ D3DCREATE
-   D3DCREATE \_ misto \_ VERTEXPROCESSING

Specificare uno dei flag del comportamento di elaborazione dei vertici quando si chiama [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice). Il flag in modalità mista consente al dispositivo di eseguire l'elaborazione dei vertici software e hardware. È possibile impostare un solo flag di elaborazione dei vertici per un dispositivo in un momento qualsiasi. Si noti che \_ \_ è necessario impostare il flag VERTEXPROCESSING hardware D3DCREATE quando si crea un dispositivo puro (D3DCREATE \_ PUREDEVICE).

Per evitare funzionalità di elaborazione di due vertici su un solo dispositivo, è possibile eseguire query sulle funzionalità di elaborazione dei vertici hardware in fase di esecuzione. Le funzionalità di elaborazione dei vertici software sono fisse e non è possibile eseguire query in fase di esecuzione.

Il membro VertexProcessingCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina le funzionalità di elaborazione dei vertici hardware del dispositivo.

Per l'elaborazione di vertici software sono supportate le funzionalità seguenti.

-   membro D3DVTXPCAPS \_ DIRECTIONALLIGHTS di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro D3DVTXPCAPS \_ LOCALVIEWER di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro D3DVTXPCAPS \_ MATERIALSOURCE7 di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro D3DVTXPCAPS \_ POSITIONALLIGHTS di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro D3DVTXPCAPS \_ TEXGEN di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   \_membro di interpolazione D3DVTXPCAPS di [D3DVTXPCAPS](d3dvtxpcaps.md)

Nella tabella seguente sono inoltre elencati i valori impostati per i membri della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per un dispositivo in modalità di elaborazione dei vertici software.



| Membro                 | Funzionalità di elaborazione dei vertici software |
|------------------------|-----------------------------------------|
| MaxActiveLights        | Nessuna limitazione                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | 0xFFFFFFFF                              |



 

In generale, qualsiasi applicazione che è associata all'elaborazione dei vertici deve usare un dispositivo HAL. L'elaborazione dei vertici software fornisce un set garantito di funzionalità di elaborazione vertici, tra cui un numero illimitato di luci e il supporto completo per i vertex shader programmabili. Quando si usa il dispositivo HAL (che è l'unico tipo di dispositivo che supporta l'elaborazione dei vertici hardware e software), è possibile passare da un'elaborazione dei vertici software a un'altra in qualsiasi momento. L'unico requisito è che i buffer vertex usati per l'elaborazione dei vertici software devono essere allocati nella memoria di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
