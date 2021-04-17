---
description: Il provider del servizio di crittografia di base Microsoft è il provider del provider del servizio di crittografia (CSP) iniziale ed è distribuito con le versioni CryptoAPI 1,0 e 2,0. Si tratta di un provider di uso generico che supporta le firme digitali e la crittografia dei dati.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Provider di crittografia di base Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc48060305337dd878dedcadca8cfed52bd2f34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307677"
---
# <a name="microsoft-base-cryptographic-provider"></a><span data-ttu-id="0f949-104">Provider di crittografia di base Microsoft</span><span class="sxs-lookup"><span data-stu-id="0f949-104">Microsoft Base Cryptographic Provider</span></span>

<span data-ttu-id="0f949-105">Il provider del servizio di crittografia di base Microsoft è il provider del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) iniziale ed è distribuito con le versioni [*CryptoAPI*](../secgloss/c-gly.md) 1,0 e 2,0.</span><span class="sxs-lookup"><span data-stu-id="0f949-105">The Microsoft Base Cryptographic Provider is the initial [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) provider, and is distributed with [*CryptoAPI*](../secgloss/c-gly.md) versions 1.0 and 2.0.</span></span> <span data-ttu-id="0f949-106">Si tratta di un provider di uso generico che supporta le [*firme digitali*](../secgloss/d-gly.md) e la crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="0f949-106">It is a general-purpose provider that supports [*digital signatures*](../secgloss/d-gly.md) and data encryption.</span></span>

<span data-ttu-id="0f949-107">L'algoritmo di chiave pubblica RSA viene utilizzato per tutte le operazioni con chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="0f949-107">The RSA public key algorithm is used for all public key operations.</span></span>

<span data-ttu-id="0f949-108">Per mantenere la compatibilità con le versioni precedenti, la nuova versione del provider mantiene la designazione della versione 1,0 del nome in WinCrypt. h.</span><span class="sxs-lookup"><span data-stu-id="0f949-108">To maintain backward compatibility with earlier versions the new version of the provider retains the version 1.0 designation of the name in Wincrypt.h.</span></span> <span data-ttu-id="0f949-109">Tuttavia, la versione 2,0 di questo provider è attualmente in fase di spedizione.</span><span class="sxs-lookup"><span data-stu-id="0f949-109">However, version 2.0 of this provider is currently shipping.</span></span> <span data-ttu-id="0f949-110">Per determinare la versione effettiva del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con l'argomento *DwParam* impostato su **PP \_ Version**.</span><span class="sxs-lookup"><span data-stu-id="0f949-110">To determine the actual version of the provider in use, call [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with the *dwParam* argument set to **PP\_VERSION**.</span></span> <span data-ttu-id="0f949-111">Se 0x0200 viene restituito in *pbData*, si avrà la versione 2,0.</span><span class="sxs-lookup"><span data-stu-id="0f949-111">If 0x0200 is returned in *pbData*, then you have version 2.0.</span></span>

|                |                     |
|----------------|---------------------|
| <span data-ttu-id="0f949-112">Tipo di provider:</span><span class="sxs-lookup"><span data-stu-id="0f949-112">Provider type:</span></span> | <span data-ttu-id="0f949-113">**PROV \_ RSA \_ completo**</span><span class="sxs-lookup"><span data-stu-id="0f949-113">**PROV\_RSA\_FULL**</span></span> |
| <span data-ttu-id="0f949-114">Nome provider:</span><span class="sxs-lookup"><span data-stu-id="0f949-114">Provider name:</span></span> | <span data-ttu-id="0f949-115">**MS \_ def \_ prova**</span><span class="sxs-lookup"><span data-stu-id="0f949-115">**MS\_DEF\_PROV**</span></span>   |



 

 

 
