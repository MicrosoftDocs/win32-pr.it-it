---
description: Microsoft Base Cryptographic Provider è il provider del provider del servizio di crittografia (CSP) iniziale e viene distribuito con CryptoAPI versioni 1.0 e 2.0. Si tratta di un provider per utilizzo generico che supporta le firme digitali e la crittografia dei dati.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Provider del servizio di crittografia Microsoft Base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581889"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="b8349-104">Provider del servizio di crittografia Microsoft Base</span><span class="sxs-lookup"><span data-stu-id="b8349-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="b8349-105">Microsoft Base Cryptographic Provider è il [*provider*](../secgloss/c-gly.md) del provider del servizio di crittografia (CSP) iniziale e viene distribuito con [*CryptoAPI*](../secgloss/c-gly.md) versioni 1.0 e 2.0.</span><span class="sxs-lookup"><span data-stu-id="b8349-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="b8349-106">Si tratta di un provider per utilizzo generico che supporta le [*firme digitali e*](../secgloss/d-gly.md) la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="b8349-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="b8349-107">L'algoritmo a chiave pubblica RSA viene usato per tutte le operazioni con chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="b8349-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="b8349-108">Per mantenere la compatibilità con le versioni precedenti, la nuova versione del provider mantiene la designazione della versione 1.0 del nome in Wincrypt.h.</span><span class="sxs-lookup"><span data-stu-id="b8349-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="b8349-109">Tuttavia, la versione 2.0 di questo provider è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="b8349-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="b8349-110">Per determinare la versione effettiva del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con l'argomento *dwParam* impostato su **PP \_ VERSION.**</span><span class="sxs-lookup"><span data-stu-id="b8349-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="b8349-111">Se 0x0200 viene restituito in *pbData*, si ha la versione 2.0.</span><span class="sxs-lookup"><span data-stu-id="b8349-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                   | <span data-ttu-id="b8349-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b8349-112">Value</span></span>            |
|-------------------|------------------|
| <span data-ttu-id="b8349-113">**Tipo provider**</span><span class="sxs-lookup"><span data-stu-id="b8349-113">**Provider type**</span></span> | <span data-ttu-id="b8349-114">PROV \_ RSA \_ FULL</span><span class="sxs-lookup"><span data-stu-id="b8349-114">PROV\_RSA\_FULL</span></span>  |
| <span data-ttu-id="b8349-115">**Nome provider**</span><span class="sxs-lookup"><span data-stu-id="b8349-115">**Provider name**</span></span> | <span data-ttu-id="b8349-116">MS \_ DEF \_ PROV</span><span class="sxs-lookup"><span data-stu-id="b8349-116">MS\_DEF\_PROV</span></span>    |



 

 

 
