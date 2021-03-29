---
title: Funzioni D3DX (grafica Direct3D 11)
description: Questa sezione contiene informazioni sulle funzioni D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- funzioni, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400062"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a>Funzioni D3DX (grafica Direct3D 11)

Questa sezione contiene informazioni sulle funzioni D3DX 11.

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 


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
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o una delle API di compilazione HLSL, ad esempio l'API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> .
</blockquote>
<br/> Compilare uno shader o un effetto da un file.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o una delle API di compilazione HLSL, ad esempio l'API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compilare uno shader o un effetto caricato in memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Invece di usare questa funzione, è consigliabile usare le <a href="/windows/desktop/menurc/resources-functions">funzioni di risorsa</a>, quindi compilare offline usando il Fxc.exe compilatore della riga di comando o usare una delle API di compilazione HLSL, ad esempio l'API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compilare uno shader o un effetto da una risorsa.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ComputeNormalMap</strong>.
</blockquote>
<br/> Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un processore di dati asincrono per uno shader.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un caricatore di file asincrono.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un caricatore di memoria asincrono.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un caricatore di risorse asincrono.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un elaboratore di dati per uno shader in modo asincrono.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un elaboratore di dati da utilizzare con una <a href="id3dx11threadpump.md"><strong>pompa di thread</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un elaboratore di dati da utilizzare con una <a href="id3dx11threadpump.md"><strong>pompa di thread</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
</blockquote>
<br/> Creare un elaboratore di dati che caricherà una risorsa e quindi crei una visualizzazione delle risorse shader. I processori di dati sono un componente della funzionalità asincrona di caricamento dei dati in D3DX11 che usa le <a href="id3dx11threadpump.md"><strong>pompe di thread</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</p>
<ul>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (dove xxx è DDS o WIC)</li>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Creare una visualizzazione risorse shader da un file.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</p>
<ul>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</li>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Creare una visualizzazione risorse shader da un file in memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della <a href="/windows/desktop/menurc/resources-functions">risorsa</a>, quindi:</p>
<ul>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</li>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Creare una visualizzazione risorse shader da una risorsa.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</p>
<ul>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (dove xxx è DDS o WIC)</li>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>createTexture</strong></li>
</ul>
</blockquote>
<br/> Creare una risorsa di trama da un file.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</p>
<ul>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</li>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>createTexture</strong></li>
</ul>
</blockquote>
<br/> Creare una risorsa di trama da un file che risiede nella memoria di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della <a href="/windows/desktop/menurc/resources-functions">risorsa</a>, quindi:</p>
<ul>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</li>
<li>Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>createTexture</strong></li>
</ul>
</blockquote>
<br/> Creare una trama da un'altra risorsa.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni.
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
Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GenerateMipMaps</strong> e <strong>GenerateMipMaps3D</strong>.
</blockquote>
<br/> Genera la catena mipmap usando un filtro di trama particolare.<br/></td>
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
Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.
</blockquote>
<br/> Recupera le informazioni su un file di immagine specificato.<br/></td>
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
Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.
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
Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della <a href="/windows/desktop/menurc/resources-functions">risorsa</a>, quindi utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.
</blockquote>
<br/> Recupera le informazioni su una determinata immagine in una risorsa.<br/></td>
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
Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ridimensionare</strong>, <strong>convertire</strong>, <strong>comprimere</strong>, <strong>decomprimere</strong>e/o <strong>CopyRectangle</strong>.
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
Invece di usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
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
Invece di usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
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
Invece di usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
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
Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> quindi <strong>SAVETOXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi. Per lo scenario semplificato della creazione di una schermata da una trama di destinazione di rendering, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> , <strong>SaveDDSTextureToFile</strong> o <strong>SaveWICTextureToFile</strong>.
</blockquote>
<br/> Salva una trama in un file.<br/></td>
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
Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> quindi <strong>SAVETOXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.
</blockquote>
<br/> Salva una trama in memoria.<br/></td>
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
Invece di usare questa funzione, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">matematica delle armoniche sferiche</a> <strong>SHProjectCubeMap</strong>.
</blockquote>
<br/> Proietta una funzione rappresentata in una mappa cubo in armoniche sferiche.<br/></td>
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
Invece di usare questa funzione, è consigliabile usare il metodo <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>sul ID3D11DeviceContext:: ClearState</strong></a> .
</blockquote>
<br/> Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su <strong>null</strong>. Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurare che, quando si rilasciano tutte le relative risorse, nessuna delle quali è associata al dispositivo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

