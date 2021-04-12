---
title: SRPTrustLevel
description: Imposta il livello di attendibilità del criterio di restrizione software per le applicazioni.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- Valore SRPTrustLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395658"
---
# <a name="srptrustlevel"></a><span data-ttu-id="52ed7-104">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="52ed7-104">SRPTrustLevel</span></span>

<span data-ttu-id="52ed7-105">Imposta il livello di attendibilità del criterio di restrizione software per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="52ed7-105">Sets the software restriction policy (SRP) trust level for applications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="52ed7-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="52ed7-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a><span data-ttu-id="52ed7-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="52ed7-107">Remarks</span></span>

<span data-ttu-id="52ed7-108">Si tratta di un valore **reg \_ DWORD** disponibile a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="52ed7-108">This is a **REG\_DWORD** value that is available starting with Windows XP.</span></span>



| <span data-ttu-id="52ed7-109">Valore</span><span class="sxs-lookup"><span data-stu-id="52ed7-109">Value</span></span>                                 | <span data-ttu-id="52ed7-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52ed7-110">Description</span></span>                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52ed7-111">0x0 (LEVELID più sicuro non \_ \_ consentito)</span><span class="sxs-lookup"><span data-stu-id="52ed7-111">0x0 (SAFER\_LEVELID\_DISALLOWED)</span></span>      | <span data-ttu-id="52ed7-112">L'applicazione non è consentita per l'accesso e i privilegi utente sensibili alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="52ed7-112">The application is disallowed from accessing and security-sensitive user privileges.</span></span> |
| <span data-ttu-id="52ed7-113">0x40000 (SAFE \_ LEVELID \_ FULLYTRUSTED)</span><span class="sxs-lookup"><span data-stu-id="52ed7-113">0x40000 (SAFE\_LEVELID\_FULLYTRUSTED)</span></span> | <span data-ttu-id="52ed7-114">L'applicazione dispone di accesso illimitato ai privilegi dell'utente.</span><span class="sxs-lookup"><span data-stu-id="52ed7-114">The application has unrestricted access to the user's privileges.</span></span>                    |



 

<span data-ttu-id="52ed7-115">Se il valore **SRPTrustLevel** non esiste, viene utilizzato il valore predefinito di LEVELID più sicuro non \_ \_ consentito.</span><span class="sxs-lookup"><span data-stu-id="52ed7-115">If the **SRPTrustLevel** value does not exist, the default value of SAFER\_LEVELID\_DISALLOWED is used.</span></span> <span data-ttu-id="52ed7-116">Se **SRPTrustLevel** è del tipo errato o non è compreso nell'intervallo, com restituisce l'errore COMAdmin \_ E \_ SAFERINVALID.</span><span class="sxs-lookup"><span data-stu-id="52ed7-116">If **SRPTrustLevel** is of the wrong type or out of range, COM returns the error COMADMIN\_E\_SAFERINVALID.</span></span> <span data-ttu-id="52ed7-117">Se l'attivazione di un ordinamento ha esito negativo a causa dei controlli di attendibilità SRP, COM restituisce l'errore CO \_ E \_ ACTIVATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="52ed7-117">If an activation of any sort fails because of SRP trust checks, COM returns the error CO\_E\_ACTIVATIONFAILED.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52ed7-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52ed7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52ed7-119">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="52ed7-119">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="52ed7-120">**SRPActivateAsActivatorChecks**</span><span class="sxs-lookup"><span data-stu-id="52ed7-120">**SRPActivateAsActivatorChecks**</span></span>](srpactivateasactivatorchecks.md)
</dt> <dt>

[<span data-ttu-id="52ed7-121">**SRPRunningObjectChecks**</span><span class="sxs-lookup"><span data-stu-id="52ed7-121">**SRPRunningObjectChecks**</span></span>](srprunningobjectchecks.md)
</dt> </dl>

 

 




