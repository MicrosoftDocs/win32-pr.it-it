---
title: 'Interfacce shader (grafica Direct3D 11) '
description: Questa sezione contiene informazioni sulle interfacce shader.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfacce, Shader Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcecdff6f35b634ecbbeca0b85bc5ba42fd1e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479457"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a>Interfacce shader (grafica Direct3D 11) 

Questa sezione contiene informazioni sulle interfacce shader.

Ognuna di queste interfacce shader gestisce uno shader compilato. L'interfaccia viene creata quando viene compilato uno shader e quindi passata a varie API che devono accedere a uno shader compilato; ad esempio quando si associa uno shader a una fase della pipeline o si riceve una firma dello shader.


## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a><br /> | Questa interfaccia incapsula una classe HLSL.<br /> | 
| <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a><br /> | Questa interfaccia incapsula un collegamento dinamico HLSL.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a><br /> | Un'interfaccia compute-shader gestisce un programma eseguibile (uno shader di calcolo) che controlla la fase compute-shader.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a><br /> | Un'interfaccia domain-shader gestisce un programma eseguibile (uno shader di dominio) che controlla la fase domain-shader.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a><br /> | Un'interfaccia function-linking-graph viene usata per costruire shader costituiti da una sequenza di chiamate di funzione precompilate che passano valori tra loro. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a><br /> | Un'interfaccia function-reflection accede alle informazioni sulla funzione. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a><br /> | Un'interfaccia function-parameter-reflection accede alle informazioni sui parametri di funzione. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a><br /> | Un'interfaccia geometry shader gestisce un programma eseguibile (uno shader geometry) che controlla la fase geometry-shader.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a><br /> | Un'interfaccia hull-shader gestisce un programma eseguibile (uno hull shader) che controlla la fase hull-shader.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a><br /> | Un'interfaccia di reflection della libreria accede alle informazioni della libreria. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a><br /> | Un'interfaccia del linker viene usata per collegare un modulo shader. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a><br /> | Per il collegamento shader viene usata un'interfaccia del nodo di collegamento. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a><br /> | Un'interfaccia del modulo crea un'istanza di un modulo usata per il riassociazione delle risorse. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a><br /> | Per il riassociazione delle risorse viene usata un'interfaccia di istanza del modulo. <br /><blockquote>[!Note]<br />Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, crearne il pacchetto in librerie e collegarle a shader completi in fase di esecuzione.</blockquote><br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a><br /> | Un'interfaccia pixel shader gestisce un programma eseguibile (pixel shader) che controlla la fase del pixel shader.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a><br /> | Un'interfaccia di reflection shader accede alle informazioni dello shader.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a><br /> | Questa interfaccia shader-reflection fornisce l'accesso a un buffer costante.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a><br /> | Questa interfaccia di reflection shader fornisce l'accesso al tipo di variabile.<br /> | 
| <a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a><br /> | Questa interfaccia di reflection shader fornisce l'accesso a una variabile.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a><br /> | <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>Un'interfaccia ID3D11ShaderTrace</strong></a> implementa metodi per ottenere tracce di esecuzioni di shader.<br /> | 
| <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a><br /> | <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>Un'interfaccia ID3D11ShaderTraceFactory</strong></a> implementa un metodo per la generazione di oggetti di informazioni di traccia shader.<br /> | 
| <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a><br /> | Un'interfaccia vertex shader gestisce un programma eseguibile (vertex shader) che controlla la fase vertex shader.<br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su shader](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

