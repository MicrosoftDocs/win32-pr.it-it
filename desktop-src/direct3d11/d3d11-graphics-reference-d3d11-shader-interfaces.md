---
title: 'Interfacce shader (grafica Direct3D 11) '
description: Questa sezione contiene informazioni sulle interfacce dello shader.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfacce, Direct3D 11 shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55e591d56442b641482a76a4ec93c0055029fc0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400119"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Interfacce shader (grafica Direct3D 11) 

Questa sezione contiene informazioni sulle interfacce dello shader.

Ognuna di queste interfacce shader gestisce uno shader compilato. L'interfaccia viene creata quando viene compilato uno shader e viene quindi passata a diverse API che necessitano dell'accesso a uno shader compilato. ad esempio quando si associa uno shader a una fase della pipeline o si recupera una firma dello shader.


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
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br/></td>
<td>Questa interfaccia incapsula una classe HLSL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br/></td>
<td>Questa interfaccia incapsula un collegamento dinamico HLSL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br/></td>
<td>Un'interfaccia compute shader gestisce un programma eseguibile (Compute Shader) che controlla la fase compute shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br/></td>
<td>Un'interfaccia di shader Domain gestisce un programma eseguibile (un Domain shader) che controlla la fase del dominio shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br/></td>
<td>Per costruire shader costituiti da una sequenza di chiamate di funzione precompilate che passano i valori tra loro, viene utilizzata un'interfaccia Graph di collegamento a funzioni. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br/></td>
<td>Un'interfaccia di reflection di funzione accede alle informazioni sulla funzione. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br/></td>
<td>Un'interfaccia function-parameter-Reflection accede alle informazioni sul parametro della funzione. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br/></td>
<td>Un'interfaccia geometry shader gestisce un programma eseguibile (Geometry shader) che controlla la fase geometry-shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br/></td>
<td>Un'interfaccia Hull shader gestisce un programma eseguibile (uno scafo) che controlla la fase Hull shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br/></td>
<td>Un'interfaccia di reflection di libreria accede alle informazioni della libreria. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br/></td>
<td>Viene usata un'interfaccia del linker per collegare un modulo shader. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br/></td>
<td>Per il collegamento dello shader viene utilizzata un'interfaccia del nodo di collegamento. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br/></td>
<td>Un'interfaccia del modulo crea un'istanza di un modulo usato per la riassociazione delle risorse. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br/></td>
<td>Per la riassociazione delle risorse viene usata un'interfaccia di istanza modulo. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br/></td>
<td>Un'interfaccia pixel shader gestisce un programma eseguibile (un pixel shader) che controlla la fase pixel shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br/></td>
<td>Un'interfaccia di Reflection shader accede alle informazioni sullo shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Questa interfaccia di Reflection shader fornisce l'accesso a un buffer costante.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br/></td>
<td>Questa interfaccia di Reflection shader consente di accedere al tipo di variabile.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br/></td>
<td>Questa interfaccia di Reflection shader consente di accedere a una variabile.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br/></td>
<td>Un'interfaccia <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> implementa i metodi per ottenere tracce di esecuzioni dello shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br/></td>
<td>Un'interfaccia <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> implementa un metodo per la generazione di oggetti di informazioni di traccia dello shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br/></td>
<td>Un'interfaccia vertex shader gestisce un programma eseguibile (Vertex shader) che controlla la fase vertex shader.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento shader](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

