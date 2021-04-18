---
description: Descrive un disco rigido, il partizionamento e il record di avvio principale.
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: Dispositivi e partizioni disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063b943d33118a45cb6ab4c304569094af2c32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568377"
---
# <a name="disk-devices-and-partitions"></a><span data-ttu-id="5bce6-103">Dispositivi e partizioni disco</span><span class="sxs-lookup"><span data-stu-id="5bce6-103">Disk Devices and Partitions</span></span>

<span data-ttu-id="5bce6-104">Un disco rigido è costituito da un set di dischi in pila, ciascuno dei quali contiene dati archiviati in modo elettromagnetico nei cerchi concentrici o in *tracce*.</span><span class="sxs-lookup"><span data-stu-id="5bce6-104">A hard disk consists of a set of stacked platters, each of which has data stored electromagnetically in concentric circles, or *tracks*.</span></span> <span data-ttu-id="5bce6-105">Ogni piatto ha due teste, una su ogni lato del piatto, che legge o scrive dati come spine del disco.</span><span class="sxs-lookup"><span data-stu-id="5bce6-105">Each platter has two heads, one on each side of the platter, that reads or writes data as the disk spins.</span></span> <span data-ttu-id="5bce6-106">Un' *unità disco rigido* controlla il posizionamento, la lettura e la scrittura del disco rigido.</span><span class="sxs-lookup"><span data-stu-id="5bce6-106">A *hard disk drive* controls the positioning, reading, and writing of the hard disk.</span></span> <span data-ttu-id="5bce6-107">Si noti che le intestazioni di tutti i dischi sono posizionate come unità.</span><span class="sxs-lookup"><span data-stu-id="5bce6-107">Note that the heads of all platters are positioned as a unit.</span></span>

<span data-ttu-id="5bce6-108">La più piccola unità indirizzabile di una traccia è un *settore*.</span><span class="sxs-lookup"><span data-stu-id="5bce6-108">The smallest addressable unit of a track is a *sector*.</span></span> <span data-ttu-id="5bce6-109">Un *cilindro* viene definito come il set di tracce visualizzate nella stessa posizione in ogni piatto.</span><span class="sxs-lookup"><span data-stu-id="5bce6-109">A *cylinder* is defined as the set of tracks that appear in the same location on each platter.</span></span> <span data-ttu-id="5bce6-110">Il diagramma seguente, ad esempio, Mostra un disco rigido con quattro dischi.</span><span class="sxs-lookup"><span data-stu-id="5bce6-110">For example, the following diagram shows a hard disk with four platters.</span></span> <span data-ttu-id="5bce6-111">Il cilindro X è costituito da otto tracce (Track X da ogni lato di ogni piatto).</span><span class="sxs-lookup"><span data-stu-id="5bce6-111">Cylinder X consists of eight tracks (track X from each side of each platter).</span></span>

![disco rigido, inclusi tracce, settori e dischi](images/diskdevice.png)

<span data-ttu-id="5bce6-113">Un disco rigido può contenere una o più aree logiche denominate *partizioni*.</span><span class="sxs-lookup"><span data-stu-id="5bce6-113">A hard disk can contain one or more logical regions called *partitions*.</span></span> <span data-ttu-id="5bce6-114">Le partizioni vengono create quando l'utente formatta un disco rigido come *disco di base*.</span><span class="sxs-lookup"><span data-stu-id="5bce6-114">Partitions are created when the user formats a hard disk as a *basic disk*.</span></span> <span data-ttu-id="5bce6-115">Windows supporta inoltre i *dischi dinamici*, che non vengono discussi in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5bce6-115">Windows also supports *dynamic disks*, which are not discussed in this topic.</span></span> <span data-ttu-id="5bce6-116">Per altre informazioni sui dischi di base e i dischi dinamici, vedere [dischi di base e dinamici](basic-and-dynamic-disks.md).</span><span class="sxs-lookup"><span data-stu-id="5bce6-116">For more information about basic disks and dynamic disks, see [Basic and Dynamic Disks](basic-and-dynamic-disks.md).</span></span>

<span data-ttu-id="5bce6-117">La creazione di più partizioni in un disco consente l'aspetto di dischi rigidi separati.</span><span class="sxs-lookup"><span data-stu-id="5bce6-117">The creation of multiple partitions on a disk allows the appearance of having separate hard drives.</span></span> <span data-ttu-id="5bce6-118">Un sistema con un disco rigido con una partizione, ad esempio, contiene un singolo volume, designato dal sistema come unità C. Un sistema con un disco rigido con due partizioni contiene in genere unità C e D. La presenza di più partizioni in un disco rigido può semplificare la gestione del sistema, ad esempio per organizzare i file o per supportare più utenti.</span><span class="sxs-lookup"><span data-stu-id="5bce6-118">For example, a system with one hard disk that has one partition contains a single volume, designated by the system as drive C. A system with a hard disk with two partitions typically contains drives C and D. Having multiple partitions on a hard disk can make it easier to manage the system, for example to organize files or to support multiple users.</span></span>

<span data-ttu-id="5bce6-119">Il primo settore fisico in un disco di base contiene una struttura di dati nota come MBR (master boot record).</span><span class="sxs-lookup"><span data-stu-id="5bce6-119">The first physical sector on a basic disk contains a data structure known as the Master Boot Record (MBR).</span></span> <span data-ttu-id="5bce6-120">Il MBR contiene gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5bce6-120">The MBR contains the following:</span></span>

-   <span data-ttu-id="5bce6-121">Un programma di avvio (dimensioni fino a 442 byte)</span><span class="sxs-lookup"><span data-stu-id="5bce6-121">A boot program (up to 442 bytes in size)</span></span>
-   <span data-ttu-id="5bce6-122">Firma del disco (un numero univoco di 4 byte)</span><span class="sxs-lookup"><span data-stu-id="5bce6-122">A disk signature (a unique 4-byte number)</span></span>
-   <span data-ttu-id="5bce6-123">Una tabella di partizione (fino a quattro voci)</span><span class="sxs-lookup"><span data-stu-id="5bce6-123">A partition table (up to four entries)</span></span>
-   <span data-ttu-id="5bce6-124">Indicatore di fine MBR (always 0x55AA)</span><span class="sxs-lookup"><span data-stu-id="5bce6-124">An end-of-MBR marker (always 0x55AA)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bce6-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5bce6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bce6-126">Informazioni sulla gestione dei volumi</span><span class="sxs-lookup"><span data-stu-id="5bce6-126">About Volume Management</span></span>](about-volume-management.md)
</dt> <dt>

[<span data-ttu-id="5bce6-127">Dischi di base e dinamici</span><span class="sxs-lookup"><span data-stu-id="5bce6-127">Basic and Dynamic Disks</span></span>](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



