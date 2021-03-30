---
title: Archiviazione di variabili e tipi per gli shader da condividere
description: L'oggetto collegamento di classe è uno spazio dei nomi per variabili e tipi che possono essere condivisi da più shader.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976823"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a><span data-ttu-id="61204-103">Archiviazione di variabili e tipi per gli shader da condividere</span><span class="sxs-lookup"><span data-stu-id="61204-103">Storing Variables and Types for Shaders to Share</span></span>

<span data-ttu-id="61204-104">L'oggetto collegamento di classe è uno spazio dei nomi per variabili e tipi che possono essere condivisi da più shader.</span><span class="sxs-lookup"><span data-stu-id="61204-104">The class linkage object is a namespace for variables and types that multiple shaders can share.</span></span> <span data-ttu-id="61204-105">Quando si passa un oggetto collegamento di classe in una chiamata per creare uno shader, il runtime raccoglie un elenco di variabili e tipi che possono implementare ogni interfaccia nello shader e archivia i nomi di tali variabili e tipi nell'oggetto del collegamento alla classe.</span><span class="sxs-lookup"><span data-stu-id="61204-105">When you pass a class linkage object in a call to create a shader, the runtime gathers a list of variables and types that can implement each interface in the shader and stores the names of those variables and types in the class linkage object.</span></span>

<span data-ttu-id="61204-106">Pertanto, quando si chiama il metodo [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) per generare istanze di classe dall'oggetto del collegamento alla classe, il runtime può recuperare la variabile o il tipo che corrisponde al nome fornito in ogni shader (se tale nome è valido per un determinato shader) e che viene creato con l'oggetto del collegamento alla classe specificato.</span><span class="sxs-lookup"><span data-stu-id="61204-106">Therefore, when you call the [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) method to generate class instances from the class linkage object, the runtime can retrieve the variable or type that corresponds to the name that is provided in each shader (if that name is valid for a given shader) and that is created with the given class linkage object.</span></span>

<span data-ttu-id="61204-107">Si supponga, ad esempio, di disporre di una classe **Light** che implementi un'interfaccia **colore** e di usare questa classe nel vertex shader e pixel shader.</span><span class="sxs-lookup"><span data-stu-id="61204-107">For example, suppose you have a **Light** class that implements a **Color** interface, and you use this class in your vertex shader and pixel shader.</span></span> <span data-ttu-id="61204-108">Quando si crea uno shader, ad esempio chiamando [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader), il runtime determina che il tipo di classe **Light** è disponibile sia in vertex che in pixel shader e aggiunge il tipo di classe **Light** all'oggetto del collegamento alla classe.</span><span class="sxs-lookup"><span data-stu-id="61204-108">When you create a shader (for example, by calling [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), the runtime determines that the **Light** class type is available in both vertex and pixel shaders and adds the **Light** class type to the class linkage object.</span></span> <span data-ttu-id="61204-109">È quindi possibile creare un'istanza di **Light** in una posizione desiderata, associare le risorse per entrambi gli shader e passare questa istanza nella matrice di istanze della classe quando si imposta lo shader sul dispositivo (ad esempio, chiamando [**sul ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span><span class="sxs-lookup"><span data-stu-id="61204-109">You can then create a **Light** instance at a location that you want, bind the resources for both shaders, and pass this instance in the class instances array when you set the shader to the device (for example, by calling [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)).</span></span> <span data-ttu-id="61204-110">Il runtime esegue quindi la sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="61204-110">The runtime then performs the following sequence:</span></span>

1.  <span data-ttu-id="61204-111">Verifica che l'istanza di sia stata creata con lo stesso oggetto di collegamento di classe.</span><span class="sxs-lookup"><span data-stu-id="61204-111">Verifies that the instance was created with the same class linkage object.</span></span>
2.  <span data-ttu-id="61204-112">Verifica che il tipo di classe **Light** sia disponibili sia in vertex che in pixel shader.</span><span class="sxs-lookup"><span data-stu-id="61204-112">Verifies that the **Light** class type is availabe in both vertex and pixel shaders.</span></span>
3.  <span data-ttu-id="61204-113">Seleziona le tabelle di funzioni corrette, che possono essere diverse per gli shader Vertex e pixel.</span><span class="sxs-lookup"><span data-stu-id="61204-113">Selects the correct function tables, which can be different for the vertex and pixel shaders.</span></span>
4.  <span data-ttu-id="61204-114">Invia gli offset forniti dall'istanza di.</span><span class="sxs-lookup"><span data-stu-id="61204-114">Sends down the offsets that the instance provides.</span></span>

<span data-ttu-id="61204-115">L'oggetto collegamento alla classe è in definitiva un repository di nomi di tipo e di variabile.</span><span class="sxs-lookup"><span data-stu-id="61204-115">The class linkage object is ultimately a repository of type and variable names.</span></span> <span data-ttu-id="61204-116">Il numero massimo di nomi disponibili per ogni elemento (tipo e variabile) è 64K.</span><span class="sxs-lookup"><span data-stu-id="61204-116">The maximum number of names available for each item (type and variable) is 64K.</span></span> <span data-ttu-id="61204-117">Più è lungo il tipo e i nomi delle variabili, più elevato è il requisito di archiviazione per i metadati dell'interfaccia archiviati per shader.</span><span class="sxs-lookup"><span data-stu-id="61204-117">The longer the type and variable names are, the higher the storage requirement is for the interface metadata that is stored per shader.</span></span> <span data-ttu-id="61204-118">Questo perché il runtime deve archiviare un mapping per questi nomi per ogni shader.</span><span class="sxs-lookup"><span data-stu-id="61204-118">This is because the runtime must store a mapping for these names for each shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61204-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61204-119">Related Topics</span></span>

[<span data-ttu-id="61204-120">Collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="61204-120">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a><span data-ttu-id="61204-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61204-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61204-122">Collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="61204-122">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 