---
title: Introduzione a una risorsa in Direct3D 11
description: Questo argomento introduce risorse Direct3D, ad esempio buffer e trame.
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb466883991795a66eec0ba1b99f5c989fa33c1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399354"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Introduzione a una risorsa in Direct3D 11

Le risorse sono i blocchi predefiniti della scena. Contengono la maggior parte dei dati usati da Direct3D per interpretare ed eseguire il rendering della scena. Le risorse sono aree in memoria a cui è possibile accedere dalla pipeline Direct3D. Le risorse contengono i tipi di dati seguenti: Geometry, Textures, shader data. Questo argomento introduce risorse Direct3D, ad esempio buffer e trame.

È possibile creare risorse fortemente tipizzate o non tipizzate; è possibile controllare se le risorse hanno accesso sia in lettura che in scrittura; è possibile rendere le risorse accessibili solo alla CPU, alla GPU o a entrambe. Per ogni fase della pipeline possono essere attive fino a 128 risorse.

Direct3D garantisce che restituisca zero per tutte le risorse a cui si accede fuori limite.

Il ciclo di vita di una risorsa Direct3D è il seguente:

-   Creare una risorsa usando uno dei metodi create dell'interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .
-   Associare una risorsa alla pipeline utilizzando un contesto e uno dei metodi set dell'interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .
-   Deallocare una risorsa chiamando il metodo di [**rilascio**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) dell'interfaccia della risorsa.

Questa sezione contiene i seguenti argomenti:

