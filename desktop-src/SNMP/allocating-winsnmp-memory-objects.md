---
title: Allocazione di oggetti memoria WinSNMP
description: I descrittori, gli handle di risorsa e le stringhe di tipo C sono i tre tipi di oggetti di memoria nell'ambiente di programmazione WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044040"
---
# <a name="allocating-winsnmp-memory-objects"></a><span data-ttu-id="ab78f-103">Allocazione di oggetti memoria WinSNMP</span><span class="sxs-lookup"><span data-stu-id="ab78f-103">Allocating WinSNMP Memory Objects</span></span>

<span data-ttu-id="ab78f-104">I descrittori, gli handle di risorsa e le stringhe di tipo C sono i tre tipi di oggetti di memoria nell'ambiente di programmazione WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="ab78f-104">Descriptors, resource handles and C-style strings are the three types of memory objects in the WinSNMP programming environment.</span></span>

<span data-ttu-id="ab78f-105">Il tipo di oggetto determina se l'implementazione di Microsoft WinSNMP o l'applicazione WinSNMP alloca e dealloca la memoria per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ab78f-105">The type of object determines whether the Microsoft WinSNMP implementation or the WinSNMP application allocates and deallocates the memory for the object.</span></span> <span data-ttu-id="ab78f-106">In questo modo si riduce l'allocazione non necessaria dello spazio del buffer temporaneo e la copia superflua dei buffer.</span><span class="sxs-lookup"><span data-stu-id="ab78f-106">This reduces unnecessary allocation of temporary buffer space and unnecessary copying of buffers.</span></span>

<span data-ttu-id="ab78f-107">La tabella seguente riepiloga l'allocazione e la deallocazione delle risorse per gli oggetti memoria WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="ab78f-107">The following table summarizes the allocation and deallocation of resources for WinSNMP memory objects.</span></span>



| <span data-ttu-id="ab78f-108">Tipo di oggetto</span><span class="sxs-lookup"><span data-stu-id="ab78f-108">Object type</span></span>                                                                   | <span data-ttu-id="ab78f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab78f-109">Description</span></span>                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab78f-110">descrittore [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)</span><span class="sxs-lookup"><span data-stu-id="ab78f-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor</span></span> | <span data-ttu-id="ab78f-111">Se l'applicazione WinSNMP alloca la memoria, deve deallocare la memoria con una chiamata a una funzione appropriata.</span><span class="sxs-lookup"><span data-stu-id="ab78f-111">If the WinSNMP application allocates the memory, it must deallocate the memory with a call to an appropriate function.</span></span> <span data-ttu-id="ab78f-112">Se l'implementazione alloca la memoria, l'applicazione deve chiamare la funzione [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) per deallocare la memoria.</span><span class="sxs-lookup"><span data-stu-id="ab78f-112">If the implementation allocates the memory, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to deallocate the memory.</span></span> |
| <span data-ttu-id="ab78f-113">struttura [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)</span><span class="sxs-lookup"><span data-stu-id="ab78f-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure</span></span>                                    | <span data-ttu-id="ab78f-114">Se il membro del **valore** è un descrittore [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) o [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , l'applicazione deve continuare come indicato in precedenza per i descrittori.</span><span class="sxs-lookup"><span data-stu-id="ab78f-114">If the **value** member is an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor, the application must proceed as indicated above for descriptors.</span></span>                                                                                                     |
| <span data-ttu-id="ab78f-115">Handle di risorsa</span><span class="sxs-lookup"><span data-stu-id="ab78f-115">Resource handle</span></span>                                                               | <span data-ttu-id="ab78f-116">L'implementazione alloca, gestisce e libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="ab78f-116">The implementation allocates, manages, and frees the memory.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="ab78f-117">Stringa di tipo C</span><span class="sxs-lookup"><span data-stu-id="ab78f-117">C-style string</span></span>                                                                | <span data-ttu-id="ab78f-118">L'applicazione WinSNMP deve gestire e liberare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="ab78f-118">The WinSNMP application must manage and free the memory it allocates.</span></span>                                                                                                                                                                                                                |



 

<span data-ttu-id="ab78f-119">Per ulteriori informazioni, vedere la pagina relativa alla [liberazione dei descrittori WinSNMP](freeing-winsnmp-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="ab78f-119">For more information, see [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).</span></span>

 

 




