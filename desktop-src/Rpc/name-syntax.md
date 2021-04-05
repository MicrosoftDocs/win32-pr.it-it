---
title: Sintassi del nome
description: RPC (Remote Procedure Call) e sintassi del nome.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955653"
---
# <a name="name-syntax"></a><span data-ttu-id="1a3f2-103">Sintassi del nome</span><span class="sxs-lookup"><span data-stu-id="1a3f2-103">Name Syntax</span></span>

<span data-ttu-id="1a3f2-104">Microsoft RPC accetta nomi conformi alla sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="1a3f2-104">Microsoft RPC accepts names that conform to the following syntax:</span></span>

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a><span data-ttu-id="1a3f2-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a3f2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a3f2-106"><span id="name"></span><span id="NAME"></span>nome</span><span class="sxs-lookup"><span data-stu-id="1a3f2-106"><span id="name"></span><span id="NAME"></span>name</span></span>
</dt> <dd>

<span data-ttu-id="1a3f2-107">Specifica un identificatore che può contenere qualsiasi carattere eccetto il carattere barra (/) di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-107">Specifies an identifier that can contain any character except the delimiting slash (/) character.</span></span>

</dd> <dt>

<span data-ttu-id="1a3f2-108"><span id="domainname"></span><span id="DOMAINNAME"></span>NomeDominio</span><span class="sxs-lookup"><span data-stu-id="1a3f2-108"><span id="domainname"></span><span id="DOMAINNAME"></span>domainname</span></span>
</dt> <dd>

<span data-ttu-id="1a3f2-109">Specifica il nome del dominio.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-109">Specifies the name of the domain.</span></span>

</dd> </dl>

<span data-ttu-id="1a3f2-110">Un parametro che seleziona il tipo di sintassi del nome e la stringa che specifica il nome vengono forniti a molte delle funzioni RPC NSI (Name Service Interface).</span><span class="sxs-lookup"><span data-stu-id="1a3f2-110">A parameter that selects the name-syntax type and the string that specifies the name are supplied to many of the name service interface (NSI) RPC functions.</span></span>

<span data-ttu-id="1a3f2-111">Microsoft RPC supporta solo un tipo di sintassi dei nomi, come specificato dalla costante RPC \_ C \_ NS \_ sintassi \_ DCE.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-111">Only one name-syntax type is supported by Microsoft RPC, as specified by the constant RPC\_C\_NS\_SYNTAX\_DCE.</span></span> <span data-ttu-id="1a3f2-112">Questa costante viene definita nel file di intestazione RPCNSI. H.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-112">This constant is defined in the header file RPCNSI.H.</span></span>

<span data-ttu-id="1a3f2-113">La sintassi del nome specificata dalla sintassi RPC \_ C \_ NS \_ \_ (DCE) è un'estensione della \_ sintassi del nome del servizio di directory di celle (CDS) OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-113">The name syntax specified by RPC\_C\_NS\_SYNTAX\_DCE is an extension of the OSF\_DCE Cell Directory Service (CDS) name syntax.</span></span> <span data-ttu-id="1a3f2-114">La possibilità di specificare un nome di dominio rappresenta un'estensione di tale sintassi.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-114">The ability to specify a domain name represents an extension to that syntax.</span></span> <span data-ttu-id="1a3f2-115">Non esiste alcun limite assoluto per il numero di nomi che possono essere separati da una barra, purché la stringa complessiva sia inferiore a 256 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-115">There is no absolute limit on the number of names that can be separated by slash characters as long as the overall string is less than 256 characters.</span></span>

<span data-ttu-id="1a3f2-116">Le barre consentono di specificare una struttura logica per il nome, ma non corrispondono a una struttura logica negli oggetti stessi.</span><span class="sxs-lookup"><span data-stu-id="1a3f2-116">The slashes allow you to specify a logical structure to the name, but they do not correspond to a logical structure in the objects themselves.</span></span>

 

 




