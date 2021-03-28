---
title: Come eseguire l'istanza di un geometry shader
description: La creazione di istanze di Geometry shader consente l'esecuzione di più esecuzioni dello stesso geometry shader per primitive.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992840"
---
# <a name="how-to-instance-a-geometry-shader"></a><span data-ttu-id="dda6b-103">Procedura: eseguire l'istanza di un geometry shader</span><span class="sxs-lookup"><span data-stu-id="dda6b-103">How To: Instance a Geometry Shader</span></span>

<span data-ttu-id="dda6b-104">La creazione di istanze di Geometry shader consente l'esecuzione di più esecuzioni dello stesso geometry shader per primitive.</span><span class="sxs-lookup"><span data-stu-id="dda6b-104">Geometry shader instancing allows multiple executions of the same geometry shader to be executed per primitive.</span></span> <span data-ttu-id="dda6b-105">Per eseguire l'istanza di un geometry shader, aggiungere un attributo instance alla funzione shader principale e identificare un parametro di indice dell'istanza nel corpo della funzione shader.</span><span class="sxs-lookup"><span data-stu-id="dda6b-105">To instance a geometry shader, add an instance attribute to the main shader function and identify an instance index parameter in the shader function body.</span></span>

<span data-ttu-id="dda6b-106">Per l'istanza di un geometry shader:</span><span class="sxs-lookup"><span data-stu-id="dda6b-106">To Instance a Geometry Shader:</span></span>

1.  <span data-ttu-id="dda6b-107">Aggiungere l' [attributo instance](sm5-attributes-instance.md) alla funzione Main.</span><span class="sxs-lookup"><span data-stu-id="dda6b-107">Add the [instance attribute](sm5-attributes-instance.md) to the main function.</span></span>

    ```
    [instance(24)]
    ```

    

    <span data-ttu-id="dda6b-108">Definisce il numero di istanze (un massimo di 32) da eseguire per ogni primitiva.</span><span class="sxs-lookup"><span data-stu-id="dda6b-108">This defines the number of instances (a maximum of 32) to be run for each primitive.</span></span>

2.  <span data-ttu-id="dda6b-109">Alleghi il valore del sistema [SV \_ GSInstanceID](sv-gsinstanceid.md) a una variabile nell'elenco dei parametri della funzione che può essere usata per tenere traccia dell'ID dell'istanza in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dda6b-109">Attach the [SV\_GSInstanceID](sv-gsinstanceid.md) system value to a variable in the function parameter list that can be used to track the ID of the instance being executed.</span></span>
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  <span data-ttu-id="dda6b-110">Compilare e creare lo shader Analogamente a qualsiasi altro geometry shader.</span><span class="sxs-lookup"><span data-stu-id="dda6b-110">Compile and create the shader just as you would any other geometry shader.</span></span>

<span data-ttu-id="dda6b-111">Altri dettagli includono:</span><span class="sxs-lookup"><span data-stu-id="dda6b-111">Other details include:</span></span>

-   <span data-ttu-id="dda6b-112">Il numero massimo di istanze è 32.</span><span class="sxs-lookup"><span data-stu-id="dda6b-112">The maximum instance count is 32.</span></span>
-   <span data-ttu-id="dda6b-113">Il numero massimo di vertici è un numero massimo di vertici per istanza.</span><span class="sxs-lookup"><span data-stu-id="dda6b-113">The maximum vertex count is a per-instance maximum vertex count.</span></span>
-   <span data-ttu-id="dda6b-114">Ogni chiamata di istanza, come qualsiasi chiamata a geometry shader, aumenta il numero di chiamate e genera un RestartStrip implicito ().</span><span class="sxs-lookup"><span data-stu-id="dda6b-114">Each instance invocation (like any geometry shader invocation) increases the invocation count and generates an implicit RestartStrip().</span></span>

## <a name="related-topics"></a><span data-ttu-id="dda6b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dda6b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dda6b-116">Funzionalità di Geometry shader</span><span class="sxs-lookup"><span data-stu-id="dda6b-116">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




