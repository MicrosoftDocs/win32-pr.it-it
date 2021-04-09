---
description: CNG è un'API di crittografia che è possibile usare per creare software di sicurezza della crittografia per la gestione delle chiavi di crittografia, la crittografia e la sicurezza dei dati, nonché la crittografia e la sicurezza di rete.
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 'API di crittografia: prossima generazione'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878518"
---
# <a name="cryptography-api-next-generation"></a><span data-ttu-id="2c848-103">API di crittografia: prossima generazione</span><span class="sxs-lookup"><span data-stu-id="2c848-103">Cryptography API: Next Generation</span></span>

## <a name="purpose"></a><span data-ttu-id="2c848-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="2c848-104">Purpose</span></span>

<span data-ttu-id="2c848-105">Cryptography API: Next Generation (CNG) è la sostituzione a lungo termine per [*CryptoAPI*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2c848-105">Cryptography API: Next Generation (CNG) is the long-term replacement for the [*CryptoAPI*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2c848-106">CNG è progettato per essere estendibile a molti livelli ed è indipendente dalla crittografia nel comportamento.</span><span class="sxs-lookup"><span data-stu-id="2c848-106">CNG is designed to be extensible at many levels and cryptography agnostic in behavior.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2c848-107">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="2c848-107">Developer audience</span></span>

<span data-ttu-id="2c848-108">CNG è progettato per essere usato dagli sviluppatori di applicazioni che consentiranno agli utenti di creare e scambiare documenti e altri dati in un ambiente protetto, soprattutto su supporti non protetti, ad esempio Internet.</span><span class="sxs-lookup"><span data-stu-id="2c848-108">CNG is intended for use by developers of applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="2c848-109">Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="2c848-109">Developers should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="2c848-110">Sebbene non sia obbligatorio, è consigliabile comprendere la crittografia o gli argomenti relativi alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="2c848-110">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="2c848-111">Se si sviluppa un provider di algoritmi di crittografia CNG o un provider di archiviazione chiavi, è necessario scaricare [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c848-111">If you are developing a CNG cryptographic algorithm provider or key storage provider, you must download the [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) from Microsoft.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2c848-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="2c848-112">Run-time requirements</span></span>

<span data-ttu-id="2c848-113">CNG è supportato a partire da Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2c848-113">CNG is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="2c848-114">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="2c848-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2c848-115">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2c848-115">In this section</span></span>



| <span data-ttu-id="2c848-116">Argomento</span><span class="sxs-lookup"><span data-stu-id="2c848-116">Topic</span></span>                                         | <span data-ttu-id="2c848-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c848-117">Description</span></span>                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c848-118">Informazioni su CNG</span><span class="sxs-lookup"><span data-stu-id="2c848-118">About CNG</span></span>](about-cng.md)<br/>         | <span data-ttu-id="2c848-119">Descrive le funzionalità CNG, le primitive crittografiche e l'archiviazione delle chiavi, il recupero, l'importazione e l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="2c848-119">Describes CNG features, cryptographic primitives, and key storage, retrieval, import, and export.</span></span><br/>                                   |
| [<span data-ttu-id="2c848-120">Uso di CNG</span><span class="sxs-lookup"><span data-stu-id="2c848-120">Using CNG</span></span>](using-cng.md)<br/>         | <span data-ttu-id="2c848-121">Viene illustrato come utilizzare le funzionalità di configurazione della crittografia di CNG e la tipica programmazione CNG.</span><span class="sxs-lookup"><span data-stu-id="2c848-121">Explains how to use the cryptography configuration features of CNG and typical CNG programming.</span></span><br/>                                     |
| [<span data-ttu-id="2c848-122">Riferimento CNG</span><span class="sxs-lookup"><span data-stu-id="2c848-122">CNG Reference</span></span>](cng-reference.md)<br/> | <span data-ttu-id="2c848-123">Descrizioni dettagliate degli elementi di programmazione CNG.</span><span class="sxs-lookup"><span data-stu-id="2c848-123">Detailed descriptions of the CNG programming elements.</span></span> <span data-ttu-id="2c848-124">Queste pagine includono descrizioni di riferimento dell'API per l'uso di CNG.</span><span class="sxs-lookup"><span data-stu-id="2c848-124">These pages include reference descriptions of the API for working with CNG.</span></span> <br/> |



 

 

