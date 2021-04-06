---
description: L'estendibilità viene eseguita fornendo per l'utilizzo di nuovi identificatori di oggetto (OID), nuovi tipi di codifica e nuove dll.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: Panoramica di OID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883610"
---
# <a name="oid-overview"></a><span data-ttu-id="e15c8-103">Panoramica di OID</span><span class="sxs-lookup"><span data-stu-id="e15c8-103">OID Overview</span></span>

<span data-ttu-id="e15c8-104">L'estendibilità viene eseguita fornendo per l'utilizzo di nuovi [*identificatori di oggetto*](../secgloss/o-gly.md) (OID), nuovi tipi di codifica e nuove dll.</span><span class="sxs-lookup"><span data-stu-id="e15c8-104">Extensibility is achieved by providing for the use of new [*object identifiers*](../secgloss/o-gly.md) (OIDs), new encoding types, and new DLLs.</span></span>

<span data-ttu-id="e15c8-105">CryptoAPI OID può assumere uno dei seguenti formati:</span><span class="sxs-lookup"><span data-stu-id="e15c8-105">CryptoAPI OIDs can take any of the following forms:</span></span>

-   <span data-ttu-id="e15c8-106">Stringa numerica, ad esempio "1.2.3.500.88"</span><span class="sxs-lookup"><span data-stu-id="e15c8-106">A numeric string such as "1.2.3.500.88"</span></span>
-   <span data-ttu-id="e15c8-107">Stringa alfanumerica, ad esempio *funzione*</span><span class="sxs-lookup"><span data-stu-id="e15c8-107">An alphanumeric string such as *MyFunction*</span></span>
-   <span data-ttu-id="e15c8-108">Costante con un valore minore o uguale a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="e15c8-108">A constant with a value that is less than or equal to 0xFFFF.</span></span> <span data-ttu-id="e15c8-109">Queste costanti sono spesso associate a un nome tramite l'utilizzo di un'istruzione **\# define** in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="e15c8-109">These constants are often associated with a name through the use of a **\#define** statement in a header file.</span></span>

<span data-ttu-id="e15c8-110">Le funzioni estendibili accettano gli argomenti di tipo OID e di codifica.</span><span class="sxs-lookup"><span data-stu-id="e15c8-110">Extensible functions accept OID and encoding type arguments.</span></span> <span data-ttu-id="e15c8-111">Queste funzioni consentono di eseguire ricerche nel registro di sistema per trovare una DLL associata all'OID e gli argomenti di tipo di codifica passati alla funzione.</span><span class="sxs-lookup"><span data-stu-id="e15c8-111">These functions search the system registry to find a DLL associated with the OID and encoding type arguments passed to the function.</span></span> <span data-ttu-id="e15c8-112">Se viene rilevata una DLL per il tipo di codifica OID, viene caricata la DLL e viene chiamata la relativa funzione.</span><span class="sxs-lookup"><span data-stu-id="e15c8-112">If a DLL for the OID, encoding type combination is found, the DLL is loaded and its function is called.</span></span> <span data-ttu-id="e15c8-113">La figura seguente illustra questo flusso per la funzione [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) :</span><span class="sxs-lookup"><span data-stu-id="e15c8-113">The following illustration shows this flow for the [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) function:</span></span>

![flusso OID](images/oidflow.png)

<span data-ttu-id="e15c8-115">Ciò consente di estendere la funzionalità della CryptoAPI in modo da richiedere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="e15c8-115">This allows the functionality of the CryptoAPI to be extended as the need arises.</span></span> <span data-ttu-id="e15c8-116">L'uso di questa metodologia impone agli sviluppatori della nuova funzionalità di scrivere tutto il codice necessario per tale funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e15c8-116">Use of this methodology places a burden on the developer of the new functionality to write all the necessary code for that functionality.</span></span> <span data-ttu-id="e15c8-117">Per codificare una nuova struttura di dati, ad esempio, la funzione nella DLL deve eseguire l'intero processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="e15c8-117">To encode some new data structure, for example, the function in the DLL must perform the entire encoding process.</span></span>

 

 
