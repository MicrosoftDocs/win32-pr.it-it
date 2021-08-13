---
description: 'Questa sezione contiene informazioni sulle interfacce shader seguenti:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfacce shader (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96962407492f5fc6b6f7bbacd155c265ffd03e11eff31f2b012a2d1c644d3f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409151"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Interfacce shader (grafica Direct3D 10)

Questa sezione contiene informazioni sulle interfacce shader seguenti:

Ognuna di queste interfacce shader gestisce uno shader compilato. L'interfaccia viene creata quando viene compilato uno shader e quindi passata a varie API che devono accedere a uno shader compilato; ad esempio quando si associa uno shader a una fase della pipeline o si riceve una firma dello shader.



| Pipeline-Stage interfacce                                      | Descrizione                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia ID3D10GeometryShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Uno shader geometry implementa l'elaborazione per primitiva nella [fase geometry-shader.](d3d10-graphics-programming-guide-pipeline-stages.md) |
| [**Interfaccia ID3D10PixelShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Un pixel shader implementa l'elaborazione per pixel nella [fase del pixel shader.](d3d10-graphics-programming-guide-pipeline-stages.md)           |
| [**Interfaccia ID3D10VertexShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Un vertex shader implementa l'elaborazione per vertice nella [fase vertex shader](d3d10-graphics-programming-guide-pipeline-stages.md).        |



 

Le interfacce di reflection shader consentono a un'applicazione di esaminare il contenuto di uno shader in fase di progettazione/autore. La reflection dello shader non è utile per l'impostazione delle variabili in fase di esecuzione perché è un mirror dei dati dello shader e pertanto non supporta metodi per l'impostazione dei dati.



| Shader-Reflection interfacce                                                                   | Descrizione                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Interfaccia ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Interfaccia COM per la lettura di informazioni da uno shader compilato in fase di creazione.     |
| [**Interfaccia ID3D10ShaderReflectionConstantBuffer**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Interfaccia helper per ottenere un'interfaccia constant-buffer shader-reflection.      |
| [**Interfaccia ID3D10ShaderReflectionType**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Interfaccia helper per ottenere un'interfaccia shader-reflection-type.                 |
| [**Interfaccia ID3D10ShaderReflectionVariable**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Interfaccia helper per ottenere un'interfaccia shader-reflection-variable.             |
| [**Interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Interfaccia shader-reflection per la lettura di informazioni da una visualizzazione shader-risorsa. |



 

Le API di reflection shader implementano un'interfaccia di reflection com shader ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) e diverse interfacce helper non COM (le altre interfacce). **L'interfaccia ID3D10ShaderReflection** viene creata quando viene creato un oggetto reflection shader. Segue le regole COM standard. La creazione dell'interfaccia aumenta un conteggio dei riferimenti e l'interfaccia deve essere rilasciata quando non è più necessaria. Le interfacce shader-reflection rimanenti sono interfacce helper che non ereditano da IUnknown. Ciò significa che non modificano alcun conteggio dei riferimenti quando vengono creati e non devono essere distrutti al termine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su shader](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
