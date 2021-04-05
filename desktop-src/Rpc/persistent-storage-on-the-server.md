---
title: Archiviazione permanente sul server
description: È possibile ottimizzare l'applicazione in modo che lo stub del server non liberi la memoria sul server al termine di una chiamata di procedura remota.
ms.assetid: 340334e2-94ac-4be2-a16d-38bc4c64e7db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7237fe6136918e5495ee1f22bac0991d71c5dbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955651"
---
# <a name="persistent-storage-on-the-server"></a><span data-ttu-id="a0691-103">Archiviazione permanente sul server</span><span class="sxs-lookup"><span data-stu-id="a0691-103">Persistent Storage on the Server</span></span>

<span data-ttu-id="a0691-104">È possibile ottimizzare l'applicazione in modo che lo stub del server non liberi la memoria sul server al termine di una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="a0691-104">You can optimize your application so the server stub does not free memory on the server at the conclusion of a remote procedure call.</span></span> <span data-ttu-id="a0691-105">Ad esempio, quando un handle di contesto verrà modificato da diverse procedure remote, è possibile usare l'attributo ACF **\[ allocate (non \_ gratuito) \]** per mantenere la memoria allocata sul server.</span><span class="sxs-lookup"><span data-stu-id="a0691-105">For example, when a context handle will be manipulated by several remote procedures, you can use the ACF attribute **\[allocate(dont\_free)\]** to retain the allocated memory on the server.</span></span>

<span data-ttu-id="a0691-106">L'attributo **\[ allocate (Not \_ free) \]** viene aggiunto alla Dichiarazione **typedef** di ACF in ACF.</span><span class="sxs-lookup"><span data-stu-id="a0691-106">The **\[allocate(dont\_free)\]** attribute is added to the ACF **typedef** declaration in the ACF.</span></span> <span data-ttu-id="a0691-107">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="a0691-107">For example:</span></span>

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes, dont_free)] P_TREE_TYPE;
```

<span data-ttu-id="a0691-108">Quando si specifica l'attributo **\[ allocate (non \_ gratuito) \]** , la struttura dei dati dell'albero viene allocata, ma non liberata, dallo stub del server.</span><span class="sxs-lookup"><span data-stu-id="a0691-108">When the **\[allocate(dont\_free)\]** attribute is specified, the tree data structure is allocated, but not freed, by the server stub.</span></span> <span data-ttu-id="a0691-109">Quando si rendono i puntatori a tali aree dati persistenti disponibili ad altre routine, ad esempio copiando i puntatori in variabili globali, i dati conservati sono accessibili ad altre funzioni server.</span><span class="sxs-lookup"><span data-stu-id="a0691-109">When you make the pointers to such persistent data areas available to other routines—for example, by copying the pointers to global variables—the retained data is accessible to other server functions.</span></span> <span data-ttu-id="a0691-110">L'attributo **\[ allocate (non \_ gratuito) \]** è particolarmente utile per la gestione di strutture di puntatore permanenti come parte delle informazioni sullo stato del server associate a un tipo di handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="a0691-110">The **\[allocate(dont\_free)\]** attribute is particularly useful for maintaining persistent pointer structures as part of the server state information associated with a context-handle type.</span></span>

 

 




