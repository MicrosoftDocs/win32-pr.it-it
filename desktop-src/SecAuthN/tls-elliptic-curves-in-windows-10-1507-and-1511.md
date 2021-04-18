---
description: Curve ellittiche abilitate in Windows 10 versioni 1507 e 1511.
title: Curve di TLS ellittiche in Windows 10 versione 1507 e 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316205"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a><span data-ttu-id="1ce35-103">Curve di TLS ellittiche in Windows 10 versione 1507 e 1511</span><span class="sxs-lookup"><span data-stu-id="1ce35-103">TLS Elliptic Curves in Windows 10 version 1507 and 1511</span></span>

<span data-ttu-id="1ce35-104">Per Windows 10, versioni 1507 e 1511, le seguenti curve ellittiche sono abilitate e in questo ordine di priorità per impostazione predefinita viene usato il provider Microsoft Schannel:</span><span class="sxs-lookup"><span data-stu-id="1ce35-104">For Windows 10, versions 1507 and 1511, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="1ce35-105">Stringa a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="1ce35-105">Elliptic curve string</span></span> | <span data-ttu-id="1ce35-106">Disponibile in modalità FIPS</span><span class="sxs-lookup"><span data-stu-id="1ce35-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="1ce35-107">NistP256</span><span class="sxs-lookup"><span data-stu-id="1ce35-107">NistP256</span></span> | <span data-ttu-id="1ce35-108">Sì</span><span class="sxs-lookup"><span data-stu-id="1ce35-108">Yes</span></span> |
| <span data-ttu-id="1ce35-109">NistP384</span><span class="sxs-lookup"><span data-stu-id="1ce35-109">NistP384</span></span> | <span data-ttu-id="1ce35-110">Sì</span><span class="sxs-lookup"><span data-stu-id="1ce35-110">Yes</span></span> |


<span data-ttu-id="1ce35-111">Le seguenti curve ellittiche sono supportate dal provider Microsoft Schannel, ma non sono abilitate per impostazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="1ce35-111">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="1ce35-112">Stringa a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="1ce35-112">Elliptic curve string</span></span> | <span data-ttu-id="1ce35-113">Disponibile in modalità FIPS</span><span class="sxs-lookup"><span data-stu-id="1ce35-113">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="1ce35-114">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-114">brainpoolP256r1</span></span> | <span data-ttu-id="1ce35-115">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-115">No</span></span> |
| <span data-ttu-id="1ce35-116">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-116">brainpoolP384r1</span></span> | <span data-ttu-id="1ce35-117">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-117">No</span></span> |
| <span data-ttu-id="1ce35-118">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-118">brainpoolP512r1</span></span> | <span data-ttu-id="1ce35-119">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-119">No</span></span> |
| <span data-ttu-id="1ce35-120">nistP192</span><span class="sxs-lookup"><span data-stu-id="1ce35-120">nistP192</span></span> | <span data-ttu-id="1ce35-121">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-121">No</span></span> |
| <span data-ttu-id="1ce35-122">nistP224</span><span class="sxs-lookup"><span data-stu-id="1ce35-122">nistP224</span></span> | <span data-ttu-id="1ce35-123">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-123">No</span></span> |
| <span data-ttu-id="1ce35-124">nistP521</span><span class="sxs-lookup"><span data-stu-id="1ce35-124">nistP521</span></span> | <span data-ttu-id="1ce35-125">Sì</span><span class="sxs-lookup"><span data-stu-id="1ce35-125">Yes</span></span> |
| <span data-ttu-id="1ce35-126">secP160k1</span><span class="sxs-lookup"><span data-stu-id="1ce35-126">secP160k1</span></span> | <span data-ttu-id="1ce35-127">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-127">No</span></span> |
| <span data-ttu-id="1ce35-128">secP160r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-128">secP160r1</span></span> | <span data-ttu-id="1ce35-129">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-129">No</span></span> |
| <span data-ttu-id="1ce35-130">secP160r2</span><span class="sxs-lookup"><span data-stu-id="1ce35-130">secP160r2</span></span> | <span data-ttu-id="1ce35-131">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-131">No</span></span> |
| <span data-ttu-id="1ce35-132">secP192k1</span><span class="sxs-lookup"><span data-stu-id="1ce35-132">secP192k1</span></span> | <span data-ttu-id="1ce35-133">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-133">No</span></span> |
| <span data-ttu-id="1ce35-134">secP192r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-134">secP192r1</span></span> | <span data-ttu-id="1ce35-135">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-135">No</span></span> |
| <span data-ttu-id="1ce35-136">secP224k1</span><span class="sxs-lookup"><span data-stu-id="1ce35-136">secP224k1</span></span> | <span data-ttu-id="1ce35-137">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-137">No</span></span> |
| <span data-ttu-id="1ce35-138">secP224r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-138">secP224r1</span></span> | <span data-ttu-id="1ce35-139">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-139">No</span></span> |
| <span data-ttu-id="1ce35-140">secP256k1</span><span class="sxs-lookup"><span data-stu-id="1ce35-140">secP256k1</span></span> | <span data-ttu-id="1ce35-141">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-141">No</span></span> |
| <span data-ttu-id="1ce35-142">secP256r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-142">secP256r1</span></span> | <span data-ttu-id="1ce35-143">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-143">No</span></span> |
| <span data-ttu-id="1ce35-144">secP384r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-144">secP384r1</span></span> | <span data-ttu-id="1ce35-145">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-145">No</span></span> |
| <span data-ttu-id="1ce35-146">secP521r1</span><span class="sxs-lookup"><span data-stu-id="1ce35-146">secP521r1</span></span> | <span data-ttu-id="1ce35-147">No</span><span class="sxs-lookup"><span data-stu-id="1ce35-147">No</span></span> |

