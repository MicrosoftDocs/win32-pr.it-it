---
description: Una risorsa di trama è una raccolta strutturata di dati.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Creazione di risorse di trama (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966170"
---
# <a name="creating-texture-resources-direct3d-10"></a>Creazione di risorse di trama (Direct3D 10)

Una risorsa di [trama](d3d10-graphics-programming-guide-resources-types.md) è una raccolta strutturata di dati. In genere, i valori dei colori vengono archiviati in trame ed è possibile accedervi durante il rendering da parte della [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) in varie fasi sia per l'input che per l'output. La creazione di trame e la definizione del modo in cui verranno usate è una parte importante del rendering di scene interessanti in Direct3D 10.

Anche se le trame contengono in genere informazioni sul colore, la creazione di trame con un [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) diverso consente loro di archiviare tipi diversi di dati. Questi dati possono quindi essere utilizzati dalla pipeline Direct3D 10 in modi non tradizionali.

Tutte le trame hanno limiti sulla quantità di memoria utilizzata e sul numero di Texel in essi contenuti. Questi limiti sono specificati dalle [costanti di risorsa](d3d10-graphics-reference-resource-constants.md).

-   [Creare una trama da un file](#create-a-texture-from-a-file)
    -   [Crea trama e Visualizza separatamente](#create-texture-and-view-separately)
    -   [Crea trama e visualizza simultaneamente](#create-texture-and-view-simultaneously)
-   [Creazione di trame vuote](#creating-empty-textures)
    -   [Rendering in una trama](#rendering-to-a-texture)
    -   [Riempimento manuale delle trame](#filling-textures-manually)
-   [Più Rendertargets](#multiple-rendertargets)
-   [Argomenti correlati](#related-topics)

## <a name="create-a-texture-from-a-file"></a>Creare una trama da un file

> [!Note]  
> La [libreria di utilità D3DX](d3d10-graphics-reference-d3dx10.md) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Quando si crea una trama in Direct3D 10, è anche necessario creare una [vista](d3d10-graphics-programming-guide-resources-access-views.md). Una vista è un oggetto che indica al dispositivo la modalità di accesso a una trama durante il rendering. Il modo più comune per accedere a una trama consiste nel leggerlo usando uno [shader](../direct3dhlsl/dx-graphics-hlsl.md). Una visualizzazione risorse shader indica a uno shader come leggere da una trama durante il rendering. Il tipo di visualizzazione che verrà utilizzato da una trama deve essere specificato al momento della creazione.

La creazione di una trama e il caricamento dei dati iniziali possono essere eseguiti in due modi diversi: creare una trama e visualizzare separatamente oppure creare contemporaneamente la trama e la visualizzazione. L'API fornisce entrambe le tecniche per poter scegliere la soluzione più adatta alle proprie esigenze.

### <a name="create-texture-and-view-separately"></a>Crea trama e Visualizza separatamente

Il modo più semplice per creare una trama consiste nel caricarlo da un file di immagine. Per creare la trama, è sufficiente compilare una struttura e fornire il nome della trama a [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



La funzione D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) esegue tre operazioni: innanzitutto crea un oggetto trama Direct3D 10; in secondo luogo, legge il file di immagine di input; in terzo luogo, archivia i dati dell'immagine nell'oggetto texture. Nell'esempio precedente viene caricato un file BMP, ma la funzione può caricare un'ampia gamma di tipi di file.

Il flag di binding indica che la trama verrà creata come una risorsa shader che consente a una fase dello shader di leggere dalla trama durante il rendering.

Nell'esempio precedente non vengono specificati tutti i parametri di caricamento. In realtà, è spesso utile semplicemente azzerare i parametri di caricamento, in quanto ciò consente a D3DX di scegliere i valori appropriati in base all'immagine di input. Se si vuole che l'immagine di input determini tutti i parametri con cui viene creata la trama, è sufficiente specificare **null** per il parametro **loadInfo** come segue:


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



La specifica di **null** per le informazioni di caricamento è un collegamento semplice ma potente.

Ora che è stata creata una trama, è necessario creare una visualizzazione delle risorse dello shader in modo che la trama possa essere associata come input a uno shader. Poiché [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) restituisce un puntatore a una risorsa e non un puntatore a una trama, è necessario determinare il tipo esatto di risorsa che è stata caricata, quindi è possibile creare una visualizzazione delle risorse dello shader usando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



Sebbene l'esempio precedente crei una visualizzazione della risorsa shader 2D, il codice per creare altri tipi di visualizzazione delle risorse shader è molto simile. Una fase di shader ora può usare questa trama come input.

L'uso di [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) per creare una trama e la visualizzazione associata è un modo per preparare una trama da associare a una fase dello shader. Un altro modo per eseguire questa operazione consiste nel creare contemporaneamente la trama e la relativa visualizzazione, come illustrato nella sezione successiva.

### <a name="create-texture-and-view-simultaneously"></a>Crea trama e visualizza simultaneamente

Direct3D 10 richiede una visualizzazione di trama e una risorsa shader per leggere da una trama durante il Runtime. Poiché la creazione di una trama e di una visualizzazione risorse dello shader è un'attività molto comune, D3DX fornisce il [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) per eseguire questa operazione.


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



Con una singola chiamata di D3DX, vengono create sia la trama che la visualizzazione delle risorse dello shader. La funzionalità del parametro **loadInfo** è invariata. è possibile usarlo per personalizzare la modalità di creazione della trama oppure derivare i parametri necessari dal file di input specificando **null** per il parametro **loadInfo** .

L'oggetto [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) restituito dalla funzione [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) può essere usato in un secondo momento per recuperare l'interfaccia [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) originale, se necessaria. Questa operazione può essere eseguita chiamando il metodo [**getResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .

D3DX fornisce una singola funzione per la creazione di una trama e una visualizzazione delle risorse dello shader come convienience; è necessario decidere quale metodo di creazione di una trama e una visualizzazione si adatta meglio alle esigenze dell'applicazione.

Ora che si è appreso come creare una trama e la relativa visualizzazione delle risorse dello shader, nella sezione successiva verrà illustrato come è possibile campionare (leggere) da tale trama usando uno shader.

## <a name="creating-empty-textures"></a>Creazione di trame vuote

Talvolta le applicazioni desiderano creare una trama e calcolare i dati da archiviare nella trama oppure utilizzare la [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) grafica per eseguire il rendering in questa trama e successivamente utilizzare i risultati in un'altra elaborazione. Queste trame potrebbero essere aggiornate dalla pipeline grafica o dall'applicazione stessa, a seconda del tipo di [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) specificato per la trama al momento della creazione.

### <a name="rendering-to-a-texture"></a>Rendering in una trama

Il caso più comune di creare una trama vuota da riempire con i dati durante il runtime è il caso in cui un'applicazione vuole eseguire il rendering in una trama e quindi usare i risultati dell'operazione di rendering in un passaggio successivo. Le trame create con questo scopo devono specificare l' [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)predefinito.

Nell'esempio di codice seguente viene creata una trama vuota che può essere sottoposta a rendering dalla pipeline e successivamente utilizzata come input per uno [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



Per creare la trama è necessario che l'applicazione specifichi alcune informazioni sulle proprietà che la trama avrà. La larghezza e l'altezza della trama nei Texel sono impostate su 256. Per questa destinazione di rendering, è sufficiente un singolo livello di mipmap. È necessaria una sola destinazione di rendering, quindi la dimensione della matrice è impostata su 1. Ogni Texel contiene valori a virgola mobile a 4 32 bit, che possono essere usati per archiviare informazioni molto precise (vedere [**DXGI \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). È sufficiente un campione per pixel. L'utilizzo è impostato su predefinito perché consente la posizione più efficiente della destinazione di rendering in memoria. Infine, il fatto che la trama verrà associata come destinazione di rendering e verrà specificata una risorsa shader in momenti diversi.

Non è possibile associare le trame per il rendering diretto della pipeline. usare una visualizzazione di destinazione di rendering, come illustrato nell'esempio di codice seguente.


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



Il formato della visualizzazione di destinazione di rendering è semplicemente impostato sul formato della trama originale. Le informazioni nella risorsa devono essere interpretate come una trama 2D e si vuole usare solo il primo livello mipmap della destinazione di rendering.

Analogamente al modo in cui è necessario creare una visualizzazione di destinazione del rendering in modo che la destinazione di rendering possa essere associata per l'output alla pipeline, è necessario creare una visualizzazione della risorsa shader in modo che la destinazione di rendering possa essere associata alla pipeline come input. Nell'esempio di codice riportato di seguito viene illustrato questo.


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



I parametri delle descrizioni delle visualizzazioni delle risorse shader sono molto simili a quelli delle descrizioni delle visualizzazioni di destinazione di rendering e sono stati scelti per gli stessi motivi.

### <a name="filling-textures-manually"></a>Riempimento manuale delle trame

A volte le applicazioni desiderano calcolare i valori in fase di esecuzione, inserirli manualmente in una trama e quindi fare in modo che la [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) grafica usi questa trama in operazioni di rendering successive. A tale scopo, l'applicazione deve creare una trama vuota in modo tale da consentire alla CPU di accedere alla memoria sottostante. Questa operazione viene eseguita creando una trama dinamica e ottenendo l'accesso alla memoria sottostante chiamando un metodo specifico. Nell'esempio di codice seguente viene illustrato come eseguire questa procedura.


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



Si noti che il formato è impostato su un 32 bit per pixel, dove ogni componente è definito da 8 bit. Il parametro Usage è impostato su Dynamic mentre i flag di binding sono impostati per specificare che la trama sarà accessibile da uno shader. Il resto della descrizione della trama è simile alla creazione di una destinazione di rendering.

La chiamata della [**mappa**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) consente all'applicazione di accedere alla memoria sottostante della trama. Il puntatore recuperato viene quindi utilizzato per riempire la trama con i dati. Questa operazione può essere visualizzata nell'esempio di codice seguente.


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a>Più Rendertargets

Fino a otto visualizzazioni di destinazione di rendering possono essere associate alla pipeline alla volta (con [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)). Per ogni pixel (o ogni campione se è abilitato il campionamento multiplo), la fusione viene eseguita indipendentemente per ogni visualizzazione di destinazione di rendering. Due delle variabili di stato di Blend-BlendEnable e RenderTargetWriteMask-sono matrici di otto, ogni membro della matrice corrisponde a una visualizzazione di destinazione di rendering. Quando si usano più destinazioni di rendering, ogni destinazione di rendering deve essere lo stesso [tipo di risorsa](d3d10-graphics-programming-guide-resources-types.md) (buffer, trama 1D, matrice di trama 2D e così via) e deve avere la stessa dimensione (larghezza, altezza, profondità per le trame 3D e dimensioni della matrice per le matrici di trama). Se le destinazioni di rendering sono multicampionate, devono avere lo stesso numero di campioni per pixel.

Può essere attivo un solo buffer di stencil Depth, indipendentemente dal numero di destinazioni di rendering attive. Quando si usano le matrici di trama come destinazioni di rendering, tutte le dimensioni di visualizzazione devono corrispondere. Non è necessario che le destinazioni di rendering abbiano lo stesso formato di trama.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
