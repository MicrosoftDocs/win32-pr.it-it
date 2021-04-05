---
title: Matrici fisse
description: Se l'interfaccia specifica una matrice con un numero specifico di elementi come parametro, viene utilizzata una matrice fissa. Quando si usa MIDL, si definiscono matrici fisse nello stesso modo in cui vengono definite in C. Specificare il tipo, il nome e la dimensione della matrice.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711431"
---
# <a name="fixed-arrays"></a><span data-ttu-id="4f749-104">Matrici fisse</span><span class="sxs-lookup"><span data-stu-id="4f749-104">Fixed Arrays</span></span>

<span data-ttu-id="4f749-105">Se l'interfaccia specifica una matrice con un numero specifico di elementi come parametro, viene utilizzata una matrice fissa.</span><span class="sxs-lookup"><span data-stu-id="4f749-105">If your interface specifies an array with a specific number of elements as a parameter, it is using a fixed array.</span></span> <span data-ttu-id="4f749-106">Quando si usa MIDL, si definiscono matrici fisse nello stesso modo in cui vengono definite in C. Specificare il tipo, il nome e la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="4f749-106">When using MIDL, you define fixed arrays in the same way you define them in C. You specify the array's type, name, and size.</span></span>

<span data-ttu-id="4f749-107">Nell'esempio seguente viene illustrato come definire una matrice fissa.</span><span class="sxs-lookup"><span data-stu-id="4f749-107">The following example demonstrates how to define a fixed array.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="4f749-108">Quando un programma client passa un array fisso a un programma server, lo stub del client invia l'intera matrice allo stub del server.</span><span class="sxs-lookup"><span data-stu-id="4f749-108">When a client program passes a fixed array to a server program, the client stub sends the entire array to the server stub.</span></span> <span data-ttu-id="4f749-109">Lo stub del server alloca memoria per la matrice e archivia i dati della matrice ricevuti attraverso la rete nella memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="4f749-109">The server stub allocates memory for the array and stores the array data it receives across the network into the allocated memory.</span></span> <span data-ttu-id="4f749-110">Passa quindi la matrice alla procedura remota sul server.</span><span class="sxs-lookup"><span data-stu-id="4f749-110">It then passes the array to the remote procedure on the server.</span></span> <span data-ttu-id="4f749-111">Il server può modificare i dati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="4f749-111">The server may modify the data in the array.</span></span>

<span data-ttu-id="4f749-112">Al termine della procedura remota, lo stub del server invia nuovamente il contenuto della matrice al client.</span><span class="sxs-lookup"><span data-stu-id="4f749-112">When the remote procedure terminates, the server stub sends the contents of the array back to the client.</span></span> <span data-ttu-id="4f749-113">Lo stub client copia i dati ricevuti dallo stub del server nella matrice originale.</span><span class="sxs-lookup"><span data-stu-id="4f749-113">The client stub copies the data it received from the server stub into the original array.</span></span> <span data-ttu-id="4f749-114">Il programma client può quindi utilizzare i dati come se ricevesse i dati da una chiamata di procedura locale.</span><span class="sxs-lookup"><span data-stu-id="4f749-114">The client program can then use the data as it would if it received the data from a local procedure call.</span></span>

 

 