-   [Tipizzazione forte rispetto alla tipizzazione debole](#strong-vs-weak-typing)
-   [Viste delle risorse](#resource-views)
-   [Viste non elaborate dei buffer](#raw-views-of-buffers)
-   [Argomenti correlati](#related-topics)

## <a name="strong-vs-weak-typing"></a>Tipizzazione forte rispetto alla tipizzazione debole

Esistono due modi per specificare completamente il layout (o footprint di memoria) di una risorsa:

-   Tipizzato: specificare completamente il tipo quando viene creata la risorsa.
-   Senza tipi: specificare completamente il tipo quando la risorsa è associata alla pipeline.

La creazione di una risorsa completamente tipizzata limita la risorsa al formato con cui è stato creato. Ciò consente al runtime di ottimizzare l'accesso, soprattutto se la risorsa viene creata con flag che indicano che non è possibile eseguirne il mapping tramite l'applicazione. Le risorse create con un tipo specifico non possono essere riinterpretate usando il meccanismo di visualizzazione a meno che la risorsa non sia stata creata con il flag D3D10 di \_ \_ Binding DDI \_ . Se \_ \_ l'associazione DDI D3D10 \_ presente è impostata su render-target o è possibile creare viste delle risorse dello shader su queste risorse usando uno dei membri completamente tipizzati della famiglia appropriata, anche se la risorsa originale è stata creata come completamente tipizzata.

In una risorsa di tipo less, il tipo di dati è sconosciuto quando la risorsa viene creata per la prima volta. L'applicazione deve scegliere tra i formati di tipo less disponibili (vedere [**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). È necessario specificare le dimensioni della memoria da allocare e se il runtime dovrà generare le sottotrame in un mipmap. Tuttavia, il formato dei dati esatto (indipendentemente dal fatto che la memoria venga interpretata come numeri interi, valori a virgola mobile, interi senza segno e così via) non viene determinato fino a quando la risorsa non viene associata alla pipeline con una [visualizzazione risorse](#resource-views). Poiché il formato di trama rimane flessibile finché la trama non è associata alla pipeline, la risorsa viene definita archiviazione debolmente tipizzata. L'archiviazione debolmente tipizzata ha il vantaggio di poter essere riutilizzata o riinterpretata in un altro formato purché il numero di componenti e il numero di bit di ogni componente siano uguali in entrambi i formati.

Una singola risorsa può essere associata a più fasi della pipeline, purché ognuna disponga di una visualizzazione univoca, che qualifica completamente i formati in ogni posizione. Ad esempio, una risorsa creata con formato DXGI \_ formato \_ R32G32B32A32 senza \_ tipo può essere usata come \_ formato DXGI \_ R32G32B32A32 \_ float e un \_ formato DXGI \_ R32G32B32A32 uint in \_ posizioni diverse della pipeline simultaneamente.

## <a name="resource-views"></a>Viste delle risorse

Le risorse possono essere archiviate in formati di memoria per utilizzo generico, in modo che possano essere condivise da più fasi della pipeline. Una fase della pipeline interpreta i dati delle risorse utilizzando una vista. Una visualizzazione risorse è concettualmente simile a eseguire il cast dei dati della risorsa in modo che possano essere usati in un determinato contesto.

Una vista può essere utilizzata con una risorsa senza tipo. Ovvero, è possibile creare una risorsa in fase di compilazione e dichiarare il tipo di dati quando la risorsa è associata alla pipeline. Una vista creata per una risorsa di tipo non ha sempre lo stesso numero di bit per componente; il modo in cui i dati vengono interpretati dipende dal formato specificato. Il formato specificato deve essere della stessa famiglia del formato del tipo utilizzato durante la creazione della risorsa. Ad esempio, una risorsa creata con il \_ formato senza tipo R8G8B8A8 non può essere considerata come una \_ risorsa float R32 anche se entrambi i formati possono avere le stesse dimensioni in memoria.

Una vista espone anche altre funzionalità, ad esempio la possibilità di leggere le superfici di profondità/stencil in uno shader, di generare un mappa cubi dinamico in un singolo passaggio e di eseguire il rendering simultaneo in più sezioni di un volume.



| Interfaccia risorsa                                             | Descrizione                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | Accedere a una risorsa di trama durante i test di stencil di profondità.                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | Accedere a una risorsa di trama usata come destinazione di rendering.                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | Accedere a una risorsa shader, ad esempio un buffer costante, un buffer di trama, una trama o un campionatore. |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | Accedere a una risorsa non ordinata usando un pixel shader o un compute shader.                        |



 

## <a name="raw-views-of-buffers"></a>Viste non elaborate dei buffer

È possibile pensare a un buffer non elaborato, che può essere chiamato anche [buffer di indirizzi di byte](direct3d-11-advanced-stages-cs-resources.md), come un contenitore di bit a cui si vuole accedere in modo non elaborato, ovvero un buffer a cui è possibile accedere facilmente tramite blocchi da uno a valori di indirizzo senza tipo a 4 32 bit. Si indica che si desidera l'accesso non elaborato a un buffer (o, una visualizzazione non elaborata di un buffer) quando si chiama uno dei metodi seguenti per creare una vista nel buffer:

-   Per creare una visualizzazione risorse dello shader (SRV) nel buffer, chiamare [**ID3D11Device:: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) con il flag [**d3d11 \_ BUFFEREX \_ SRV \_ flag \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag). Questo flag viene specificato nel membro **Flags** della struttura [**d3d11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv) . Impostare **d3d11 \_ BUFFEREX \_ SRV** nel membro **BUFFEREX** della struttura [**\_ \_ \_ \_ desc della visualizzazione risorse dello shader d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) a cui punta il parametro *pDesc* di **ID3D11Device:: CreateShaderResourceView** . Si imposta anche il [**valore \_ \_ \_ BUFFEREX della dimensione d3d11 SRV**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)) nel membro **ViewDimension** di **d3d11 \_ shader \_ Resource \_ View \_ desc** per indicare che SRV è una visualizzazione non elaborata.
-   Per creare una visualizzazione di accesso non ordinata (UAV) nel buffer, chiamare [**ID3D11Device:: CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) con il flag [**UAV del buffer D3D11 non \_ \_ \_ \_ elaborato**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag). Questo flag viene specificato nel membro **Flags** della struttura [**d3d11 \_ buffer \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav) . Si imposta **d3d11 \_ buffer \_ UAV** nel membro **buffer** della struttura [**d3d11 della \_ \_ \_ vista \_ di accesso non ordinata**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc) in cui il parametro *pDesc* di **ID3D11Device:: CreateUnorderedAccessView** punta. Si imposta anche il valore del [**\_ buffer della \_ dimensione \_ d3d11 UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension) nel membro **ViewDimension** di **d3d11 \_ unordered \_ Access \_ View \_ desc** per indicare che UAV è una visualizzazione non elaborata.

È possibile utilizzare i tipi di oggetto HLSL [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) e [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) quando si utilizzano buffer non elaborati.

Per creare una visualizzazione non elaborata in un buffer, è prima necessario chiamare [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) con il [**buffer di \_ varie risorse d3d11 \_ \_ \_ allow \_ RAW \_ views**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag per creare la risorsa buffer sottostante. È possibile specificare questo flag nel membro **MiscFlags** della struttura [**\_ \_ Desc del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a cui punta il parametro *pDesc* di **ID3D11Device:: CreateBuffer** . Non è possibile combinare **il \_ buffer di varie risorse d3d11 \_ \_ \_ Consenti \_ \_ viste non elaborate** con la [**\_ risorsa d3d11 \_ \_ \_ struttura del buffer varie**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag). Inoltre, se si specifica [**il \_ \_ \_ buffer costante di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) in **BindFlags** di **d3d11 \_ buffer \_ desc**, non è possibile specificare anche il **buffer di \_ varie risorse d3d11 \_ \_ \_ Consenti \_ \_ viste non elaborate** in **MiscFlags**. Non si tratta di una limitazione delle visualizzazioni RAW perché i buffer costanti hanno già un vincolo che non possono essere combinati con altre visualizzazioni.

A parte i casi non validi precedenti, quando si crea un buffer con il [**\_ buffer di varie risorse d3d11 \_ \_ \_ Consenti \_ \_ viste non elaborate**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), la funzionalità non è limitata rispetto alla mancata impostazione del **buffer di \_ varie risorse d3d11 \_ \_ \_ Consenti \_ \_ viste non elaborate**. Ovvero, è possibile usare un buffer di questo tipo per l'accesso non RAW in diversi modi possibili con Direct3D. Se si specifica il flag **d3d11 per \_ varie risorse, \_ \_ \_ Consenti \_ \_ viste non elaborate** , si aumentano solo le funzionalità disponibili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse](overviews-direct3d-11-resources.md)
</dt> <dt>

[Nuovi tipi di risorse](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 