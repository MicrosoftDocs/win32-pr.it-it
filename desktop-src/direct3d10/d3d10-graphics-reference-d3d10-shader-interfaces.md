---
description: 'Questa sezione contiene informazioni sulle interfacce shader seguenti:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfacce shader (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483397"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Interfacce shader (grafica Direct3D 10)

Questa sezione contiene informazioni sulle interfacce shader seguenti:

Ognuna di queste interfacce shader gestisce uno shader compilato. L'interfaccia viene creata quando viene compilato uno shader e viene quindi passata a diverse API che necessitano dell'accesso a uno shader compilato. ad esempio quando si associa uno shader a una fase della pipeline o si recupera una firma dello shader.



| Interfacce di Pipeline-Stage                                      | Descrizione                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia ID3D10GeometryShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Un geometry shader implementa l'elaborazione per primitiva nella [fase geometry-shader](d3d10-graphics-programming-guide-pipeline-stages.md). |
| [**Interfaccia ID3D10PixelShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Un pixel shader implementa l'elaborazione per pixel nella [fase pixel shader](d3d10-graphics-programming-guide-pipeline-stages.md).           |
| [**Interfaccia ID3D10VertexShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Un vertex shader implementa l'elaborazione per vertice nella [fase vertex shader](d3d10-graphics-programming-guide-pipeline-stages.md).        |



 

Shader: le interfacce di Reflection consentono a un'applicazione di ispezionare il contenuto di uno shader in fase di progettazione/creazione. La reflection dello shader non è utile per impostare le variabili in fase di esecuzione perché è un mirror dei dati dello shader e pertanto non supporta alcun metodo per l'impostazione dei dati.



| Interfacce di Shader-Reflection                                                                   | Descrizione                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Interfaccia ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Interfaccia COM per la lettura di informazioni da uno shader compilato in fase di creazione.     |
| [**Interfaccia ID3D10ShaderReflectionConstantBuffer**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Interfaccia di supporto per ottenere un'interfaccia del buffer costante di Reflection shader.      |
| [**Interfaccia ID3D10ShaderReflectionType**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Interfaccia di supporto per ottenere un'interfaccia shader-reflection-Type.                 |
| [**Interfaccia ID3D10ShaderReflectionVariable**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Interfaccia di supporto per ottenere un'interfaccia shader-Reflection-variable.             |
| [**Interfaccia ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Interfaccia di Reflection shader per la lettura di informazioni da una visualizzazione risorse shader. |



 

Le API di Reflection dello shader implementano un'interfaccia di Reflection COM shader ([**interfaccia ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) e diverse interfacce Helper non com (il resto delle interfacce). L' **interfaccia ID3D10ShaderReflection** viene creata quando viene creato un oggetto di Reflection dello shader. Segue le regole COM standard; la creazione dell'interfaccia aumenta un conteggio dei riferimenti e l'interfaccia deve essere rilasciata quando non è più necessaria. Le interfacce di Reflection shader rimanenti sono interfacce helper che non ereditano da IUnknown. Ciò significa che non modificano il conteggio dei riferimenti quando vengono creati e non è necessario eliminarli definitivamente al termine dell'operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento shader](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
