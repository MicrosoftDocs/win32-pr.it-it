---
description: I materiali descrivono il modo in cui i poligoni riflettono la luce o sembrano emettere luce in una scena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materials (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8140de30243c7a0f7290715da3d0720cd15cea769bd78cbf66893c0082062d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092955"
---
# <a name="materials-direct3d-9"></a>Materials (Direct3D 9)

I materiali descrivono il modo in cui i poligoni riflettono la luce o sembrano emettere luce in una scena 3D. Le proprietà dei materiali illustrano in dettaglio le caratteristiche di riflessione diffusa, riflessione ambientale, emissione di luce e evidenziazione speculare di un materiale. Direct3D usa la [**struttura D3DMATERIAL9**](d3dmaterial9.md) per portare tutte le informazioni sulle proprietà dei materiali. Ad eccezione della proprietà speculare, ogni proprietà viene descritta come un colore RGBA che rappresenta la quantità di parti rosse, verdi e blu di un determinato tipo di luce che riflette e un fattore di fusione alfa.

## <a name="diffuse-and-ambient-reflection"></a>Reflection diffusa e ambientale

I membri Diffuse e Ambient della [**struttura D3DMATERIAL9**](d3dmaterial9.md) descrivono in che modo un materiale riflette la luce ambientale e diffusa in una scena. Poiché la maggior parte delle scene contiene una luce molto più diffusa rispetto alla luce ambientale, la reflection diffusa svolge la parte più importante nella determinazione del colore. Inoltre, poiché la luce diffusa è direzionale, l'angolo di inclinazione per la luce diffusa influisce sull'intensità complessiva della reflection. La reflection diffusa è massima quando la luce sfora un vertice parallelo alla normale del vertice. Con l'aumentare dell'angolo, l'effetto della reflection diffusa diminuisce. La quantità di luce riflessa è il coseno dell'angolo tra la luce in ingresso e la normale del vertice, come illustrato nella figura seguente.

![illustrazione della quantità di luce riflessa](images/incident.png)

La reflection ambientale, come la luce ambientale, non è direzionale. La reflection ambientale ha un impatto minore sul colore apparente di un oggetto sottoposto a rendering, ma influisce sul colore complessivo ed è più evidente quando una luce diffusa poco o nessuna riflette il materiale. La reflection ambientale di un materiale è influenzata dalla luce ambientale impostata per una scena chiamando il metodo [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con il \_ flag AMBIENT D3DRS.

La reflection diffusa e ambientale funzionano insieme per determinare il colore percepito di un oggetto e sono in genere valori identici. Ad esempio, per eseguire il rendering di un oggetto blu della sfera, si crea un materiale che riflette solo il componente blu della luce diffusa e ambientale. Quando viene posizionato in una stanza con una luce bianca, il cristallo sembra essere blu. Tuttavia, in una stanza con solo luce rossa, lo stesso cristallo apparirebbe nero, perché il materiale non riflette la luce rossa.

## <a name="emission"></a>Emissione

I materiali possono essere usati per fare in modo che un oggetto di cui è stato eseguito il rendering sia auto-lumineso. Il membro Emissive della [**struttura D3DMATERIAL9**](d3dmaterial9.md) viene usato per descrivere il colore e la trasparenza della luce emessa. L'emissione influisce sul colore di un oggetto e può, ad esempio, rendere più chiaro un materiale scuro e assumere parte del colore emesso.

È possibile usare la proprietà emissiva di un materiale per aggiungere l'effetto che un oggetto sta emettendo luce, senza incorrere nell'overhead di calcolo dovuto all'aggiunta di una luce alla scena. Nel caso del cristallo blu, la proprietà emissiva è utile se si vuole far apparire il cristallo in luce, ma non proiettare luce su altri oggetti nella scena. Tenere presente che i materiali con proprietà emissive non emettono luce che può essere riflessa da altri oggetti in una scena. Per ottenere questa luce riflessa, è necessario posizionare una luce aggiuntiva all'interno della scena.

## <a name="specular-reflection"></a>Reflection speculare

La reflection speculare crea evidenziazioni sugli oggetti, rendendoli molto luminosi. La [**struttura D3DMATERIAL9**](d3dmaterial9.md) contiene due membri che descrivono il colore di evidenziazione speculare e la luminosità complessiva del materiale. È possibile stabilire il colore delle evidenziazioni speculari impostando il membro Specular sul colore RGBA desiderato. I colori più comuni sono il bianco o il grigio chiaro. I valori impostati nel membro Power controllano la nitidezza degli effetti speculari.

Le evidenziazioni speculari possono creare effetti notevoli. Disegnando di nuovo sull'analogia blu del cristallo: un valore di Potenza maggiore crea evidenziazioni speculari più nitide, facendo sembrare il cristallo piuttosto chiaro. I valori più piccoli aumentano l'area dell'effetto, creando un effetto di riflessione che rende l'aspetto del cristallo insoddibile. Per rendere un oggetto realmente opaco, impostare il membro Power su zero e il colore in Specular (Speculare) su nero. Sperimentare diversi livelli di reflection per produrre un aspetto realistico per le proprie esigenze. Nella figura seguente vengono illustrati due modelli identici. Quella a sinistra usa una potenza di reflection speculare di 10; il modello a destra non ha reflection speculare.

![illustrazione di modelli di reflection speculari](images/spechigh.png)

## <a name="setting-material-properties"></a>Impostazione delle proprietà dei materiali

I dispositivi di rendering Direct3D possono eseguire il rendering con un set di proprietà materiale alla volta.

In un'applicazione C++ è possibile impostare le proprietà del materiale utilizzate dal sistema preparando una struttura [**D3DMATERIAL9**](d3dmaterial9.md) e quindi chiamando il [**metodo IDirect3DDevice9::SetMaterial.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)

Per preparare la [**struttura D3DMATERIAL9 per**](d3dmaterial9.md) l'uso, impostare le informazioni sulla proprietà nella struttura per creare l'effetto desiderato durante il rendering. Nell'esempio di codice seguente viene impostata la **struttura D3DMATERIAL9** per un materiale viola con evidenziazioni speculari di colore bianco acuto.


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



Dopo aver preparato [**la struttura D3DMATERIAL9,**](d3dmaterial9.md) applicare le proprietà chiamando il metodo [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) del dispositivo di rendering. Questo metodo accetta l'indirizzo di una struttura **D3DMATERIAL9 preparata** come unico parametro. È possibile chiamare **IDirect3DDevice9::SetMaterial** con le nuove informazioni necessarie per aggiornare le proprietà dei materiali per il dispositivo. Nell'esempio di codice seguente viene illustrato l'aspetto che può avere nel codice.


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



Quando si crea un dispositivo Direct3D, il materiale corrente viene impostato automaticamente sul valore predefinito illustrato nella tabella seguente.



| Membro   | Valore                |
|----------|----------------------|
| Diffusa  | (R:0, G:0, B:0, A:0) |
| Speculare | (R:0, G:0, B:0, A:0) |
| Di ambiente  | (R:0, G:0, B:0, A:0) |
| Emissiva | (R:0, G:0, B:0, A:0) |
| Elettricità    | (0.0)                |



 

## <a name="retrieving-material-properties"></a>Recupero delle proprietà dei materiali

È possibile recuperare le proprietà materiali attualmente in uso nel dispositivo di rendering chiamando il metodo [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) per il dispositivo. A differenza [**del metodo IDirect3DDevice9::SetMaterial,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) **IDirect3DDevice9::GetMaterial** non richiede la preparazione. Il **metodo IDirect3DDevice9::GetMaterial** accetta l'indirizzo di una struttura [**D3DMATERIAL9**](d3dmaterial9.md) e inserisce nella struttura fornita informazioni che descrivono le proprietà dei materiali correnti prima della restituzione.


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> Se l'applicazione non specifica le proprietà dei materiali per il rendering, il sistema usa un materiale predefinito. Il materiale predefinito riflette tutta la luce diffusa, ad esempio il bianco, senza riflessi ambientali o speculari e senza colore emissivo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 
