---
title: 10Level9 METODI ID3D11DeviceContext
description: Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D FEATURE LEVEL 11 0 e superiore per i metodi \_ \_ \_ \_ ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e268f45465139e49afe0f81a64eeeb93939734e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473127"
---
# <a name="10level9-id3d11devicecontext-methods"></a>10Level9 METODI ID3D11DeviceContext

Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D FEATURE LEVEL 11 0 e superiore per i metodi \_ \_ \_ \_ [**ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

-   [ID3D11DeviceContext::CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [ID3D11DeviceContext::CopyResource](#id3d11devicecontextcopyresource)
-   [ID3D11DeviceContext::CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [ID3D11DeviceContext::ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [ID3D11DeviceContext::ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [ID3D11DeviceContext::CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [ID3D11DeviceContext::CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [ID3D11DeviceContext::CSSetShader](#id3d11devicecontextcssetshader)
-   [ID3D11DeviceContext::CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [ID3D11DeviceContext::CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [ID3D11DeviceContext::D ispatch](#id3d11devicecontextdispatch)
-   [ID3D11DeviceContext::D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext::D raw](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext::D rawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext::D rawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext::D rawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [ID3D11DeviceContext::D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext::D rawInstanced](#id3d11devicecontextdrawinstanced)
-   [ID3D11DeviceContext::D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [ID3D11DeviceContext::D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [ID3D11DeviceContext::D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [ID3D11DeviceContext::D SSetShader](#id3d11devicecontextdssetshader)
-   [ID3D11DeviceContext::D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [ID3D11DeviceContext::GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [ID3D11DeviceContext::GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [ID3D11DeviceContext::GSSetShader](#id3d11devicecontextgssetshader)
-   [ID3D11DeviceContext::GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [ID3D11DeviceContext::HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [ID3D11DeviceContext::HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [ID3D11DeviceContext::HSSetShader](#id3d11devicecontexthssetshader)
-   [ID3D11DeviceContext::HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext::IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [ID3D11DeviceContext::OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [ID3D11DeviceContext::OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [ID3D11DeviceContext::P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [ID3D11DeviceContext::P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [ID3D11DeviceContext::P SSetShader](#id3d11devicecontextpssetshader)
-   [ID3D11DeviceContext::P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [ID3D11DeviceContext::RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [ID3D11DeviceContext::RSSetViewports](#id3d11devicecontextrssetviewports)
-   [ID3D11DeviceContext::SetPredication](#id3d11devicecontextsetpredication)
-   [ID3D11DeviceContext::SOSetTargets](#id3d11devicecontextsosettargets)
-   [ID3D11DeviceContext::VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [ID3D11DeviceContext::VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [ID3D11DeviceContext::VSSetShader](#id3d11devicecontextvssetshader)
-   [ID3D11DeviceContext::VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [Argomenti correlati](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>ID3D11DeviceContext::CopySubresourceRegion




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Solo Texture2D e buffer possono essere copiati all'interno della memoria accessibile tramite GPU.<br /> Impossibile copiare Texture3D dalla memoria accessibile tramite GPU alla memoria accessibile dalla CPU.<br /> Qualsiasi risorsa con solo D3D10_BIND_SHADER_RESOURCE non può essere copiata dalla memoria accessibile tramite GPU alla memoria accessibile dalla CPU.<br /> Non è possibile copiare trame di volume mipmapped. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopyresource"></a>ID3D11DeviceContext::CopyResource




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Solo Texture2D e buffer possono essere copiati all'interno della memoria accessibile tramite GPU.<br /> Impossibile copiare Texture3D dalla memoria accessibile tramite GPU alla memoria accessibile dalla CPU.<br /> Qualsiasi risorsa con solo D3D10_BIND_SHADER_RESOURCE non può essere copiata dalla memoria accessibile tramite GPU alla memoria accessibile dalla CPU.<br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcopystructurecount"></a>ID3D11DeviceContext::CopyStructureCount




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>ID3D11DeviceContext::ClearUnorderedAccessViewFloat




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>ID3D11DeviceContext::ClearUnorderedAccessViewUint




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextclearrendertargetview"></a>ID3D11DeviceContext::ClearRenderTargetView




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Verrà cancellata solo la prima sezione della matrice. Le applicazioni devono creare una visualizzazione di destinazione di rendering per ogni viso o sezione di matrice, quindi cancellare ogni visualizzazione singolarmente.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>ID3D11DeviceContext::CSSetConstantBuffers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetsamplers"></a>ID3D11DeviceContext::CSSetSamplers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshader"></a>ID3D11DeviceContext::CSSetShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetshaderresources"></a>ID3D11DeviceContext::CSSetShaderResources




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>ID3D11DeviceContext::CSSetUnorderedAccessViews




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatch"></a>ID3D11DeviceContext::D ispatch




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdispatchindirect"></a>ID3D11DeviceContext::D ispatchIndirect




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::D raw



| Livello di funzionalità             | Differenze di comportamento                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Il numero di primitive non può superare 65535.<br/> Le trame non possono essere ripetute più di 128 volte su una primitiva.<br/>    |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Il numero di primitive non può superare 1048575.<br/> Le trame non possono essere ripetute più di 2048 volte su una primitiva.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Il numero di primitive non può superare 1048575.<br/> Le trame non possono essere ripetute più di 8192 volte su una primitiva.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::D rawAuto




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::D rawIndexed



| Livello di funzionalità             | Differenze di comportamento                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FUNZIONALITÀ D3D \_ \_ LIVELLO \_ 9 \_ 1 | Il numero di primitive non può superare 65535.<br/> Le trame non possono essere ripetute più di 128 volte su una primitiva.<br/> I valori di indice non possono superare 65534.<br/> Gli elenchi di punti indicizzati non sono supportati.<br/>      |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Il numero di primitive non può superare 1048575.<br/> Le trame non possono essere ripetute più di 2048 volte su una primitiva.<br/> I valori di indice non possono superare 1048575.<br/> Gli elenchi di punti indicizzati non sono supportati.<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Il numero di primitive non può superare 1048575.<br/> Le trame non possono essere ripetute più di 8192 volte su una primitiva.<br/> I valori di indice non possono superare 1048575.<br/> Gli elenchi di punti indicizzati non sono supportati.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::D rawIndexedInstanced




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Il numero di primitive non può superare 1048575.<br /> Le trame non possono essere ripetute più di 8192 volte su una primitiva.<br /> I valori di indice non possono superare 1048575.<br /><blockquote>[!Note]<br />Quando si chiama il metodo <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> con un vertex shader associato alla pipeline e che non importa dati per istanza, alcuni componenti hardware grafici Direct3D 9 potrebbero non disegnare nulla. In particolare, se il vertex shader non usa dati per istanza, chiamare <strong>DrawIndexedInstanced</strong> con 1 istanza non equivale a chiamare <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw.</strong></a></blockquote><br /> | 




 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>ID3D11DeviceContext::D rawIndexedInstancedIndirect




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::D rawInstanced




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>ID3D11DeviceContext::D rawInstancedIndirect




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>ID3D11DeviceContext::D SSetConstantBuffers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetsamplers"></a>ID3D11DeviceContext::D SSetSamplers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshader"></a>ID3D11DeviceContext::D SSetShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextdssetshaderresources"></a>ID3D11DeviceContext::D SSetShaderResources




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>ID3D11DeviceContext::GSSetConstantBuffers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetsamplers"></a>ID3D11DeviceContext::GSSetSamplers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshader"></a>ID3D11DeviceContext::GSSetShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextgssetshaderresources"></a>ID3D11DeviceContext::GSSetShaderResources




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>ID3D11DeviceContext::HSSetConstantBuffers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetsamplers"></a>ID3D11DeviceContext::HSSetSamplers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshader"></a>ID3D11DeviceContext::HSSetShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontexthssetshaderresources"></a>ID3D11DeviceContext::HSSetShaderResources




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* o 10.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Il formato può essere diverso da quello specificato al momento della creazione del buffer, ma verrà comportata una conversione dispendiosa.<br /> Consente solo buffer di indice con il DXGI_FORMAT_R16_UINT dati. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Il formato può essere diverso da quello specificato al momento della creazione del buffer, ma verrà comportata una conversione dispendiosa.<br /> Consente buffer di indice con i DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT come D3D_FEATURE_LEVEL_10_0 e versioni successive. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext::IASetPrimitiveTopology




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Le topologie primitive con adicenza non sono supportate${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetblendstate"></a>ID3D11DeviceContext::OMSetBlendState




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | SampleMask non può essere zero${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextomsetrendertargets"></a>ID3D11DeviceContext::OMSetRenderTargets




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | È supportata una sola destinazione di rendering${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Sono supportate solo quattro destinazioni di rendering e tutte le risorse associate devono avere la stessa profondità in bit. | 




 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.*.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>ID3D11DeviceContext::P SSetConstantBuffers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Vedere il livello di funzionalità 10.0, ma il numero totale di costanti usate dallo shader non può superare 32${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetsamplers"></a>ID3D11DeviceContext::P SSetSamplers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non possono essere associati più di 16 campionatori${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextpssetshader"></a>ID3D11DeviceContext::P SSetShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo ps_4_0_level_9_1${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Solo ps_4_0_level_9_3 o ps_4_0_level_9_1 | 




 

## <a name="id3d11devicecontextpssetshaderresources"></a>ID3D11DeviceContext::P SSetShaderResources




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non più di 8 risorse shader associate contemporaneamente${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetscissorrects"></a>ID3D11DeviceContext::RSSetScissorRects




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | È disponibile solo il retto della forbice zero${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextrssetviewports"></a>ID3D11DeviceContext::RSSetViewports




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | È disponibile solo il viewport zero${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

Anche se si specificano valori float per i membri della struttura [**\_ VIEWPORT D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) per la matrice *pViewports* in una chiamata a [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) per i livelli di funzionalità [9](overviews-direct3d-11-devices-downlevel-intro.md) \_ x, **RSSetViewports** usa internamente DWORD. A causa di questo comportamento, quando si usa un angolo superiore sinistro negativo per il viewport, la chiamata a **RSSetViewports** per i livelli di funzionalità 9 x ha \_ esito negativo. Questo errore si verifica perché **RSSetViewports** per 9 x esegue il cast dei valori a virgola mobile in interi senza segno senza convalida, causando un \_ overflow di integer.

La chiamata a [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) per i livelli di funzionalità [10](overviews-direct3d-11-devices-downlevel-intro.md) x e 11 x funziona come previsto anche quando si usa un angolo superiore sinistro negativo per il \_ \_ viewport.

## <a name="id3d11devicecontextsetpredication"></a>ID3D11DeviceContext::SetPredication




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextsosettargets"></a>ID3D11DeviceContext::SOSetTargets




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>ID3D11DeviceContext::VSSetConstantBuffers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Vedere il livello di funzionalità 10.0, ma il numero totale di costanti usate dallo shader non può superare 255${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetsamplers"></a>ID3D11DeviceContext::VSSetSamplers




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecontextvssetshader"></a>ID3D11DeviceContext::VSSetShader




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Solo vs_4_0_level_9_1${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | Solo vs_4_0_level_9_3 o vs_4_0_level_9_1 | 




 

## <a name="id3d11devicecontextvssetshaderresources"></a>ID3D11DeviceContext::VSSetShaderResources




| Livello di funzionalità | Differenze di comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Non supportato a livello di funzionalità 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





