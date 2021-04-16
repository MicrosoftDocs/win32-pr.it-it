---
description: I materiali descrivono il modo in cui i poligoni riflettono la luce o sembrano emettere luce in una scena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materiali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558073"
---
# <a name="materials-direct3d-9"></a>Materiali (Direct3D 9)

I materiali descrivono il modo in cui i poligoni riflettono la luce o sembrano emettere luce in una scena 3D. Le proprietà del materiale illustrano in dettaglio la reflection diffusa del materiale, la reflection ambiente, le emissioni chiare e le caratteristiche di evidenziazione speculare. Direct3D usa la struttura [**D3DMATERIAL9**](d3dmaterial9.md) per contenere tutte le informazioni sulle proprietà del materiale. Fatta eccezione per la proprietà speculare, ogni proprietà viene descritta come un colore RGBA che rappresenta la quantità di parti rosse, verdi e blu di un determinato tipo di luce che riflette e un fattore di fusione alfa.

## <a name="diffuse-and-ambient-reflection"></a>Reflection diffusa e di ambiente

I membri diffusi e di ambiente della struttura [**D3DMATERIAL9**](d3dmaterial9.md) descrivono in che modo un materiale riflette l'ambiente e diffonde la luce in una scena. Poiché la maggior parte delle scene contiene una luce molto più diffusa rispetto alla luce ambientale, la reflection diffusa riproduce la parte più ampia per determinare il colore. Inoltre, poiché la luce diffusa è direzionale, l'angolo di incidenza della luce diffusa influiscono sull'intensità complessiva della reflection. La reflection diffusa è maggiore quando la luce colpisce un vertice parallelo alla normale del vertice. Con l'aumentare dell'angolo, l'effetto della reflection diffusa diminuisce. La quantità di luce riflessa è il coseno dell'angolo tra la luce in arrivo e il vertice normale, come illustrato nella figura seguente.

![illustrazione della quantità di luce riflessa](images/incident.png)

La reflection di ambiente, ad esempio la luce di ambiente, non è direzionale. La reflection di ambiente ha un impatto minore sul colore apparente di un oggetto di cui è stato eseguito il rendering, ma influisce sul colore complessivo ed è più evidente quando poca o nessuna luce diffusa riflette il materiale. La reflection di ambiente di un materiale è interessata dal set di luce di ambiente per una scena chiamando il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con il \_ flag di ambiente D3DRS.

La reflection diffusa e di ambiente interagiscono per determinare il colore percepito di un oggetto e sono in genere valori identici. Ad esempio, per eseguire il rendering di un oggetto cristallino blu, si crea un materiale che riflette solo il componente blu di diffusione e luce ambientale. Quando viene inserita in una stanza con una luce bianca, il cristallo sembra essere blu. Tuttavia, in una stanza con solo luce rossa, lo stesso cristallo sembrerebbe nero, perché il materiale non riflette la luce rossa.

## <a name="emission"></a>Emissione

I materiali possono essere usati per fare in modo che un oggetto di cui è stato eseguito il rendering risulti con luminosità automatica. Il membro emissivo della struttura [**D3DMATERIAL9**](d3dmaterial9.md) viene usato per descrivere il colore e la trasparenza della luce emessa. L'emissione influiscono sul colore di un oggetto e può, ad esempio, rendere un materiale scuro più chiaro e assumere parte del colore emesso.

È possibile usare la proprietà emissivo di un materiale per aggiungere l'illusione che un oggetto emette la luce, senza incorrere nel sovraccarico computazionale dell'aggiunta di una luce alla scena. Nel caso del cristallo blu, la proprietà emissivo è utile se si vuole che il cristallo appaia chiaro, ma non viene eseguito il cast della luce sugli altri oggetti nella scena. Tenere presente che i materiali con proprietà emissivo non emettono luce che possono essere riflessi da altri oggetti in una scena. Per ottenere questa luce riflessa, è necessario inserire una luce aggiuntiva all'interno della scena.

## <a name="specular-reflection"></a>Reflection speculare

