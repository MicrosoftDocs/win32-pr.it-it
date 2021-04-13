---
description: Elenca i tipi di dati usati dalle API di autenticazione.
ms.assetid: 1c2f932d-11f4-406f-8874-2f247b53d70f
title: Tipi di dati di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38873b3385817187469466bf67f350a7f0701d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347316"
---
# <a name="authentication-data-types"></a><span data-ttu-id="fb793-103">Tipi di dati di autenticazione</span><span class="sxs-lookup"><span data-stu-id="fb793-103">Authentication Data Types</span></span>

## <a name="lsa-data-types"></a><span data-ttu-id="fb793-104">Tipi di dati LSA</span><span class="sxs-lookup"><span data-stu-id="fb793-104">LSA Data Types</span></span>

<span data-ttu-id="fb793-105">Nell' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) viene utilizzato il tipo di dati seguente.</span><span class="sxs-lookup"><span data-stu-id="fb793-105">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) uses the following data type.</span></span>



| <span data-ttu-id="fb793-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fb793-106">Data type</span></span>                                            | <span data-ttu-id="fb793-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb793-107">Description</span></span>                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb793-108">**\_richiesta client \_ PLSA**</span><span class="sxs-lookup"><span data-stu-id="fb793-108">**PLSA\_CLIENT\_REQUEST**</span></span>](plsa-client-request.md) | <span data-ttu-id="fb793-109">Tipo di dati opaco utilizzato internamente dall'LSA per mantenere le informazioni sul client correlate a singole richieste.</span><span class="sxs-lookup"><span data-stu-id="fb793-109">An opaque data type used internally by the LSA to maintain client information related to individual requests.</span></span><br/> |



 

## <a name="sspi-data-types-and-values"></a><span data-ttu-id="fb793-110">Tipi di dati e valori di SSPI</span><span class="sxs-lookup"><span data-stu-id="fb793-110">SSPI Data Types and Values</span></span>

<span data-ttu-id="fb793-111">[SSPI](sspi.md) utilizza i dati e i tipi enumerati seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb793-111">[SSPI](sspi.md) uses the following data and enumerated types.</span></span>



| <span data-ttu-id="fb793-112">Tipo di dati o valore</span><span class="sxs-lookup"><span data-stu-id="fb793-112">Data type or value</span></span>                         | <span data-ttu-id="fb793-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb793-113">Description</span></span>                                                                      |
|--------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="fb793-114">Handle SSPI</span><span class="sxs-lookup"><span data-stu-id="fb793-114">SSPI Handles</span></span>](sspi-handles.md)           | <span data-ttu-id="fb793-115">I tipi di handle e i puntatori di SSPI a questi handle.</span><span class="sxs-lookup"><span data-stu-id="fb793-115">SSPI handle types and pointers to these handles.</span></span><br/>                      |
| [<span data-ttu-id="fb793-116">Codici di stato SSPI</span><span class="sxs-lookup"><span data-stu-id="fb793-116">SSPI Status Codes</span></span>](sspi-status-codes.md) | <span data-ttu-id="fb793-117">Codici di stato restituiti nelle applicazioni SSPI.</span><span class="sxs-lookup"><span data-stu-id="fb793-117">Status codes returned in SSPI applications.</span></span><br/>                           |
| [<span data-ttu-id="fb793-118">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="fb793-118">TimeStamp</span></span>](timestamp.md)                 | <span data-ttu-id="fb793-119">Tipo definito che consente di conservare le informazioni sulla validità del tempo dei token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fb793-119">Defined type to hold information on time validity of security tokens.</span></span><br/> |



 

 