## <a name="enabling-elliptic-curves"></a><span data-ttu-id="1ce35-148">Abilitazione di curve ellittiche</span><span class="sxs-lookup"><span data-stu-id="1ce35-148">Enabling Elliptic Curves</span></span>

<span data-ttu-id="1ce35-149">Per aggiungere curve ellittiche, distribuire un criterio di gruppo o usare i cmdlet di TLS:</span><span class="sxs-lookup"><span data-stu-id="1ce35-149">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="1ce35-150">Per usare criteri di gruppo, [configurare l'ordine di curva ecc](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) in configurazione Computer > modelli amministrativi > rete > impostazioni di configurazione SSL con l'elenco di priorità per tutte le curve ellittiche che si vuole abilitare.</span><span class="sxs-lookup"><span data-stu-id="1ce35-150">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="1ce35-151">Per usare PowerShell, vedere [cmdlet TLS](/powershell/module/tls) per un elenco completo della sintassi e delle descrizioni dei cmdlet TLS.</span><span class="sxs-lookup"><span data-stu-id="1ce35-151">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="1ce35-152">Prima di Windows 10, le stringhe del pacchetto di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva.</span><span class="sxs-lookup"><span data-stu-id="1ce35-152">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="1ce35-153">Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica, quindi il suffisso della curva ellittica non è obbligatorio e viene sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di utilizzare criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.</span><span class="sxs-lookup"><span data-stu-id="1ce35-153">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="1ce35-154">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1ce35-154">See Also</span></span>

[<span data-ttu-id="1ce35-155">Configurazione dell'ordine delle curve TLS ECC</span><span class="sxs-lookup"><span data-stu-id="1ce35-155">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="1ce35-156">Gestione dell'ordine di TLS</span><span class="sxs-lookup"><span data-stu-id="1ce35-156">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="1ce35-157">Gestione delle curve ECC di Windows con Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="1ce35-157">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="1ce35-158">Cmdlet TLS</span><span class="sxs-lookup"><span data-stu-id="1ce35-158">TLS cmdlets</span></span>](/powershell/module/tls)
