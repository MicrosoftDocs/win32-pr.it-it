---
description: Come per qualsiasi caratteristica, il driver utilizzato dall'applicazione potrebbe non supportare tutti i tipi di buffering di profondità.
ms.assetid: 8bf022f6-fd97-43f5-ac19-6a75ddb45f5e
title: Esecuzione di query per il supporto del buffer di profondità (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfe7555c1fa0fccddcfcb12ff8bc53f1a0f5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745522"
---
# <a name="querying-for-depth-buffer-support-direct3d-9"></a>Esecuzione di query per il supporto del buffer di profondità (Direct3D 9)

Come per qualsiasi caratteristica, il driver utilizzato dall'applicazione potrebbe non supportare tutti i tipi di buffering di profondità. Controllare sempre le funzionalità del driver. Sebbene la maggior parte dei driver supporti il buffering di profondità basato su z, non tutti supporteranno il buffering basato su w. I driver non hanno esito negativo se si tenta di abilitare uno schema non supportato. Eseguono invece il fallback su un altro metodo di buffering di profondità, o talvolta disabilitano completamente il buffering di profondità, che può comportare il rendering di scene con artefatti di ordinamento estremamente approfonditi.

È possibile verificare il supporto generale per i buffer di profondità eseguendo una query su Direct3D per il dispositivo di visualizzazione che l'applicazione userà prima di creare un dispositivo Direct3D. Se l'oggetto Direct3D segnala che supporta il buffering di profondità, qualsiasi dispositivo hardware creato dall'oggetto Direct3D supporterà il buffer z.

Per eseguire una query per il supporto del buffering di profondità, è possibile usare il metodo [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) , come illustrato nell'esempio di codice seguente.


```
// The following example assumes that pCaps is a valid pointer to an 
// initialized D3DCAPS9 structure
if(FAILED(m_pD3D->CheckDeviceFormat(pCaps->AdapterOrdinal, 
                                    pCaps->DeviceType, 
                                    AdapterFormat, 
                                    D3DUSAGE_DEPTHSTENCIL, 
                                    D3DRTYPE_SURFACE,
                                    D3DFMT_D16)))
    return E_FAIL;
```



[**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) consente di scegliere un dispositivo da creare in base alle funzionalità del dispositivo. In questo caso, i dispositivi che non supportano i buffer di profondità a 16 bit vengono rifiutati.

Nell'esempio di codice seguente viene illustrato l'uso di [**IDirect3D9:: CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch) per determinare la compatibilità di stencil Depth con una destinazione di rendering.


```
// Reject devices that cannot create a render target of RTFormat while
// the back buffer is of RTFormat and the depth-stencil buffer is
// at least 8 bits of stencil
if(FAILED(m_pD3D->CheckDepthStencilMatch(pCaps->AdapterOrdinal,
                                        pCaps->DeviceType, 
                                        AdapterFormat, 
                                        RTFormat, 
                                        D3DFMT_D24S8)))
    return E_FAIL;
```



Quando si è certi che il driver supporta i buffer di profondità, è possibile verificare il supporto del buffer w. Sebbene i buffer di profondità siano supportati per tutti i rasterizzatori software, i buffer w sono supportati solo dall'rasterizzatore dei riferimenti, che non è adatto per l'uso da parte di applicazioni reali. Indipendentemente dal tipo di dispositivo usato dall'applicazione, verificare il supporto per i buffer w prima di provare ad abilitare il buffering con profondità basata su w.

1.  Dopo la creazione del dispositivo, chiamare il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/desktop/api) , passando una struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) inizializzata.
2.  Dopo la chiamata, il membro LineCaps contiene informazioni sul supporto del driver per il rendering delle primitive.
3.  Se il membro RasterCaps della struttura contiene il flag D3DPRASTERCAPS \_ WBUFFER, il driver supporta il buffering con profondità basata su w per quel tipo primitivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer di profondità](depth-buffers.md)
</dt> </dl>

 

 
