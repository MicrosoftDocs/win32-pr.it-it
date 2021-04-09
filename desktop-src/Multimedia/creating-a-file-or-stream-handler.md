---
title: Creazione di un gestore di file o di flussi
description: Creazione di un gestore di file o di flussi
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044579"
---
# <a name="creating-a-file-or-stream-handler"></a><span data-ttu-id="40e27-103">Creazione di un gestore di file o di flussi</span><span class="sxs-lookup"><span data-stu-id="40e27-103">Creating a File or Stream Handler</span></span>

<span data-ttu-id="40e27-104">In un'applicazione scritta nel linguaggio di programmazione C, un gestore di file o flussi crea in genere una funzione per ogni metodo.</span><span class="sxs-lookup"><span data-stu-id="40e27-104">In an application written in the C programming language, a file or stream handler usually creates a function for each method.</span></span> <span data-ttu-id="40e27-105">L'applicazione accede a queste funzioni tramite una matrice di puntatori a funzione creati dal gestore del flusso.</span><span class="sxs-lookup"><span data-stu-id="40e27-105">Your application accesses these functions through an array of function pointers the stream handler creates.</span></span> <span data-ttu-id="40e27-106">Una struttura **IAVIStreamVtbl** contiene la matrice di puntatori a funzione.</span><span class="sxs-lookup"><span data-stu-id="40e27-106">An **IAVIStreamVtbl** structure contains the array of function pointers.</span></span> <span data-ttu-id="40e27-107">Un gestore di flusso può assegnare qualsiasi nome che desideri alle funzioni create per i metodi.</span><span class="sxs-lookup"><span data-stu-id="40e27-107">A stream handler can assign any name it wants to functions it creates for the methods.</span></span> <span data-ttu-id="40e27-108">La posizione del puntatore a funzione nella struttura implica la corrispondenza della funzione con il metodo.</span><span class="sxs-lookup"><span data-stu-id="40e27-108">The position of the function pointer in the structure implies the correspondence of the function to the method.</span></span> <span data-ttu-id="40e27-109">Il primo puntatore a funzione nella struttura, ad esempio, corrisponde al metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="40e27-109">For example, the first function pointer in the structure corresponds to the **QueryInterface** method.</span></span> <span data-ttu-id="40e27-110">Il gestore del flusso deve fornire tutte le funzioni di un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="40e27-110">Your stream handler must provide all the functions of an interface.</span></span>

 

 




