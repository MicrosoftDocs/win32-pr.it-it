---
description: Crypt32.dll è il modulo che implementa molte delle funzioni CryptoAPI.
ms.assetid: b6063c92-5831-4b78-b2cd-812e55194bc9
title: Versioni Crypt32.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b55d78b3ff3654e4bf3e5956917dd8de20eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750922"
---
# <a name="crypt32dll-versions"></a><span data-ttu-id="d2362-103">Versioni Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="d2362-103">Crypt32.dll Versions</span></span>

<span data-ttu-id="d2362-104">Crypt32.dll è il modulo che implementa molte delle funzioni di messaggistica crittografica e di certificato in CryptoAPI, ad esempio [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span><span class="sxs-lookup"><span data-stu-id="d2362-104">Crypt32.dll is the module that implements many of the Certificate and Cryptographic Messaging functions in the CryptoAPI, such as [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage).</span></span> <span data-ttu-id="d2362-105">Crypt32.dll è un modulo fornito con i sistemi operativi Windows e Windows Server, ma versioni diverse di questa DLL offrono funzionalità diverse.</span><span class="sxs-lookup"><span data-stu-id="d2362-105">Crypt32.dll is a module that comes with the Windows and Windows Server operating systems, but different versions of this DLL provide different capabilities.</span></span> <span data-ttu-id="d2362-106">Non è disponibile alcuna API per determinare la versione di CryptoAPI in uso, ma è possibile determinare la versione di Crypt32.dll attualmente in uso usando le funzioni [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) e [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) .</span><span class="sxs-lookup"><span data-stu-id="d2362-106">There is no API to determine the version of CryptoAPI that is in use, but you can determine the version of Crypt32.dll that is currently in use by using the [**GetFileVersionInfo**](/windows/win32/api/winver/nf-winver-getfileversioninfoa) and [**VerQueryValue**](/windows/win32/api/winver/nf-winver-verqueryvaluea) functions.</span></span>

<span data-ttu-id="d2362-107">In generale, gli intervalli di versione di Crypt32.dll mappato alle versioni del sistema operativo, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d2362-107">In general, the version ranges of Crypt32.dll map to the operating system versions as shown in the following table.</span></span> <span data-ttu-id="d2362-108">Questa tabella, tuttavia, deve essere utilizzata come riferimento solo perché è possibile, attraverso altre vie di aggiornamento, che la versione del Crypt32.dll sia diversa da quella indicata nella tabella.</span><span class="sxs-lookup"><span data-stu-id="d2362-108">However, this table should be used as a guideline only because it is possible, through other update avenues, that the Crypt32.dll version will differ from the one indicated in the table.</span></span>

| <span data-ttu-id="d2362-109">Versione Crypt32.dll</span><span class="sxs-lookup"><span data-stu-id="d2362-109">Crypt32.dll version</span></span>                               | <span data-ttu-id="d2362-110">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d2362-110">Operating system</span></span>                                                                                                                                                                |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2362-111">*versione* >= 5.131.3790.0</span><span class="sxs-lookup"><span data-stu-id="d2362-111">*version* >= 5.131.3790.0</span></span>                      | <span data-ttu-id="d2362-112">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d2362-112">Windows Server 2003</span></span>                                                                                                                                                             |
| <span data-ttu-id="d2362-113">*versione* >= 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="d2362-113">*version* >= 5.131.2600.1243</span></span>                   | <span data-ttu-id="d2362-114">Windows XP con Service Pack 2 (SP2) Windows XP con Service Pack 1 (SP1) con hotfix [Q329433](https://support.microsoft.com/kb/329433)</span><span class="sxs-lookup"><span data-stu-id="d2362-114">Windows XP with Service Pack 2 (SP2)Windows XP with Service Pack 1 (SP1) with hotfix [Q329433](https://support.microsoft.com/kb/329433)</span></span><br/> <span data-ttu-id="d2362-115">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2362-115">Windows XP</span></span><br/> |
| <span data-ttu-id="d2362-116">5.131.2600.0 <= *versione* < 5.131.2600.1243</span><span class="sxs-lookup"><span data-stu-id="d2362-116">5.131.2600.0 <= *version* < 5.131.2600.1243</span></span> | <span data-ttu-id="d2362-117">Windows XP con SP1Windows XP</span><span class="sxs-lookup"><span data-stu-id="d2362-117">Windows XP with SP1Windows XP</span></span><br/>                                                                                                                                        |



 

 

 
