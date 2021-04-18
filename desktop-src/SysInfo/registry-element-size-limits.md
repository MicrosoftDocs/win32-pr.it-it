---
description: La tabella seguente identifica i limiti delle dimensioni per i vari elementi del registro di sistema.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Limiti delle dimensioni degli elementi del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313267"
---
# <a name="registry-element-size-limits"></a><span data-ttu-id="dd877-103">Limiti delle dimensioni degli elementi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="dd877-103">Registry Element Size Limits</span></span>

<span data-ttu-id="dd877-104">La tabella seguente identifica i limiti delle dimensioni per i vari elementi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dd877-104">The following table identifies the size limits for the various registry elements.</span></span>



| <span data-ttu-id="dd877-105">Elemento Registry</span><span class="sxs-lookup"><span data-stu-id="dd877-105">Registry Element</span></span> | <span data-ttu-id="dd877-106">Limite dimensione</span><span class="sxs-lookup"><span data-stu-id="dd877-106">Size Limit</span></span>                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd877-107">Nome della chiave</span><span class="sxs-lookup"><span data-stu-id="dd877-107">Key name</span></span>         | <span data-ttu-id="dd877-108">255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="dd877-108">255 characters.</span></span> <span data-ttu-id="dd877-109">Il nome della chiave include il percorso assoluto della chiave nel registro di sistema, iniziando sempre con una chiave di base, ad esempio \_ HKEY \_ macchina locale.</span><span class="sxs-lookup"><span data-stu-id="dd877-109">The key name includes the absolute path of the key in the registry, always starting at a base key, for example, HKEY\_LOCAL\_MACHINE.</span></span> |
| <span data-ttu-id="dd877-110">Nome del valore</span><span class="sxs-lookup"><span data-stu-id="dd877-110">Value name</span></span>       | <span data-ttu-id="dd877-111">16.383 caratteri **Windows 2000:** 260 caratteri ANSI o 16.383 caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="dd877-111">16,383 characters **Windows 2000:** 260 ANSI characters or 16,383 Unicode characters.</span></span><br/>                                                       |
| <span data-ttu-id="dd877-112">Valore</span><span class="sxs-lookup"><span data-stu-id="dd877-112">Value</span></span>            | <span data-ttu-id="dd877-113">Memoria disponibile (formato più recente) 1 MB (formato standard)</span><span class="sxs-lookup"><span data-stu-id="dd877-113">Available memory (latest format)1 MB (standard format)</span></span><br/>                                                                                     |
| <span data-ttu-id="dd877-114">Albero</span><span class="sxs-lookup"><span data-stu-id="dd877-114">Tree</span></span>             | <span data-ttu-id="dd877-115">Un albero del registro di sistema può avere una profondità di 512 livelli.</span><span class="sxs-lookup"><span data-stu-id="dd877-115">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="dd877-116">È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dd877-116">You can create up to 32 levels at a time through a single registry API call.</span></span>                                  |



 

<span data-ttu-id="dd877-117">I valori Long (più di 2.048 byte) devono essere archiviati in un file e il percorso del file deve essere archiviato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dd877-117">Long values (more than 2,048 bytes) should be stored in a file, and the location of the file should be stored in the registry.</span></span> <span data-ttu-id="dd877-118">Ciò consente di eseguire in modo efficiente il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dd877-118">This helps the registry perform efficiently.</span></span>

<span data-ttu-id="dd877-119">Il percorso del file può corrispondere al nome di un valore o ai dati di un valore.</span><span class="sxs-lookup"><span data-stu-id="dd877-119">The file location can be the name of a value or the data of a value.</span></span> <span data-ttu-id="dd877-120">Ogni barra rovesciata nella stringa di posizione deve essere preceduta da un'altra barra rovesciata come carattere di escape.</span><span class="sxs-lookup"><span data-stu-id="dd877-120">Each backslash in the location string must be preceded by another backslash as an escape character.</span></span> <span data-ttu-id="dd877-121">Ad esempio, specificare "C: \\ \\ mydir \\ \\ MyFile" per archiviare la stringa "c: \\ mydir \\ MyFile".</span><span class="sxs-lookup"><span data-stu-id="dd877-121">For example, specify "C:\\\\mydir\\\\myfile" to store the string "C:\\mydir\\myfile".</span></span> <span data-ttu-id="dd877-122">Un percorso di file può essere anche il nome di una chiave se è entro il limite di 255 caratteri per i nomi delle chiavi e non contiene barre rovesciate, che non sono consentite nei nomi di chiave.</span><span class="sxs-lookup"><span data-stu-id="dd877-122">A file location can also be the name of a key if it is within the 255-character limit for key names and does not contain backslashes, which are not allowed in key names.</span></span>

 

 




