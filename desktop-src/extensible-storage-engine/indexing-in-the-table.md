---
description: 'Altre informazioni su: indicizzazione nella tabella'
title: Indicizzazione nella tabella
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5d09fde8c5fcdcf2411f6d40c5a3a70912bed27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049611"
---
# <a name="indexing-in-the-table"></a><span data-ttu-id="e0856-103">Indicizzazione nella tabella</span><span class="sxs-lookup"><span data-stu-id="e0856-103">Indexing in the Table</span></span>


<span data-ttu-id="e0856-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e0856-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="indexing-in-the-table"></a><span data-ttu-id="e0856-105">Indicizzazione nella tabella</span><span class="sxs-lookup"><span data-stu-id="e0856-105">Indexing in the Table</span></span>

<span data-ttu-id="e0856-106">Un indice è un set di colonne chiave che definiscono un ordinamento permanente dei record in una tabella.</span><span class="sxs-lookup"><span data-stu-id="e0856-106">An index is a set of key columns that define a persistent ordering of records in a table.</span></span> <span data-ttu-id="e0856-107">I record sono voci di indice nell'indice primario.</span><span class="sxs-lookup"><span data-stu-id="e0856-107">Records are index entries in the primary index.</span></span> <span data-ttu-id="e0856-108">È possibile definire un indice primario e più indici secondari per creare ordini diversi di dati nella tabella.</span><span class="sxs-lookup"><span data-stu-id="e0856-108">One primary index and multiple secondary indexes can be defined to create different orders of data in the table.</span></span>

<span data-ttu-id="e0856-109">Sebbene sia possibile definire più indici, i record vengono archiviati fisicamente in alberi B + nell'ordine specificato dall'indice primario.</span><span class="sxs-lookup"><span data-stu-id="e0856-109">Although multiple indices can be defined, the records are physically stored in B+ trees in the order specified by the primary index.</span></span> <span data-ttu-id="e0856-110">L'indice primario è sempre un indice cluster e deve anche essere univoco.</span><span class="sxs-lookup"><span data-stu-id="e0856-110">The primary index is always a clustered index, and must also be unique.</span></span> <span data-ttu-id="e0856-111">L'indice primario deve essere dichiarato prima dell'aggiornamento della prima tabella per mantenere l'ordine degli indici.</span><span class="sxs-lookup"><span data-stu-id="e0856-111">The primary index must be declared before the first table update to preserve the index ordering.</span></span> <span data-ttu-id="e0856-112">Quando l'applicazione non definisce alcun indice primario, i dati vengono archiviati nell'ordine in cui i record vengono aggiunti alla tabella.</span><span class="sxs-lookup"><span data-stu-id="e0856-112">When no primary index is defined by the application, the data is stored in the order in which records are added to the table.</span></span> <span data-ttu-id="e0856-113">Questo indice speciale viene definito indice sequenziale.</span><span class="sxs-lookup"><span data-stu-id="e0856-113">This special index is referred to as a sequential index.</span></span>

<span data-ttu-id="e0856-114">Gli alberi B + separati vengono usati per ordinare i record in base all'indice secondario.</span><span class="sxs-lookup"><span data-stu-id="e0856-114">Separate B+ trees are used to order records according to the secondary index.</span></span> <span data-ttu-id="e0856-115">Le voci di indice nell'indice secondario contengono puntatori ai dati archiviati in base all'indice primario.</span><span class="sxs-lookup"><span data-stu-id="e0856-115">Index entries in the secondary index contain pointers to the data stored according to the primary index.</span></span> <span data-ttu-id="e0856-116">Le voci di indice per i record nell'indice primario devono essere univoche perché l'indice secondario punta al record utilizzando la chiave primaria del record.</span><span class="sxs-lookup"><span data-stu-id="e0856-116">The index entries for records in the primary index must be unique because the secondary index points to the record using the primary key of the record.</span></span> <span data-ttu-id="e0856-117">Gli indici secondari possono avere o meno un vincolo di univocità.</span><span class="sxs-lookup"><span data-stu-id="e0856-117">Secondary indices may or may not have a uniqueness constraint.</span></span> <span data-ttu-id="e0856-118">Per ulteriori informazioni, vedere l'argomento relativo alla [Panoramica del database](./database-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="e0856-118">For more information, see the [Database Overview](./database-overview.md) topic.</span></span>
