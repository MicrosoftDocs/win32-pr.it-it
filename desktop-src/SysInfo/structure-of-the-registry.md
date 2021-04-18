---
description: Il registro di sistema è un database gerarchico che contiene dati cruciali per il funzionamento di Windows e delle applicazioni e dei servizi eseguiti in Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Struttura del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563424"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="b4d9b-103">Struttura del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b4d9b-103">Structure of the Registry</span></span>

<span data-ttu-id="b4d9b-104">Il registro di sistema è un database gerarchico che contiene dati cruciali per il funzionamento di Windows e delle applicazioni e dei servizi eseguiti in Windows.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="b4d9b-105">I dati sono strutturati in un formato struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-105">The data is structured in a tree format.</span></span> <span data-ttu-id="b4d9b-106">Ogni nodo dell'albero è denominato *chiave*.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="b4d9b-107">Ogni chiave può contenere sia *sottochiavi* che voci di dati denominate *valori*.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="b4d9b-108">In alcuni casi, la presenza di una chiave è costituita da tutti i dati richiesti da un'applicazione. in altri casi, un'applicazione apre una chiave e usa i valori associati alla chiave.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="b4d9b-109">Una chiave può avere un numero qualsiasi di valori e i valori possono essere in qualsiasi formato.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="b4d9b-110">Per altre informazioni, vedere [tipi di valore del registro](registry-value-types.md) di sistema e [limiti delle dimensioni degli elementi del registro](registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="b4d9b-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="b4d9b-111">Ogni chiave ha un nome costituito da uno o più caratteri stampabili.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="b4d9b-112">Per i nomi di chiave non viene fatta distinzione tra maiuscole</span><span class="sxs-lookup"><span data-stu-id="b4d9b-112">Key names are not case sensitive.</span></span> <span data-ttu-id="b4d9b-113">I nomi di chiave non possono includere il carattere barra rovesciata ( \) , ma è possibile usare qualsiasi altro carattere stampabile.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-113">Key names cannot include the backslash character (\), but any other printable character can be used.</span></span> <span data-ttu-id="b4d9b-114">I nomi dei valori e i dati possono includere il carattere barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="b4d9b-115">Il nome di ogni sottochiave è univoco rispetto alla chiave immediatamente superiore nella gerarchia.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="b4d9b-116">I nomi delle chiavi non sono localizzati in altre lingue, anche se i valori possono essere.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="b4d9b-117">Nella figura seguente è riportato un esempio di struttura di chiavi del registro di sistema come visualizzato dall'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![finestra dell'editor del registro di sistema](images/regtree.png)

<span data-ttu-id="b4d9b-119">Ogni albero sotto **computer locale** è una chiave.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="b4d9b-120">La chiave del **\_ \_ computer locale HKEY** presenta le sottochiavi seguenti: **hardware**, **Sam**, **Security**, **software** e **System**.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="b4d9b-121">Ognuna di queste chiavi a sua volta contiene sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="b4d9b-122">Ad esempio, la chiave **hardware** presenta le sottochiavi **Description**, **DEVICEMAP** e **RESOURCEMAP**; la chiave **DEVICEMAP** include diverse sottochiavi, incluso il **video**.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="b4d9b-123">Ogni valore è costituito da un nome di valore e dai dati associati, se presenti.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="b4d9b-124">**MaxObjectNumber** e **VgaCompatible** sono valori che contengono dati nella sottochiave **video** .</span><span class="sxs-lookup"><span data-stu-id="b4d9b-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="b4d9b-125">Un albero del registro di sistema può avere una profondità di 512 livelli.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="b4d9b-126">È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b4d9b-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4d9b-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b4d9b-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b4d9b-128">[Panoramica del registro di sistema di Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b4d9b-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
