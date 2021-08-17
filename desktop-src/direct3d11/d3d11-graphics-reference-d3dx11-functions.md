---
title: Funzioni D3DX (grafica Direct3D 11)
description: Questa sezione contiene informazioni sulle funzioni D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- funzioni, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b4c98dda5f85f03af1add120d22b95fa620d4a45e8e4db80d3b607f2c3e70e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126055"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a>Funzioni D3DX (grafica Direct3D 11)

Questa sezione contiene informazioni sulle funzioni D3DX 11.

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.

 


## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il compilatore della riga di comando di Fxc.exe o usare una delle API di compilazione HLSL, come l'API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile.</strong></a>
</blockquote>
<br/> Compilare uno shader o un effetto da un file.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il compilatore della riga di comando di Fxc.exe o usare una delle API di compilazione HLSL, ad esempio <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>l'API D3DCompile.</strong></a>
</blockquote>
<br/> Compilare uno shader o un effetto caricato in memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Invece di usare questa funzione, è consigliabile usare le funzioni di risorsa <a href="/windows/desktop/menurc/resources-functions">,</a>quindi eseguire la compilazione offline usando il compilatore della riga di comando di Fxc.exe o usare una delle API di compilazione HLSL, ad esempio l'API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile.</strong></a>
</blockquote>
<br/> Compilare uno shader o un effetto da una risorsa.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Invece di usare questa funzione, è consigliabile usare la <a href="https://github.com/Microsoft/DirectXTex">libreria DirectXTex,</a> <strong>ComputeNormalMap.</strong>
</blockquote>
<br/> Converte una mappa di altezza in una mappa normale. I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un processore di dati asincrono per uno shader.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un caricatore di file asincrono.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un caricatore di memoria asincrona.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un caricatore di risorse asincrono.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un processore di dati per uno shader in modo asincrono.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un processore di dati da usare con un <a href="id3dx11threadpump.md"><strong>thread pump.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un processore di dati da usare con un <a href="id3dx11threadpump.md"><strong>thread pump.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un processore di dati che carica una risorsa e quindi crea una visualizzazione shader-risorsa per essa. I processori di dati sono un componente della funzionalità di caricamento asincrono dei dati in D3DX11 che usa <a href="id3dx11threadpump.md"><strong>i thread pump.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Invece di usare questa funzione, è consigliabile usare:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Libreria DirectXTK</a> (runtime), <strong>CreateXXXTextureFromFile</strong> (dove XXX è DDS o WIC)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Libreria DirectXTex</a> (strumenti), <strong>LoadFromXXXFile</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Creare una visualizzazione shader-risorsa da un file.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Invece di usare questa funzione, è consigliabile usare:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Libreria DirectXTK</a> (runtime), <strong>CreateXXXTextureFromMemory</strong> (dove XXX è DDS o WIC)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Libreria DirectXTex</a> (strumenti), <strong>LoadFromXXXMemory</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Creare una visualizzazione shader-risorsa da un file in memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Invece di usare questa funzione, è consigliabile usare le <a href="/windows/desktop/menurc/resources-functions">funzioni di risorsa</a>, quindi:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Libreria DirectXTK</a> (runtime), <strong>CreateXXXTextureFromMemory</strong> (dove XXX è DDS o WIC)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Libreria DirectXTex</a> (strumenti), <strong>LoadFromXXXMemory</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Creare una visualizzazione shader-risorsa da una risorsa.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Invece di usare questa funzione, è consigliabile usare:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Libreria DirectXTK</a> (runtime), <strong>CreateXXXTextureFromFile</strong> (dove XXX è DDS o WIC)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Libreria DirectXTex</a> (strumenti), <strong>LoadFromXXXFile</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Creare una risorsa trama da un file.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Invece di usare questa funzione, è consigliabile usare:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Libreria DirectXTK</a> (runtime), <strong>CreateXXXTextureFromMemory</strong> (dove XXX è DDS o WIC)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Libreria DirectXTex</a> (strumenti), <strong>LoadFromXXXMemory</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Creare una risorsa trama da un file che risiede nella memoria di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Invece di usare questa funzione, è consigliabile usare le <a href="/windows/desktop/menurc/resources-functions">funzioni di risorsa</a>, quindi:</p>
<ul>
<li><a href="https://github.com/Microsoft/DirectXTK">Libreria DirectXTK</a> (runtime), <strong>CreateXXXTextureFromMemory</strong> (dove XXX è DDS o WIC)</li>
<li><a href="https://github.com/Microsoft/DirectXTex">Libreria DirectXTex</a> (strumenti), <strong>LoadFromXXXMemory</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi) quindi <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Creare una trama da un'altra risorsa.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare una pompa di thread.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare la <a href="https://github.com/Microsoft/DirectXTex">libreria DirectXTex,</a> <strong>GenerateMipMaps</strong> e <strong>GenerateMipMaps3D.</strong>
</blockquote>
<br/> Genera una catena mipmap usando un filtro di trama specifico.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare la <a href="https://github.com/Microsoft/DirectXTex">libreria DirectXTex,</a> <strong>GetMetadataFromXXXFile</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi.
</blockquote>
<br/> Recupera informazioni su un file di immagine specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex,</a> <strong>GetMetadataFromXXXMemory</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi.
</blockquote>
<br/> Ottenere informazioni su un'immagine già caricata in memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare le funzioni di risorsa <a href="/windows/desktop/menurc/resources-functions">,</a>quindi usare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LoadFromXXXMemory</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi.
</blockquote>
<br/> Recupera informazioni su una determinata immagine in una risorsa.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex,</a> <strong>Resize,</strong> <strong>Convert</strong>, <strong>Compress,</strong> <strong>Decompress</strong>e/o <strong>CopyRectangle</strong>.
</blockquote>
<br/> Caricare una trama da una trama.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess.</strong></a>
</blockquote>
<br/> Creare uno shader da un file senza compilarlo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess.</strong></a>
</blockquote>
<br/> Creare uno shader dalla memoria senza compilarlo.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess.</strong></a>
</blockquote>
<br/> Creare uno shader da una risorsa senza compilarlo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare la <a href="https://github.com/Microsoft/DirectXTex">libreria DirectXTex,</a> <strong>CaptureTexture</strong> e <strong>SaveToXXXFile</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi. Per lo scenario semplificato di creazione di una schermata da una trama di destinazione di rendering, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK,</a> <strong>SaveDDSTextureToFile</strong> o <strong>SaveWICTextureToFile.</strong>
</blockquote>
<br/> Salvare una trama in un file.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex,</a> <strong>CaptureTexture</strong> e <strong>SaveToXXXMemory</strong> (dove XXX è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine grafica comune per i giochi.
</blockquote>
<br/> Salvare una trama in memoria.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare la <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">libreria matematica Spherical Harmonics,</a> <strong>SHProjectCubeMap.</strong>
</blockquote>
<br/> Proietta una funzione rappresentata in una mappa del cubo in armonici sferici.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché usare questa funzione, è consigliabile usare il <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>metodo ID3D11DeviceContext::ClearState.</strong></a>
</blockquote>
<br/> Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su <strong>NULL.</strong> Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurarsi che, quando si rilasciano tutte le risorse, nessuna di esse sia associata al dispositivo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

