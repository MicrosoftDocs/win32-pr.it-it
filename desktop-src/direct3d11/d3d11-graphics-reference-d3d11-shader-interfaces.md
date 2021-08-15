---
title: 'Interfacce shader (grafica Direct3D 11) '
description: Questa sezione contiene informazioni sulle interfacce dello shader.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfacce, shader Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6c3d628f83747831dae0e98bd604f88f9ee0946aeb56a38c9734df30ba0d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988481"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Interfacce shader (grafica Direct3D 11) 

Questa sezione contiene informazioni sulle interfacce dello shader.

Ognuna di queste interfacce shader gestisce uno shader compilato. L'interfaccia viene creata quando viene compilato uno shader e quindi passata a diverse API che devono accedere a uno shader compilato. ad esempio quando si associa uno shader a una fase della pipeline o si riceve una firma dello shader.


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
<td>Un'interfaccia compute shader gestisce un programma eseguibile (compute shader) che controlla la fase compute shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br/></td>
<td>Un'interfaccia domain-shader gestisce un programma eseguibile (domain shader) che controlla la fase domain-shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br/></td>
<td>Un'interfaccia function-linking-graph viene usata per costruire shader costituiti da una sequenza di chiamate di funzione precompilate che passano valori tra loro. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br/></td>
<td>Un'interfaccia di reflection di funzione accede alle informazioni sulla funzione. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br/></td>
<td>Un'interfaccia function-parameter-reflection accede alle informazioni sui parametri di funzione. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br/></td>
<td>Un'interfaccia geometry shader gestisce un programma eseguibile (geometry shader) che controlla la fase geometry shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br/></td>
<td>Un'interfaccia di tipo hull shader gestisce un programma eseguibile (uno hull shader) che controlla la fase di hull shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br/></td>
<td>Un'interfaccia di reflection della libreria accede alle informazioni sulla libreria. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br/></td>
<td>Un'interfaccia del linker viene usata per collegare un modulo shader. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br/></td>
<td>Un'interfaccia del nodo di collegamento viene usata per il collegamento dello shader. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br/></td>
<td>Un'interfaccia del modulo crea un'istanza di un modulo usato per il riassociazione delle risorse. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br/></td>
<td>Un'interfaccia dell'istanza del modulo viene usata per la riassociazione delle risorse. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br/></td>
<td>Un'interfaccia pixel shader gestisce un programma eseguibile (un pixel shader) che controlla la fase del pixel shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br/></td>
<td>Un'interfaccia di reflection shader accede alle informazioni dello shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br/></td>
<td>Questa interfaccia di reflection shader fornisce l'accesso a un buffer costante.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br/></td>
<td>Questa interfaccia di reflection shader fornisce l'accesso al tipo di variabile.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br/></td>
<td>Questa interfaccia di reflection shader fornisce l'accesso a una variabile.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br/></td>
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>Un'interfaccia ID3D11ShaderTrace</strong></a> implementa i metodi per ottenere tracce delle esecuzioni dello shader.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br/></td>
<td><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>Un'interfaccia ID3D11ShaderTraceFactory</strong></a> implementa un metodo per la generazione di oggetti di informazioni di traccia shader.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br/></td>
<td>Un'interfaccia vertex shader gestisce un programma eseguibile (vertex shader) che controlla la fase vertex shader.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento per lo shader](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

