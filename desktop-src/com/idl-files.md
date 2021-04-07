---
title: File IDL
description: File IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873009"
---
# <a name="idl-files"></a><span data-ttu-id="734d2-103">File IDL</span><span class="sxs-lookup"><span data-stu-id="734d2-103">IDL Files</span></span>

<span data-ttu-id="734d2-104">COM usa il Microsoft Interface Definition Language (MIDL) per descrivere gli oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="734d2-104">COM uses the Microsoft Interface Definition Language (MIDL) to describe COM objects.</span></span> <span data-ttu-id="734d2-105">MIDL è un'estensione dell'IDL per gli ambienti di calcolo distribuiti definiti da Open Software Foundation, sviluppato per definire interfacce per le chiamate di procedure remote in applicazioni client/server tradizionali.</span><span class="sxs-lookup"><span data-stu-id="734d2-105">MIDL is an extension of the IDL for distributed computing environments defined by the Open Software Foundation, which was developed to define interfaces for remote procedure calls in traditional client/server applications.</span></span> <span data-ttu-id="734d2-106">MIDL include la maggior parte degli attributi e delle istruzioni del linguaggio di definizione dell'oggetto (FAD), il linguaggio originariamente usato per generare librerie dei tipi per l'automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="734d2-106">MIDL includes most of the attributes and statements of Object Definition Language (ODL), the language originally used to generate type libraries for OLE Automation.</span></span>

<span data-ttu-id="734d2-107">In C++ e Java uno sviluppatore che compila un oggetto COM crea un file IDL che viene elaborato dal compilatore MIDL per creare una libreria dei tipi, un file di intestazione e proxy o entrambi.</span><span class="sxs-lookup"><span data-stu-id="734d2-107">In C++ and Java, a developer building a COM object creates an IDL file that the MIDL compiler then processes to create a type library or header and proxy files, or both.</span></span> <span data-ttu-id="734d2-108">Una *libreria dei tipi* è un file binario che descrive l'oggetto com o le interfacce com oppure entrambe.</span><span class="sxs-lookup"><span data-stu-id="734d2-108">A *type library* is a binary file that describes the COM object or COM interfaces, or both.</span></span> <span data-ttu-id="734d2-109">Una libreria dei tipi è la versione compilata del file IDL.</span><span class="sxs-lookup"><span data-stu-id="734d2-109">A type library is the compiled version of the IDL file.</span></span> <span data-ttu-id="734d2-110">Tuttavia, le librerie di tipi supportano solo la semantica di FAD.</span><span class="sxs-lookup"><span data-stu-id="734d2-110">However, type libraries support ODL semantics only.</span></span> <span data-ttu-id="734d2-111">In particolare, non possono rappresentare tutte le informazioni provenienti da un file IDL correlato agli attributi IDL, ad esempio le \[ [**dimensioni \_**](/windows/desktop/Midl/size-is) \] .</span><span class="sxs-lookup"><span data-stu-id="734d2-111">In particular, they cannot represent all the information from an IDL file related to IDL attributes like \[[**size\_is**](/windows/desktop/Midl/size-is)\].</span></span> <span data-ttu-id="734d2-112">È necessario creare e utilizzare i file proxy per i file IDL interessati dalla perdita di informazioni nella libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="734d2-112">You need to create and use proxy files for IDL files affected by information loss in the type library.</span></span>

<span data-ttu-id="734d2-113">In Visual Basic, uno sviluppatore che crea un oggetto COM non crea un file IDL.</span><span class="sxs-lookup"><span data-stu-id="734d2-113">In Visual Basic, a developer creating a COM object does not create an IDL file.</span></span> <span data-ttu-id="734d2-114">Al contrario, Visual Basic raccoglie le informazioni usando le proprietà di classe e progetto e crea direttamente la libreria dei tipi.</span><span class="sxs-lookup"><span data-stu-id="734d2-114">Instead, Visual Basic gathers information using class and project properties and directly creates the type library.</span></span>

 

 