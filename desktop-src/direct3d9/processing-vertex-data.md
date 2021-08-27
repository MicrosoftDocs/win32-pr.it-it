---
description: L'interfaccia IDirect3DDevice9 supporta l'elaborazione dei vertici sia nel software che nell'hardware.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Elaborazione dei dati dei vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4656aadee8f39c61be438f85ae0829f0b10dac42c7e5c9014b6ba8c164b3257b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118611"
---
# <a name="processing-vertex-data-direct3d-9"></a>Elaborazione dei dati dei vertici (Direct3D 9)

[**L'interfaccia IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) supporta l'elaborazione dei vertici sia nel software che nell'hardware. In generale, le funzionalità del dispositivo per l'elaborazione dei vertici software e hardware non sono identiche. Le funzionalità hardware sono variabili, a seconda della scheda video e del driver, mentre le funzionalità software sono fisse.

I flag seguenti controllano il comportamento di elaborazione dei vertici per il livello di astrazione hardware (HAL) e i dispositivi di riferimento.

-   D3DCREATE \_ SOFTWARE \_ VERTEXPROCESSING
-   D3DCREATE \_ HARDWARE \_ VERTEXPROCESSING
-   D3DCREATE \_ MIXED \_ VERTEXPROCESSING

Specificare uno dei flag di comportamento di elaborazione dei vertici quando si chiama [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice). Il flag in modalità mista consente al dispositivo di eseguire sia l'elaborazione dei vertici software che hardware. È possibile impostare un solo flag di elaborazione dei vertici per un dispositivo alla volta. Si noti che è necessario impostare il flag D3DCREATE HARDWARE VERTEXPROCESSING quando si crea un dispositivo puro \_ \_ (D3DCREATE \_ PUREDEVICE).

Per evitare la doppia funzionalità di elaborazione dei vertici in un singolo dispositivo, è possibile eseguire query solo sulle funzionalità di elaborazione dei vertici hardware in fase di esecuzione. Le funzionalità di elaborazione dei vertici software sono fisse e non è possibile eseguire query in fase di esecuzione.

Il membro VertexProcessingCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) determina le funzionalità di elaborazione dei vertici hardware del dispositivo.

Per l'elaborazione dei vertici software sono supportate le funzionalità seguenti.

-   membro D3DVTXPCAPS \_ DIRECTIONALLIGHTS di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro D3DVTXPCAPS \_ LOCALVIEWER di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   il membro D3DVTXPCAPS \_ MATERIALSOURCE7 di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro POSITIONALLIGHTS D3DVTXPCAPS \_ di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro D3DVTXPCAPS \_ TEXGEN di [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membro TWEENING D3DVTXPCAPS \_ di [D3DVTXPCAPS](d3dvtxpcaps.md)

Nella tabella seguente sono inoltre elencati i valori impostati per i membri della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per un dispositivo in modalità di elaborazione dei vertici software.



| Membro                 | Funzionalità di elaborazione dei vertici software |
|------------------------|-----------------------------------------|
| MaxActiveLights        | Nessuna limitazione                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | 0xffffffff                              |



 

In generale, qualsiasi applicazione associata all'elaborazione dei vertici deve usare un dispositivo HAL. L'elaborazione dei vertici software offre un set garantito di funzionalità di elaborazione dei vertici, tra cui un numero illimitato di luci e il supporto completo per i vertex shader programmabili. È possibile alternare l'elaborazione dei vertici software e hardware in qualsiasi momento quando si usa il dispositivo HAL (che è l'unico tipo di dispositivo che supporta sia l'elaborazione dei vertici hardware che software). L'unico requisito è che i vertex buffer usati per l'elaborazione dei vertici software devono essere allocati nella memoria di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
