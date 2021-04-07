---
description: Per la creazione di buffer è necessario definire i dati archiviati nel buffer, fornire dati di inizializzazione e impostare i flag di utilizzo e di associazione appropriati. Per creare trame, vedere Creazione di risorse di trama (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Creazione di risorse buffer (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748514"
---
# <a name="creating-buffer-resources-direct3d-10"></a>Creazione di risorse buffer (Direct3D 10)

Per la creazione di buffer è necessario definire i dati archiviati nel buffer, fornire dati di inizializzazione e impostare i flag di utilizzo e di associazione appropriati. Per creare trame, vedere [creazione di risorse di trama (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).

-   [Creare un buffer vertici](#create-a-vertex-buffer)
    -   [Creare una descrizione del buffer](#create-a-buffer-description)
    -   [Creare i dati di inizializzazione per il buffer](#create-the-initialization-data-for-the-buffer)
    -   [Creare il buffer](#create-the-buffer)
-   [Creazione di un buffer di indice](#create-an-index-buffer)
-   [Creare un buffer costante](#create-a-constant-buffer)
-   [Argomenti correlati](#related-topics)

## <a name="create-a-vertex-buffer"></a>Creare un buffer vertici

Di seguito sono riportati i passaggi per la creazione di un [buffer vertex](d3d10-graphics-programming-guide-resources-types.md) .

-   [Creare una descrizione del buffer](#create-a-buffer-description)
-   [Creare i dati di inizializzazione per il buffer](#create-the-initialization-data-for-the-buffer)
-   [Creare il buffer](#create-the-buffer)

### <a name="create-a-buffer-description"></a>Creare una descrizione del buffer

Quando si crea un vertex buffer, viene usata una descrizione del buffer (vedere [**D3D10 \_ buffer \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) per definire la modalità di organizzazione dei dati all'interno del buffer, il modo in cui la pipeline può accedere al buffer e il modo in cui verrà usato il buffer.

Nell'esempio seguente viene illustrato come creare una descrizione del buffer per un singolo triangolo con vertici che contengono valori di posizione e colore.


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



In questo esempio la descrizione del buffer viene inizializzata con quasi tutte le impostazioni predefinite per l' [**utilizzo**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**l'accesso alla CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) e i [**flag varie**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag). Le altre impostazioni sono per il [**flag di binding**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) che identifica la risorsa solo come buffer dei vertici e le dimensioni del buffer.

I flag di utilizzo e di accesso alla CPU sono importanti per le prestazioni. Questi due flag determinano la frequenza con cui viene eseguito l'accesso a una risorsa, il tipo di memoria in cui è possibile caricare la risorsa e il processore che deve accedere alla risorsa. Utilizzo predefinito questa risorsa non verrà aggiornata molto spesso. Se si imposta l'accesso alla CPU su 0, la CPU non dovrà leggere o scrivere la risorsa. In combinazione, questo significa che il runtime può caricare la risorsa nella memoria più elevata per la GPU, perché la risorsa non richiede l'accesso alla CPU.

Come previsto, esiste un compromesso tra prestazioni ottimali e accessibilità in qualsiasi momento da parte del processore. Ad esempio, l'utilizzo predefinito senza accesso alla CPU significa che la risorsa può essere resa disponibile esclusivamente alla GPU. Questo potrebbe includere il caricamento della risorsa in memoria non direttamente accessibile dalla CPU. La risorsa può essere modificata solo con [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).

### <a name="create-the-initialization-data-for-the-buffer"></a>Creare i dati di inizializzazione per il buffer

Un buffer è semplicemente una raccolta di elementi ed è disposto come matrice 1D. Di conseguenza, il pitch della memoria di sistema e il passo della sezione della memoria di sistema sono uguali; dimensione della dichiarazione dei dati dei vertici. Un'applicazione può fornire dati di inizializzazione quando viene creato un buffer usando una [**Descrizione della sottorisorsa**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), che contiene un puntatore ai dati della risorsa effettivi e contiene informazioni sulle dimensioni e sul layout dei dati.

Qualsiasi buffer creato con utilizzo non modificabile (vedere l' [**utilizzo di D3D10 non \_ \_ modificabile**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) deve essere inizializzato al momento della creazione. I buffer che usano uno qualsiasi degli altri flag di utilizzo possono essere aggiornati dopo l'inizializzazione usando [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)e [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)oppure accedendo alla relativa memoria sottostante usando il metodo [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .

### <a name="create-the-buffer"></a>Creare il buffer

Utilizzando la descrizione del buffer e i dati di inizializzazione (facoltativo), chiamare [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) per creare un buffer vertex. Il frammento di codice seguente illustra come creare un buffer vertex da una matrice di dati vertex dichiarata dall'applicazione.


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a>Creazione di un buffer di indice

La creazione di un buffer di indice è molto simile alla creazione di un buffer vertex; con due differenze. Un buffer di indice contiene solo dati a 16 bit o a 32 bit, anziché l'ampia gamma di formati disponibili per un buffer di vertici. Un buffer di indice richiede anche un flag di binding del buffer di indice.

Nell'esempio seguente viene illustrato come creare un buffer di indice da una matrice di dati di indice.


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a>Creare un buffer costante

Direct3D 10 introduce un buffer costante. Un buffer costante o un buffer costante dello shader è un buffer che contiene costanti shader. Di seguito è riportato un esempio di creazione di un buffer costante, tratto dall' [esempio HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



Si noti che quando si usa l'interfaccia [**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , il processo di creazione, associazione e invio di un buffer costante viene gestito dall'istanza dell' **interfaccia ID3D10Effect** . In tal caso, è solo nescesary ottenere la variabile dall'effetto con uno dei metodi GetVariable, ad esempio [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , e aggiornare la variabile con uno dei metodi sevariable, ad esempio [**sematrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix). Per un esempio di utilizzo dell' **interfaccia ID3D10Effect** per la gestione di un buffer costante [, vedere Esercitazione 7: mapping di trame e buffer costanti](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



