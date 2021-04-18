---
description: "È possibile fare riferimento a cluster da due diverse prospettive: all'interno del file e nel volume."
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Cluster ed extent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312940"
---
# <a name="clusters-and-extents"></a><span data-ttu-id="eb45b-103">Cluster ed extent</span><span class="sxs-lookup"><span data-stu-id="eb45b-103">Clusters and Extents</span></span>

<span data-ttu-id="eb45b-104">È possibile fare riferimento a cluster da due diverse prospettive: all'interno del file e nel volume.</span><span class="sxs-lookup"><span data-stu-id="eb45b-104">Clusters may be referred to from two different perspectives: within the file and on the volume.</span></span> <span data-ttu-id="eb45b-105">Qualsiasi cluster in un file ha un *numero di cluster virtuale* (VCN), ovvero il relativo offset rispetto all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="eb45b-105">Any cluster in a file has a *virtual cluster number* (VCN), which is its relative offset from the beginning of the file.</span></span> <span data-ttu-id="eb45b-106">Ad esempio, una ricerca a due volte la dimensione di un cluster, seguita da un'operazione di lettura, restituirà i dati a partire dalla terza VCN.</span><span class="sxs-lookup"><span data-stu-id="eb45b-106">For example, a seek to twice the size of a cluster, followed by a read, will return data beginning at the third VCN.</span></span> <span data-ttu-id="eb45b-107">Un *numero di cluster logico* (LCN) descrive l'offset di un cluster da un punto arbitrario all'interno del volume.</span><span class="sxs-lookup"><span data-stu-id="eb45b-107">A *logical cluster number* (LCN) describes the offset of a cluster from some arbitrary point within the volume.</span></span> <span data-ttu-id="eb45b-108">LCNs deve essere trattato solo come numeri ordinali o relativi.</span><span class="sxs-lookup"><span data-stu-id="eb45b-108">LCNs should be treated only as ordinal, or relative, numbers.</span></span> <span data-ttu-id="eb45b-109">Non esiste un mapping garantito dei cluster logici ai settori di unità disco rigido fisico.</span><span class="sxs-lookup"><span data-stu-id="eb45b-109">There is no guaranteed mapping of logical clusters to physical hard disk drive sectors.</span></span>

<span data-ttu-id="eb45b-110">Un *extent* è un'esecuzione di cluster contigui.</span><span class="sxs-lookup"><span data-stu-id="eb45b-110">An *extent* is a run of contiguous clusters.</span></span> <span data-ttu-id="eb45b-111">Si supponga, ad esempio, che un file costituito da 30 cluster venga registrato in due extent.</span><span class="sxs-lookup"><span data-stu-id="eb45b-111">For example, suppose a file consisting of 30 clusters is recorded in two extents.</span></span> <span data-ttu-id="eb45b-112">Il primo extent può essere costituito da cinque cluster contigui, l'altro dei 25 cluster rimanenti.</span><span class="sxs-lookup"><span data-stu-id="eb45b-112">The first extent might consist of five contiguous clusters, the other of the remaining 25 clusters.</span></span>

<span data-ttu-id="eb45b-113">Non esiste alcuna garanzia di alcuna relazione sul disco di qualsiasi extent con qualsiasi altro extent.</span><span class="sxs-lookup"><span data-stu-id="eb45b-113">There is no guarantee of any relationship on the disk of any extent to any other extent.</span></span> <span data-ttu-id="eb45b-114">Il primo extent, ad esempio, può essere a una LCN superiore rispetto a un extent successivo.</span><span class="sxs-lookup"><span data-stu-id="eb45b-114">For example, the first extent may be at a higher LCN than a subsequent extent.</span></span>

 

 



