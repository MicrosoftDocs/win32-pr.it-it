---
title: Informazioni sulle versioni
description: In questo argomento vengono illustrate le funzioni delle informazioni sulla versione.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- risorse, informazioni sulla versione
- informazioni sulla versione
- aggiunta di informazioni sulla versione
- conflitti di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398920"
---
# <a name="about-version-information"></a><span data-ttu-id="7bea2-107">Informazioni sulle versioni</span><span class="sxs-lookup"><span data-stu-id="7bea2-107">About Version Information</span></span>

<span data-ttu-id="7bea2-108">È possibile utilizzare le funzioni di informazioni sulla versione per determinare la posizione in cui deve essere installato un file e identificare i conflitti con i file attualmente installati.</span><span class="sxs-lookup"><span data-stu-id="7bea2-108">You can use the version information functions to determine where a file should be installed and identify conflicts with currently installed files.</span></span> <span data-ttu-id="7bea2-109">Queste funzioni consentono di evitare i problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7bea2-109">These functions enable you to avoid the following problems:</span></span>

-   <span data-ttu-id="7bea2-110">installazione di versioni precedenti dei componenti rispetto a versioni più recenti</span><span class="sxs-lookup"><span data-stu-id="7bea2-110">installing older versions of components over newer versions</span></span>
-   <span data-ttu-id="7bea2-111">modifica della lingua in un sistema con linguaggio misto senza notifica</span><span class="sxs-lookup"><span data-stu-id="7bea2-111">changing the language in a mixed-language system without notification</span></span>
-   <span data-ttu-id="7bea2-112">installazione di più copie di una raccolta in directory diverse</span><span class="sxs-lookup"><span data-stu-id="7bea2-112">installing multiple copies of a library in different directories</span></span>
-   <span data-ttu-id="7bea2-113">copia di file in directory di rete condivise da più utenti</span><span class="sxs-lookup"><span data-stu-id="7bea2-113">copying files to network directories shared by multiple users</span></span>

<span data-ttu-id="7bea2-114">Le funzioni di informazioni sulla versione consentono alle applicazioni di eseguire query su una risorsa di versione per ottenere informazioni sui file e presentare le informazioni in un formato non crittografato.</span><span class="sxs-lookup"><span data-stu-id="7bea2-114">The version information functions enable applications to query a version resource for file information and present the information in a clear format.</span></span> <span data-ttu-id="7bea2-115">Queste informazioni includono lo scopo, l'autore, il numero di versione e così via del file.</span><span class="sxs-lookup"><span data-stu-id="7bea2-115">This information includes the file's purpose, author, version number, and so on.</span></span>

<span data-ttu-id="7bea2-116">È possibile aggiungere informazioni sulla versione a tutti i file che possono avere risorse di Windows, ad esempio le dll, i file eseguibili o i file del tipo di carattere fon.</span><span class="sxs-lookup"><span data-stu-id="7bea2-116">You can add version information to any files that can have Windows resources, such as DLLs, executable files, or .fon font files.</span></span> <span data-ttu-id="7bea2-117">Per aggiungere le informazioni, creare una [risorsa VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) e usare il compilatore di risorse per compilare la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7bea2-117">To add the information, create a [VERSIONINFO Resource](/windows/desktop/menurc/versioninfo-resource) and use the resource compiler to compile the resource.</span></span>

 

 