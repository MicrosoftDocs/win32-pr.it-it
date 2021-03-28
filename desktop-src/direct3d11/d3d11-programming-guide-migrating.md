---
title: Migrazione a Direct3D 11
description: Questa sezione fornisce informazioni per la migrazione a Direct3D 11 da una versione precedente di Direct3D.
ms.assetid: 3ec8b5c2-01e6-4fbe-ada7-43898db63bbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ade0a0d32d3f8b5c07e6653955c0c407c8fa8f
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104339462"
---
# <a name="migrating-to-direct3d-11"></a>Migrazione a Direct3D 11

Questa sezione fornisce informazioni per la migrazione a Direct3D 11 da una versione precedente di Direct3D.

-   [Da Direct3D 9 a Direct3D 11](#direct3d-9-to-direct3d-11)
-   [Da Direct3D 10 a Direct3D 11](#direct3d-10-to-direct3d-11)
    -   [Enumerazioni e definizioni](#enumerations-and-defines)
    -   [Strutture](#structures)
    -   [Interfacce](#interfaces)
    -   [Altre tecnologie correlate](#other-related-technologies)
-   [Da Direct3D 10,1 a Direct3D 11](#direct3d-101-to-direct3d-11)
    -   [Enumerazioni e definizioni](#enumerations-and-defines)
    -   [Strutture](#structures)
    -   [Interfacce](#interfaces)
-   [Nuove funzionalità per Direct3D 11](#new-features-for-direct3d-11)
-   [Nuove funzionalità per DirectX 11,1](#new-features-for-directx-111)
-   [Nuove funzionalità per DirectX 11,2](#new-features-for-directx-112)
-   [Argomenti correlati](#related-topics)

## <a name="direct3d-9-to-direct3d-11"></a>Da Direct3D 9 a Direct3D 11

L'API Direct3D 11 si basa sui miglioramenti dell'infrastruttura apportati in Direct3D 10 e 10,1. Il porting da Direct3D 9 a Direct3D 11 è simile al passaggio da Direct3D 9 a Direct3D 10. Di seguito sono riportate le principali difficoltà di questo sforzo.

-   Rimozione di tutti i dati di utilizzo della pipeline della funzione fissa a favore degli shader programmabili creati esclusivamente in HLSL (compilati tramite D3DCompiler anziché D3DX9).
-   Gestione dello stato in base a oggetti non modificabili anziché a singoli Stati.
-   Aggiornamento per conformità ai requisiti di collegamento severi dei layout di input del buffer di vertice e delle firme dello shader.
-   Associazione delle visualizzazioni delle risorse dello shader a tutte le risorse di trama.
-   Mapping di tutto il contenuto di un'immagine a un \_ formato DXGI, inclusa la rimozione di tutti i formati di colore a 16 bit (5/5/5/1, 5/6/5, 4/4/4/4), la rimozione di tutti i formati di colore a 24 bit (8/8/8) e l'ordinamento dei colori RGB rigoroso.
-   Suddivisione dell'utilizzo dello stato costante globale in diversi buffer costanti aggiornati e di dimensioni ridotte.

Per altre informazioni sul passaggio da Direct3D 9 a Direct3D 10, vedere [considerazioni su Direct3D 9 in Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

## <a name="direct3d-10-to-direct3d-11"></a>Da Direct3D 10 a Direct3D 11

La conversione di programmi scritti per l'uso dell'API Direct3D 10 o 10,1 è un processo semplice, in quanto Direct3D 11 è un'estensione dell'API esistente. Con una sola eccezione secondaria (come indicato di seguito: filtro del testo monocromatico), in Direct3D 11 sono disponibili tutti i metodi e le funzionalità di Direct3D 10/10.1. Il contorno seguente descrive le differenze tra le due API per facilitare l'aggiornamento del codice esistente. Di seguito sono riportate le differenze principali:

-   Le operazioni di rendering (disegni, stato e così via) non fanno più parte dell'interfaccia del dispositivo, ma fanno invece parte della nuova interfaccia DeviceContext insieme ai metodi di query map/annullare e Device.
-   Direct3D 11 include tutti i miglioramenti e le modifiche apportate tra Direct3D 10,0 e 10,1

### <a name="enumerations-and-defines"></a>Enumerazioni e definizioni



| Direct3D 10                            | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_formato DXGI                           | [**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)È stato definito il formato di diversi nuovi formati DXGI.<br/>                                                                                                                                                                                                                                                                                                                                |
| D3D10 \_ Crea il \_ passaggio del dispositivo \_ \_ a \_ ref | [**D3d11 \_ CREARE \_ il \_ passaggio del dispositivo \_ a \_ ref**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)la funzionalità switch-to-ref non è supportata da Direct3D 11.<br/>                                                                                                                                                                                                                                                                        |
| \_Tipo di driver D3D10 \_                    | [**D3D \_ \_Tipo di driver**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)si noti che gli identificatori di enumerazione nel [**\_ \_ tipo di driver D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) sono stati ridefiniti dagli identificatori nel [**\_ \_ tipo di driver D3D10**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type). Pertanto, è necessario assicurarsi di usare gli identificatori di enumerazione anziché i numeri letterali.<br/> [**D3D \_ Il \_ tipo di driver**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) è definito in D3Dcommon. h.<br/> |
| \_ \_ Flag varie della risorsa D3D10 \_            | [**D3d11 \_ \_ \_ Flag misc delle risorse**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag). si noti che molti di questi flag sono stati ridefiniti, quindi assicurarsi di usare gli identificatori di enumerazione anziché i numeri letterali.<br/>                                                                                                                                                                                                                                |
| \_Filtro D3D10                          | [**D3d11 \_ Si noti che il filtro**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)del testo D3D10 \_ filtro \_ del testo \_ 1BIT è stato rimosso da Direct3D 11. Vedere DirectWrite.<br/>                                                                                                                                                                                                                                                                            |
| \_Contatore d3d11                         | [**D3d11 \_ Si noti che**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_counter)i contatori indipendenti dal fornitore sono stati rimossi per Direct3D 11 poiché erano raramente supportati.<br/>                                                                                                                                                                                                                                                                          |
| D3D10 \_ x                               | D3D11 \_ x molte enumerazioni e definizioni sono uguali, hanno limiti maggiori o hanno valori aggiuntivi.<br/>                                                                                                                                                                                                                                                                                                               |



 

### <a name="structures"></a>Strutture



| Direct3D 10                              | Direct3D 11                                                                                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ la \_ voce della Dichiarazione \_            | [**D3d11 \_ QUINDI, la \_ \_ voce di dichiarazione**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)aggiunge il flusso.<br/>                                                                  |
| D3D10 \_ Blend \_ DESC                       | [**D3d11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)Nota: questa struttura è cambiata significativamente da 10 a 10,1 per fornire lo stato di Blend per ogni destinazione di rendering<br/> |
| D3D10 \_ buffer \_ DESC                      | [**D3d11 \_ BUFFER \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)aggiunge un StructureByteStride per l'uso con le risorse compute shader<br/>                                 |
| \_ \_ Descrizione della visualizzazione risorse \_ shader \_ D3D10      | [**D3d11 \_ \_ \_ Visualizzazione risorse \_ shader**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc). Nota: questa struttura ha aggiunto membri di unione aggiuntivi per 10,1<br/>    |
| \_ \_ Visualizzazione stencil profondità \_ D3D10 \_ DESC        | [**D3d11 \_ Nella \_ visualizzazione stencil profondità \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)è presente un nuovo membro Flags.<br/>                                                |
| \_Statistiche della \_ pipeline di dati di query D3D10 \_ \_ | [**D3d11 \_ Le \_ \_ \_ statistiche della pipeline di dati di query**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics)aggiungono diversi nuovi contatori di fasi dello shader.<br/>                  |
| D3D10 \_ x                                 | D3D11 \_ x molte strutture sono identiche tra le due API.<br/>                                                                                     |



 

### <a name="interfaces"></a>Interfacce



| Direct3D 10        | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device       | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> L'interfaccia del dispositivo è stata suddivisa in queste due parti. Per una rapida portabilità, è possibile usare [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> I metodi "ID3D10Device:: GetTextFilterSize" e "SetTextFilerSize" non esistono più. Vedere DirectWrite.<br/> Create \* shader accetta un parametro facoltativo aggiuntivo per [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*Seshader e \* getshader accettano altri parametri facoltativi per [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) accetta una matrice e conta più stride del flusso di output.<br/> Il limite per il parametro NumEntries di [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) è aumentato a d3d11 \_ , quindi il conteggio dei \_ flussi \_ \* d3d11 quindi il \_ numero di componenti di \_ output \_ \_ in Direct3D 11.<br/> |
| ID3D10Buffer       | [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10SwitchToRef  | [**ID3D11SwitchToRef**](/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref) La funzionalità switch-to-ref non è supportata in Direct3D 11.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ID3D10Texture1D    | [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture2D    | [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture3D    | [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) I metodi map e annullare sono stati spostati in [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)e tutti i metodi map utilizzano la [**\_ \_ sottorisorsa**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) mappata d3d11 anziché void \* \* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ID3D10Asynchronous | [**ID3D11Asynchronous**](/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous) Begin, end e GetData sono stati spostati in [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10x            | ID3D11x molte interfacce sono identiche tra le due API.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="other-related-technologies"></a>Altre tecnologie correlate



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>soluzione 10/10.1</th>
<th>11 soluzione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>API di Reflection HLSL (D3D10Compile *, D3DX10Compile*) e shader Reflection</td>
<td>D3DCompiler (vedere D3DCompiler. h)
<blockquote>
[!Note]<br />
Per le app di Windows Store, le <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">API D3DCompiler</a> sono supportate solo per lo sviluppo, non per la distribuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Effetti 10</td>
<td><a href="https://github.com/Microsoft/FX11">Gli effetti 11</a> sono disponibili come origine condivisa online.
<blockquote>
[!Note]<br />
Questa soluzione non è adatta alle app di Windows Store perché richiede le <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">API D3DCompiler</a> in fase di esecuzione (distribuzione).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DX9/D3DX10 Math</td>
<td><a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a></td>
</tr>
<tr class="even">
<td>D3DX10</td>
<td>D3DX11 in Legacy DirectX SDK <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a>, <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a>e <a href="https://github.com/Microsoft/DirectXMesh">DirectXMesh</a> offrono alternative a molte tecnologie nelle librerie d3dx10 e D3DX11 legacy.<br/> <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> e <a href="/windows/desktop/DirectWrite/direct-write-portal">DirectWrite</a> offrono un supporto di qualità elevata per il rendering di linee e caratteri con stile.<br/></td>
</tr>
</tbody>
</table>



 

Per informazioni sul legacy DirectX SDK, vedere [dove è DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).

## <a name="direct3d-101-to-direct3d-11"></a>Da Direct3D 10,1 a Direct3D 11

Direct3D 10,1 è un'estensione dell'interfaccia Direct3D 10 e tutte le funzionalità di Direct3D 10,1 sono disponibili in Direct3D 11. La maggior parte del porting da 10,1 a 11 è già stata risolta in precedenza in passaggio da 10 a 11.

### <a name="enumerations-and-defines"></a>Enumerazioni e definizioni



| Direct3D 10,1          | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Level1 funzionalità \_ D3D10 | [**D3D \_ \_Livello di funzionalità**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)identico ma definito in D3DCommon. h, oltre all'aggiunta del \_ livello di funzionalità D3D \_ \_ 11 \_ 0 per l'hardware di 11 classi insieme al \_ livello di funzionalità D3D \_ \_ 9 \_ 1, al \_ livello di funzionalità D3D \_ \_ 9 \_ 2 e al \_ livello di funzionalità D3D \_ \_ 9 \_ 3 per 10level9<br/> (D3D10 \_ Sono stati aggiunti anche il livello di funzionalità 9 1, il livello di funzionalità \_ \_ \_ D3D10 \_ \_ \_ 9 \_ 2 e il livello di \_ funzionalità D3D10 \_ \_ 9 \_ 3 per 10,1 a D3D10 \_ 1. h)<br/> |



 

### <a name="structures"></a>Strutture



| Direct3D 10,1                        | Direct3D 11                                                                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \_DESC1 Blend \_ D3D10                  | [**D3d11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)la versione 11 è identica a 10,1.<br/>                                 |
| \_ \_ Visualizzazione risorse shader D3D10 \_ \_ DESC1 | [**D3d11 \_ \_Visualizzazione risorse shader \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)la versione 11 è identica a 10,1.<br/> |



 

### <a name="interfaces"></a>Interfacce



| Direct3D 10,1             | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device1             | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [ **sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> L'interfaccia del dispositivo è stata suddivisa in queste due parti. Per una rapida portabilità, è possibile usare [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> I metodi "ID3D10Device:: GetTextFilterSize" e "SetTextFilerSize" non esistono più. Vedere DirectWrite.<br/> Create \* shader accetta un parametro facoltativo aggiuntivo per [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*Seshader e \* getshader accettano altri parametri facoltativi per [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) accetta una matrice e conta più stride del flusso di output.<br/> Il limite per il parametro NumEntries di [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) è aumentato a d3d11 \_ , quindi il conteggio dei \_ flussi \_ \* d3d11 quindi il \_ numero di componenti di \_ output \_ \_ in Direct3D 11.<br/> |
| ID3D10BlendState1         | [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ID3D10ShaderResourceView1 | [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="new-features-for-direct3d-11"></a>Nuove funzionalità per Direct3D 11

Una volta aggiornato il codice per l'uso dell'API Direct3D 11, è necessario prendere in considerazione numerose [nuove funzionalità](direct3d-11-features.md) .

-   Rendering multithreading tramite elenchi di comandi e più contesti
-   Implementazione di algoritmi avanzati con compute shader (usando i profili Shader 4,0, 4,1 o 5,0)
-   Nuove funzionalità hardware di 11 classi:
    -   Modello HLSL shader 5,0
    -   Collegamento dinamico dello shader
    -   Suddivisione a mosaico tramite Hull e Domain shader
    -   Nuovi formati di compressione dei blocchi: BC6H per immagini HDR, BC7 per immagini standard a fedeltà superiore
-   Uso della [tecnologia 10level9](overviews-direct3d-11-devices-downlevel.md) per il rendering in molti dispositivi shader model 2,0 e shader model 3,0 tramite l'API DIrect3D 11 per il supporto hardware video di fascia inferiore in Windows Vista e Windows 7.
-   Sfruttando il dispositivo di rendering del software WARP.

## <a name="new-features-for-directx-111"></a>Nuove funzionalità per DirectX 11,1

Windows 8 include ulteriori miglioramenti della grafica DirectX da considerare quando si implementa il codice grafico DirectX, che include [Direct3D 11,1](direct3d-11-features.md), [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), [Windows Display Driver Model (WDDM) 1,2](/windows-hardware/drivers/display/wddm-in-windows-8), hardware a [livello di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, contesti di dispositivo Direct2D e altri miglioramenti.

Il supporto parziale per [Direct3D 11,1](direct3d-11-features.md) è disponibile anche in Windows 7 tramite l' [aggiornamento della piattaforma per Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), disponibile tramite l' [aggiornamento della piattaforma per Windows 7](https://support.microsoft.com/kb/2670838).

## <a name="new-features-for-directx-112"></a>Nuove funzionalità per DirectX 11,2

Il Windows 8.1 include [Direct3D 11,2](direct3d-11-2-features.md), [DXGI 1,3](/windows/desktop/direct3ddxgi/dxgi-1-3-improvements)e altri miglioramenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

