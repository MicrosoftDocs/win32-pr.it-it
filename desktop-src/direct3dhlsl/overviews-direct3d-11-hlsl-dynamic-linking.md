---
title: Collegamento dinamico
description: Gli sviluppatori di grafica talvolta creano shader di grandi dimensioni e per utilizzo generico che possono essere usati da un'ampia gamma di elementi della scena.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710861"
---
# <a name="dynamic-linking"></a><span data-ttu-id="b0f49-103">Collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="b0f49-103">Dynamic Linking</span></span>

<span data-ttu-id="b0f49-104">Gli sviluppatori di grafica talvolta creano shader di grandi dimensioni e per utilizzo generico che possono essere usati da un'ampia gamma di elementi della scena.</span><span class="sxs-lookup"><span data-stu-id="b0f49-104">Graphics developers sometimes create large, general-purpose shaders that can be used by a wide variety of scene items.</span></span> <span data-ttu-id="b0f49-105">In fase di esecuzione, lo shader esegue in modo condizionale il codice appropriato per la situazione specificata.</span><span class="sxs-lookup"><span data-stu-id="b0f49-105">At runtime, the shader conditionally runs code appropriate for the given situation.</span></span> <span data-ttu-id="b0f49-106">Sfortunatamente, questi shader di uso generale di grandi dimensioni usano i registri di utilizzo generico (GPRs) in modo non efficiente e possono essere molto più lenti rispetto agli shader più piccoli e più mirati.</span><span class="sxs-lookup"><span data-stu-id="b0f49-106">Unfortunately, these large, general-purpose shaders use general-purpose registers (GPRs) inefficiently, and can be much slower than smaller, more targeted shaders.</span></span>

<span data-ttu-id="b0f49-107">Il modello di shader 5 risolve questo problema di prestazioni introducendo il collegamento dinamico dello shader.</span><span class="sxs-lookup"><span data-stu-id="b0f49-107">Shader model 5 addresses this performance problem by introducing dynamic shader linking.</span></span> <span data-ttu-id="b0f49-108">Il collegamento dinamico separa i frammenti di codice dello shader usando le interfacce e le funzioni virtuali e consente all'applicazione di selezionare il frammento da usare in fase di estrazione.</span><span class="sxs-lookup"><span data-stu-id="b0f49-108">Dynamic linking separates shader code fragments by using interfaces and virtual functions and allows the application to select the fragment to use at draw time.</span></span> <span data-ttu-id="b0f49-109">Ciò consente di migliorare le prestazioni associando solo il codice dello shader necessario e non l'intero shader di utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="b0f49-109">This improves performance by binding only the shader code needed and not the entire large, general-purpose shader.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b0f49-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b0f49-110">In This Section</span></span>



| <span data-ttu-id="b0f49-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="b0f49-111">Item</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="b0f49-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0f49-112">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f49-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Archiviazione di variabili e tipi per gli shader da condividere](storing-variables-and-types-for-shaders-to-share.md)</span><span class="sxs-lookup"><span data-stu-id="b0f49-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Storing Variables and Types for Shaders to Share](storing-variables-and-types-for-shaders-to-share.md)</span></span><br/> | <span data-ttu-id="b0f49-114">Descrive l'oggetto collegamento di classe per l'archiviazione di variabili e tipi che possono essere condivisi da più shader.</span><span class="sxs-lookup"><span data-stu-id="b0f49-114">Describes the class linkage object for storing variables and types that multiple shaders can share.</span></span><br/> |
| <span data-ttu-id="b0f49-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfacce e classi](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span><span class="sxs-lookup"><span data-stu-id="b0f49-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces and Classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span></span><br/>                                                                                                         | <span data-ttu-id="b0f49-116">Viene descritto l'utilizzo di interfacce e classi HLSL per implementare il collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="b0f49-116">Describes using HLSL interfaces and classes to implement dynamic linking.</span></span><br/>                           |
| <span data-ttu-id="b0f49-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Limitazioni di utilizzo dell'interfaccia](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span><span class="sxs-lookup"><span data-stu-id="b0f49-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Interface Usage Restrictions](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span></span><br/>                                                                            | <span data-ttu-id="b0f49-118">Descrive le restrizioni relative all'uso delle interfacce nel codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="b0f49-118">Describes restrictions on the use of interfaces in shader code.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="b0f49-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0f49-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f49-120">HLSL</span><span class="sxs-lookup"><span data-stu-id="b0f49-120">HLSL</span></span>](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





