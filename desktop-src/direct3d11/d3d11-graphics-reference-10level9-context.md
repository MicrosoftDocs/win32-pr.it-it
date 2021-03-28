---
title: Metodi sul ID3D11DeviceContext di 10Level9
description: Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi sul ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb3dc46aeeb5d629c4bf50492083d09b34de1b08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044250"
---
# <a name="10level9-id3d11devicecontext-methods"></a>Metodi sul ID3D11DeviceContext di 10Level9

Questa sezione elenca le differenze tra ogni livello di funzionalità 10Level9 e il livello di funzionalità D3D \_ \_ \_ 11 \_ 0 e un livello di funzionalità superiore per i metodi [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

-   [Sul ID3D11DeviceContext:: CopySubresourceRegion](#id3d11devicecontextcopysubresourceregion)
-   [Sul ID3D11DeviceContext:: CopyResource](#id3d11devicecontextcopyresource)
-   [Sul ID3D11DeviceContext:: CopyStructureCount](#id3d11devicecontextcopystructurecount)
-   [Sul ID3D11DeviceContext:: ClearUnorderedAccessViewFloat](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [Sul ID3D11DeviceContext:: ClearUnorderedAccessViewUint](#id3d11devicecontextclearunorderedaccessviewuint)
-   [Sul ID3D11DeviceContext:: ClearRenderTargetView](#id3d11devicecontextclearrendertargetview)
-   [Sul ID3D11DeviceContext:: CSSetConstantBuffers](#id3d11devicecontextcssetconstantbuffers)
-   [Sul ID3D11DeviceContext:: CSSetSamplers](#id3d11devicecontextcssetsamplers)
-   [Sul ID3D11DeviceContext:: CSSetShader](#id3d11devicecontextcssetshader)
-   [Sul ID3D11DeviceContext:: CSSetShaderResources](#id3d11devicecontextcssetshaderresources)
-   [Sul ID3D11DeviceContext:: CSSetUnorderedAccessViews](#id3d11devicecontextcssetunorderedaccessviews)
-   [Sul ID3D11DeviceContext::D patch](#id3d11devicecontextdispatch)
-   [Sul ID3D11DeviceContext::D ispatchIndirect](#id3d11devicecontextdispatchindirect)
-   [Sul ID3D11DeviceContext::D RAW](#id3d11devicecontextdraw)
-   [Sul ID3D11DeviceContext::D rawAuto](#id3d11devicecontextdrawauto)
-   [Sul ID3D11DeviceContext::D rawIndexed](#id3d11devicecontextdrawindexed)
-   [Sul ID3D11DeviceContext::D rawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [Sul ID3D11DeviceContext::D rawIndexedInstancedIndirect](#id3d11devicecontextdrawindexedinstancedindirect)
-   [Sul ID3D11DeviceContext::D rawInstanced](#id3d11devicecontextdrawinstanced)
-   [Sul ID3D11DeviceContext::D rawInstancedIndirect](#id3d11devicecontextdrawinstancedindirect)
-   [Sul ID3D11DeviceContext::D SSetConstantBuffers](#id3d11devicecontextdssetconstantbuffers)
-   [Sul ID3D11DeviceContext::D SSetSamplers](#id3d11devicecontextdssetsamplers)
-   [Sul ID3D11DeviceContext::D SSetShader](#id3d11devicecontextdssetshader)
-   [Sul ID3D11DeviceContext::D SSetShaderResources](#id3d11devicecontextdssetshaderresources)
-   [Sul ID3D11DeviceContext:: GSSetConstantBuffers](#id3d11devicecontextgssetconstantbuffers)
-   [Sul ID3D11DeviceContext:: GSSetSamplers](#id3d11devicecontextgssetsamplers)
-   [Sul ID3D11DeviceContext:: GSSetShader](#id3d11devicecontextgssetshader)
-   [Sul ID3D11DeviceContext:: GSSetShaderResources](#id3d11devicecontextgssetshaderresources)
-   [Sul ID3D11DeviceContext:: HSSetConstantBuffers](#id3d11devicecontexthssetconstantbuffers)
-   [Sul ID3D11DeviceContext:: HSSetSamplers](#id3d11devicecontexthssetsamplers)
-   [Sul ID3D11DeviceContext:: HSSetShader](#id3d11devicecontexthssetshader)
-   [Sul ID3D11DeviceContext:: HSSetShaderResources](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [Sul ID3D11DeviceContext:: IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [Sul ID3D11DeviceContext:: OMSetBlendState](#id3d11devicecontextomsetblendstate)
-   [Sul ID3D11DeviceContext:: OMSetRenderTargets](#id3d11devicecontextomsetrendertargets)
-   [Sul ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [Sul ID3D11DeviceContext::P SSetConstantBuffers](#id3d11devicecontextpssetconstantbuffers)
-   [Sul ID3D11DeviceContext::P SSetSamplers](#id3d11devicecontextpssetsamplers)
-   [Sul ID3D11DeviceContext::P SSetShader](#id3d11devicecontextpssetshader)
-   [Sul ID3D11DeviceContext::P SSetShaderResources](#id3d11devicecontextpssetshaderresources)
-   [Sul ID3D11DeviceContext:: RSSetScissorRects](#id3d11devicecontextrssetscissorrects)
-   [Sul ID3D11DeviceContext:: RSSetViewports](#id3d11devicecontextrssetviewports)
-   [Sul ID3D11DeviceContext:: SetPredication](#id3d11devicecontextsetpredication)
-   [Sul ID3D11DeviceContext:: SOSetTargets](#id3d11devicecontextsosettargets)
-   [Sul ID3D11DeviceContext:: VSSetConstantBuffers](#id3d11devicecontextvssetconstantbuffers)
-   [Sul ID3D11DeviceContext:: VSSetSamplers](#id3d11devicecontextvssetsamplers)
-   [Sul ID3D11DeviceContext:: VSSetShader](#id3d11devicecontextvssetshader)
-   [Sul ID3D11DeviceContext:: VSSetShaderResources](#id3d11devicecontextvssetshaderresources)
-   [Argomenti correlati](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>Sul ID3D11DeviceContext:: CopySubresourceRegion



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Solo Texture2D e buffer possono essere copiati nella memoria accessibile dalla GPU.<br/> Non è possibile copiare Texture3D dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.<br/> Tutte le risorse che hanno solo D3D10_BIND_SHADER_RESOURCE non possono essere copiate dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.<br/> Non è possibile copiare le trame del volume mipmap. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a>Sul ID3D11DeviceContext:: CopyResource



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Solo Texture2D e buffer possono essere copiati nella memoria accessibile dalla GPU.<br/> Non è possibile copiare Texture3D dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.<br/> Tutte le risorse che hanno solo D3D10_BIND_SHADER_RESOURCE non possono essere copiate dalla memoria accessibile dalla GPU alla memoria accessibile dalla CPU.<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a>Sul ID3D11DeviceContext:: CopyStructureCount



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>Sul ID3D11DeviceContext:: ClearUnorderedAccessViewFloat



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>Sul ID3D11DeviceContext:: ClearUnorderedAccessViewUint



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a>Sul ID3D11DeviceContext:: ClearRenderTargetView



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Solo la prima sezione della matrice verrà cancellata. Le applicazioni devono creare una visualizzazione della destinazione di rendering per ogni sezione della faccia o della matrice, quindi deselezionare singolarmente ogni visualizzazione. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>Sul ID3D11DeviceContext:: CSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a>Sul ID3D11DeviceContext:: CSSetSamplers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a>Sul ID3D11DeviceContext:: CSSetShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a>Sul ID3D11DeviceContext:: CSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>Sul ID3D11DeviceContext:: CSSetUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a>Sul ID3D11DeviceContext::D patch



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a>Sul ID3D11DeviceContext::D ispatchIndirect



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a>Sul ID3D11DeviceContext::D RAW



| Livello funzionalità             | Differenze di comportamento                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | Il numero di primitive non può essere maggiore di 65535.<br/> Le trame non possono essere ripetute su una primitiva più di 128 volte.<br/>    |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | Il numero di primitive non può essere maggiore di 1048575.<br/> Le trame non possono essere ripetute su una primitiva più di 2048 volte.<br/> |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | Il numero di primitive non può essere maggiore di 1048575.<br/> Le trame non possono essere ripetute su una primitiva più di 8192 volte.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>Sul ID3D11DeviceContext::D rawAuto



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a>Sul ID3D11DeviceContext::D rawIndexed



| Livello funzionalità             | Differenze di comportamento                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Livello di funzionalità D3D \_ \_ 9 \_ 1 | Il numero di primitive non può essere maggiore di 65535.<br/> Le trame non possono essere ripetute su una primitiva più di 128 volte.<br/> I valori di indice non possono superare 65534.<br/> Gli elenchi di punti indicizzati non sono supportati.<br/>      |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 2 | Il numero di primitive non può essere maggiore di 1048575.<br/> Le trame non possono essere ripetute su una primitiva più di 2048 volte.<br/> I valori di indice non possono superare 1048575.<br/> Gli elenchi di punti indicizzati non sono supportati.<br/> |
| \_Livello di funzionalità D3D \_ \_ 9 \_ 3 | Il numero di primitive non può essere maggiore di 1048575.<br/> Le trame non possono essere ripetute su una primitiva più di 8192 volte.<br/> I valori di indice non possono superare 1048575.<br/> Gli elenchi di punti indicizzati non sono supportati.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>Sul ID3D11DeviceContext::D rawIndexedInstanced



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Non supportato $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Il numero di primitive non può essere maggiore di 1048575.<br/> Le trame non possono essere ripetute su una primitiva più di 8192 volte.<br/> I valori di indice non possono superare 1048575.<br/>
<blockquote>
[!Note]<br />
Quando si chiama il metodo <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>DrawIndexedInstanced</strong></a> con un vertex shader associato alla pipeline e che non importa dati per istanza, è possibile che alcuni componenti hardware della grafica Direct3D 9 non disegnino nulla. In particolare, se il vertex shader non utilizza dati per istanza, la chiamata a <strong>DrawIndexedInstanced</strong> con 1 istanza non è equivalente alla chiamata di di <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>estrazione</strong></a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>Sul ID3D11DeviceContext::D rawIndexedInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a>Sul ID3D11DeviceContext::D rawInstanced



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>Sul ID3D11DeviceContext::D rawInstancedIndirect



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>Sul ID3D11DeviceContext::D SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a>Sul ID3D11DeviceContext::D SSetSamplers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a>Sul ID3D11DeviceContext::D SSetShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a>Sul ID3D11DeviceContext::D SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>Sul ID3D11DeviceContext:: GSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a>Sul ID3D11DeviceContext:: GSSetSamplers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a>Sul ID3D11DeviceContext:: GSSetShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a>Sul ID3D11DeviceContext:: GSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>Sul ID3D11DeviceContext:: HSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a>Sul ID3D11DeviceContext:: HSSetSamplers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a>Sul ID3D11DeviceContext:: HSSetShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a>Sul ID3D11DeviceContext:: HSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Non supportato in alcun livello di funzionalità 9. * o 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Il formato può essere diverso da quello specificato al momento della creazione del buffer, ma verrà subita una traduzione costosa.<br/> Consente solo buffer di indice con il formato DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Il formato può essere diverso da quello specificato al momento della creazione del buffer, ma verrà subita una traduzione costosa.<br/> Consente i buffer di indice con i formati DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT come D3D_FEATURE_LEVEL_10_0 e versioni successive. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>Sul ID3D11DeviceContext:: IASetPrimitiveTopology



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Le topologie primitive con adiacenza non sono supportate $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a>Sul ID3D11DeviceContext:: OMSetBlendState



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">SampleMask non può essere zero $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a>Sul ID3D11DeviceContext:: OMSetRenderTargets



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Una sola destinazione di rendering supporta $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Sono supportate solo quattro destinazioni di rendering e tutte le risorse con binding devono avere la stessa profondità dei bit.</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>Sul ID3D11DeviceContext:: OMSetRenderTargetsAndUnorderedAccessViews



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>Sul ID3D11DeviceContext::P SSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Vedere il livello di funzionalità 10,0, ma il numero totale di costanti usate da shader non può superare 32 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a>Sul ID3D11DeviceContext::P SSetSamplers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non è possibile associare più di 16 campionatori $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a>Sul ID3D11DeviceContext::P SSetShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Solo ps_4_0_level_9_1 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Solo ps_4_0_level_9_3 o ps_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a>Sul ID3D11DeviceContext::P SSetShaderResources



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non più di 8 risorse dello shader con binding simultaneo $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a>Sul ID3D11DeviceContext:: RSSetScissorRects



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sono disponibili solo zero Scissor Rect, $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a>Sul ID3D11DeviceContext:: RSSetViewports



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">È disponibile solo il viewport zero $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

Anche se si specificano valori float per i membri della struttura del [**\_ viewport d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) per la matrice *pViewports* in una chiamata a [**sul ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) per i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **RSSetViewports** usa i valori DWORD internamente. A causa di questo comportamento, quando si usa un angolo superiore sinistro negativo per il viewport, la chiamata a **RSSetViewports** per i livelli di funzionalità 9 \_ x ha esito negativo. Questo errore si verifica perché **RSSetViewports** per 9 \_ x esegue il cast dei valori a virgola mobile in interi senza segno senza convalida, che comporta un overflow di Integer.

La chiamata a [**sul ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) per i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x e 11 \_ x funziona come previsto anche quando si usa un angolo superiore sinistro negativo per il viewport.

## <a name="id3d11devicecontextsetpredication"></a>Sul ID3D11DeviceContext:: SetPredication



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a>Sul ID3D11DeviceContext:: SOSetTargets



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>Sul ID3D11DeviceContext:: VSSetConstantBuffers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Vedere il livello di funzionalità 10,0, ma il numero totale di costanti usate da shader non può superare 255 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a>Sul ID3D11DeviceContext:: VSSetSamplers



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a>Sul ID3D11DeviceContext:: VSSetShader



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Solo vs_4_0_level_9_1 $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Solo vs_4_0_level_9_3 o vs_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a>Sul ID3D11DeviceContext:: VSSetShaderResources



<table>
<thead>
<tr class="header">
<th>Livello funzionalità</th>
<th>Differenze di comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Non supportato in alcun livello di funzionalità 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





