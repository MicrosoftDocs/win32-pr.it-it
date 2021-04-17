---
title: Valori restituiti dalla funzione
description: I valori restituiti dalla funzione sono simili ai parametri \ out solo perché i dati non sono forniti dall'applicazione client.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300329"
---
# <a name="function-return-values"></a><span data-ttu-id="8e124-103">Valori restituiti dalla funzione</span><span class="sxs-lookup"><span data-stu-id="8e124-103">Function Return Values</span></span>

<span data-ttu-id="8e124-104">I valori restituiti dalla funzione sono simili ai parametri **\[ out \]**-only perché i dati non sono forniti dall'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="8e124-104">Function return values are similar to **\[out\]**-only parameters because their data is not provided by the client application.</span></span> <span data-ttu-id="8e124-105">Tuttavia, vengono gestiti in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="8e124-105">However they are managed differently.</span></span> <span data-ttu-id="8e124-106">A differenza dei parametri di sola **\[ uscita \]**, non è necessario che siano puntatori.</span><span class="sxs-lookup"><span data-stu-id="8e124-106">Unlike **\[out\]**-only parameters, they are not required to be pointers.</span></span> <span data-ttu-id="8e124-107">La procedura remota può restituire qualsiasi tipo di dati valido ad eccezione dei puntatori di riferimento e delle unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="8e124-107">The remote procedure can return any valid data type except reference pointers and nonencapsulated unions.</span></span>

<span data-ttu-id="8e124-108">È tuttavia consigliabile utilizzare un parametro **\[ out \]** anziché un valore restituito per tipi di dati complessi.</span><span class="sxs-lookup"><span data-stu-id="8e124-108">However, using an **\[out\]** parameter instead of a return value for complex data types is recommended.</span></span> <span data-ttu-id="8e124-109">Quando si restituiscono tipi di dati complessi, il compilatore MIDL genera uno stub in modalità/OS.</span><span class="sxs-lookup"><span data-stu-id="8e124-109">While returning complex data types, the MIDL compiler will generate an /Os mode stub.</span></span> <span data-ttu-id="8e124-110">Di conseguenza, tutte le informazioni di controllo degli errori recenti fornite da/Robust vengono perse.</span><span class="sxs-lookup"><span data-stu-id="8e124-110">As a result, all recent error-checking information provided by /robust is lost.</span></span>

<span data-ttu-id="8e124-111">I valori restituiti dalla funzione che sono tipi di puntatore vengono allocati dallo stub client con una chiamata a [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="8e124-111">Function return values that are pointer types are allocated by the client stub with a call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="8e124-112">Di conseguenza, è possibile applicare solo l'attributo puntatore univoco o completo a un tipo restituito dalla funzione puntatore.</span><span class="sxs-lookup"><span data-stu-id="8e124-112">Accordingly, only the unique or full pointer attribute can be applied to a pointer function-return type.</span></span>

 

 