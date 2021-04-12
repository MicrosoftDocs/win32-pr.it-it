---
title: Conversione in Java da Visual Basic
description: Conversione in Java da Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d02071641901c5217069d997c22fa04c94cef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395407"
---
# <a name="translating-to-java-from-visual-basic"></a><span data-ttu-id="ada1c-103">Conversione in Java da Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ada1c-103">Translating to Java from Visual Basic</span></span>

<span data-ttu-id="ada1c-104">Per impostazione predefinita, Visual Basic passa i parametri per riferimento.</span><span class="sxs-lookup"><span data-stu-id="ada1c-104">By default, Visual Basic passes parameters by reference.</span></span> <span data-ttu-id="ada1c-105">I parametri che devono essere passati solo per valore sono specificati dalla parola chiave **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="ada1c-105">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span>

<span data-ttu-id="ada1c-106">Java non supporta le matrici multidimensionali.</span><span class="sxs-lookup"><span data-stu-id="ada1c-106">Java does not support multidimensional arrays.</span></span> <span data-ttu-id="ada1c-107">I metodi che accettano o restituiscono matrici multidimensionali non sono disponibili in Java.</span><span class="sxs-lookup"><span data-stu-id="ada1c-107">Methods that accept or return multidimensional arrays are not available from Java.</span></span>

<span data-ttu-id="ada1c-108">Java e Visual Basic differiscono leggermente per la rappresentazione delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ada1c-108">Java and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="ada1c-109">In Java le proprietà sono rappresentate come un set di funzioni di accesso, una che imposta il valore della proprietà e una che recupera il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ada1c-109">In Java, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="ada1c-110">In Visual Basic le proprietà sono rappresentate come un singolo elemento che può essere utilizzato per recuperare o impostare il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ada1c-110">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ada1c-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ada1c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ada1c-112">Conversione in Java</span><span class="sxs-lookup"><span data-stu-id="ada1c-112">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