La reflection speculare crea evidenziazioni sugli oggetti, facendo in modo che vengano visualizzate lucide. La struttura [**D3DMATERIAL9**](d3dmaterial9.md) contiene due membri che descrivono il colore di evidenziazione speculare, nonché il lucentezza globale del materiale. Il colore delle evidenziazioni speculari viene stabilito impostando il membro speculare sul colore RGBA desiderato. i colori più comuni sono bianco o grigio chiaro. I valori impostati in Power membri controllano la nitidezza degli effetti speculari.

Le evidenziazioni speculari possono creare effetti drammatici. Disegno di nuovo in Blue Crystal analogy: un valore di potenza maggiore crea evidenziazioni speculari più nitide, rendendo il cristallo apparentemente chiaro. I valori più piccoli aumentano l'area dell'effetto, creando una reflection noiosa che rende l'aspetto cristallizzato. Per fare in modo che un oggetto sia effettivamente opaco, impostare il membro di alimentazione su zero e il colore da speculare a nero. Sperimentare diversi livelli di reflection per produrre un aspetto realistico per le proprie esigenze. Nella figura seguente vengono illustrati due modelli identici. Quello a sinistra usa una potenza di Reflection speculare di 10. il modello a destra non ha Reflection speculare.

![illustrazione dei modelli di Reflection speculare](images/spechigh.png)

## <a name="setting-material-properties"></a>Impostazione delle proprietà del materiale

I dispositivi di rendering Direct3D possono eseguire il rendering con un set di proprietà del materiale alla volta.

In un'applicazione C++ è possibile impostare le proprietà del materiale utilizzate dal sistema preparando una struttura [**D3DMATERIAL9**](d3dmaterial9.md) , quindi chiamando il metodo [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .

Per preparare la struttura [**D3DMATERIAL9**](d3dmaterial9.md) per l'uso, impostare le informazioni sulle proprietà nella struttura per creare l'effetto desiderato durante il rendering. Nell'esempio di codice seguente viene impostata la struttura **D3DMATERIAL9** per un materiale viola con evidenziazioni speculari bianche nitide.


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



Dopo aver preparato la struttura [**D3DMATERIAL9**](d3dmaterial9.md) , è necessario applicare le proprietà chiamando il metodo [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) del dispositivo di rendering. Questo metodo accetta l'indirizzo di una struttura **D3DMATERIAL9** predisposta come unico parametro. È possibile chiamare **IDirect3DDevice9:: sematerial** con le nuove informazioni necessarie per aggiornare le proprietà del materiale per il dispositivo. Nell'esempio di codice riportato di seguito viene illustrato come potrebbe apparire nel codice.


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



Quando si crea un dispositivo Direct3D, il materiale corrente viene impostato automaticamente sul valore predefinito indicato nella tabella seguente.



| Membro   | Valore                |
|----------|----------------------|
| Diffusa  | (R:0, G:0, B:0, A:0) |
| Speculare | (R:0, G:0, B:0, A:0) |
| Di ambiente  | (R:0, G:0, B:0, A:0) |
| Emissiva | (R:0, G:0, B:0, A:0) |
| Potenza    | (0,0)                |



 

## <a name="retrieving-material-properties"></a>Recupero delle proprietà del materiale

È possibile recuperare le proprietà del materiale utilizzate attualmente dal dispositivo di rendering chiamando il metodo [**IDirect3DDevice9:: getmaterial**](/windows/desktop/api) per il dispositivo. A differenza del metodo [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , **IDirect3DDevice9:: getmaterial** non richiede la preparazione. Il metodo **IDirect3DDevice9:: getmaterial** accetta l'indirizzo di una struttura [**D3DMATERIAL9**](d3dmaterial9.md) e riempie la struttura fornita con le informazioni che descrivono le proprietà Material correnti prima di restituire.


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
> Se l'applicazione non specifica le proprietà del materiale per il rendering, il sistema utilizza un materiale predefinito. Il materiale predefinito riflette tutto il bianco chiaro, ad esempio, senza reflection di ambiente o speculare e nessun colore emissivo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Luci e materiali](lights-and-materials.md)
</dt> </dl>

 

 
