---
description: Curve ellittiche abilitate in Windows 10 versione 1607 e successive.
title: Curve di TLS ellittiche in Windows 10 versione 1607 e successive
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232953"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a><span data-ttu-id="50d31-103">Curve di TLS ellittiche in Windows 10 versione 1607 e successive</span><span class="sxs-lookup"><span data-stu-id="50d31-103">TLS Elliptic Curves in Windows 10 version 1607 and later</span></span>

<span data-ttu-id="50d31-104">Per Windows 10, versioni 1607 e successive, le seguenti curve ellittiche sono abilitate e in questo ordine di priorità per impostazione predefinita tramite il provider Microsoft Schannel:</span><span class="sxs-lookup"><span data-stu-id="50d31-104">For Windows 10, versions 1607 and later, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="50d31-105">Stringa a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="50d31-105">Elliptic curve string</span></span> | <span data-ttu-id="50d31-106">Disponibile in modalità FIPS</span><span class="sxs-lookup"><span data-stu-id="50d31-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="50d31-107">curve25519</span><span class="sxs-lookup"><span data-stu-id="50d31-107">curve25519</span></span> | <span data-ttu-id="50d31-108">No</span><span class="sxs-lookup"><span data-stu-id="50d31-108">No</span></span> |
| <span data-ttu-id="50d31-109">NistP256</span><span class="sxs-lookup"><span data-stu-id="50d31-109">NistP256</span></span> | <span data-ttu-id="50d31-110">Sì</span><span class="sxs-lookup"><span data-stu-id="50d31-110">Yes</span></span> |
| <span data-ttu-id="50d31-111">NistP384</span><span class="sxs-lookup"><span data-stu-id="50d31-111">NistP384</span></span> | <span data-ttu-id="50d31-112">Sì</span><span class="sxs-lookup"><span data-stu-id="50d31-112">Yes</span></span> |


<span data-ttu-id="50d31-113">Le seguenti curve ellittiche sono supportate dal provider Microsoft Schannel, ma non sono abilitate per impostazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="50d31-113">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="50d31-114">Stringa a curva ellittica</span><span class="sxs-lookup"><span data-stu-id="50d31-114">Elliptic curve string</span></span> | <span data-ttu-id="50d31-115">Disponibile in modalità FIPS</span><span class="sxs-lookup"><span data-stu-id="50d31-115">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="50d31-116">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="50d31-116">brainpoolP256r1</span></span> | <span data-ttu-id="50d31-117">No</span><span class="sxs-lookup"><span data-stu-id="50d31-117">No</span></span> |
| <span data-ttu-id="50d31-118">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="50d31-118">brainpoolP384r1</span></span> | <span data-ttu-id="50d31-119">No</span><span class="sxs-lookup"><span data-stu-id="50d31-119">No</span></span> |
| <span data-ttu-id="50d31-120">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="50d31-120">brainpoolP512r1</span></span> | <span data-ttu-id="50d31-121">No</span><span class="sxs-lookup"><span data-stu-id="50d31-121">No</span></span> |
| <span data-ttu-id="50d31-122">nistP192</span><span class="sxs-lookup"><span data-stu-id="50d31-122">nistP192</span></span> | <span data-ttu-id="50d31-123">No</span><span class="sxs-lookup"><span data-stu-id="50d31-123">No</span></span> |
| <span data-ttu-id="50d31-124">nistP224</span><span class="sxs-lookup"><span data-stu-id="50d31-124">nistP224</span></span> | <span data-ttu-id="50d31-125">No</span><span class="sxs-lookup"><span data-stu-id="50d31-125">No</span></span> |
| <span data-ttu-id="50d31-126">nistP521</span><span class="sxs-lookup"><span data-stu-id="50d31-126">nistP521</span></span> | <span data-ttu-id="50d31-127">Sì</span><span class="sxs-lookup"><span data-stu-id="50d31-127">Yes</span></span> |
| <span data-ttu-id="50d31-128">secP160k1</span><span class="sxs-lookup"><span data-stu-id="50d31-128">secP160k1</span></span> | <span data-ttu-id="50d31-129">No</span><span class="sxs-lookup"><span data-stu-id="50d31-129">No</span></span> |
| <span data-ttu-id="50d31-130">secP160r1</span><span class="sxs-lookup"><span data-stu-id="50d31-130">secP160r1</span></span> | <span data-ttu-id="50d31-131">No</span><span class="sxs-lookup"><span data-stu-id="50d31-131">No</span></span> |
| <span data-ttu-id="50d31-132">secP160r2</span><span class="sxs-lookup"><span data-stu-id="50d31-132">secP160r2</span></span> | <span data-ttu-id="50d31-133">No</span><span class="sxs-lookup"><span data-stu-id="50d31-133">No</span></span> |
| <span data-ttu-id="50d31-134">secP192k1</span><span class="sxs-lookup"><span data-stu-id="50d31-134">secP192k1</span></span> | <span data-ttu-id="50d31-135">No</span><span class="sxs-lookup"><span data-stu-id="50d31-135">No</span></span> |
| <span data-ttu-id="50d31-136">secP192r1</span><span class="sxs-lookup"><span data-stu-id="50d31-136">secP192r1</span></span> | <span data-ttu-id="50d31-137">No</span><span class="sxs-lookup"><span data-stu-id="50d31-137">No</span></span> |
| <span data-ttu-id="50d31-138">secP224k1</span><span class="sxs-lookup"><span data-stu-id="50d31-138">secP224k1</span></span> | <span data-ttu-id="50d31-139">No</span><span class="sxs-lookup"><span data-stu-id="50d31-139">No</span></span> |
| <span data-ttu-id="50d31-140">secP224r1</span><span class="sxs-lookup"><span data-stu-id="50d31-140">secP224r1</span></span> | <span data-ttu-id="50d31-141">No</span><span class="sxs-lookup"><span data-stu-id="50d31-141">No</span></span> |
| <span data-ttu-id="50d31-142">secP256k1</span><span class="sxs-lookup"><span data-stu-id="50d31-142">secP256k1</span></span> | <span data-ttu-id="50d31-143">No</span><span class="sxs-lookup"><span data-stu-id="50d31-143">No</span></span> |
| <span data-ttu-id="50d31-144">secP256r1</span><span class="sxs-lookup"><span data-stu-id="50d31-144">secP256r1</span></span> | <span data-ttu-id="50d31-145">No</span><span class="sxs-lookup"><span data-stu-id="50d31-145">No</span></span> |
| <span data-ttu-id="50d31-146">secP384r1</span><span class="sxs-lookup"><span data-stu-id="50d31-146">secP384r1</span></span> | <span data-ttu-id="50d31-147">No</span><span class="sxs-lookup"><span data-stu-id="50d31-147">No</span></span> |
| <span data-ttu-id="50d31-148">secP521r1</span><span class="sxs-lookup"><span data-stu-id="50d31-148">secP521r1</span></span> | <span data-ttu-id="50d31-149">No</span><span class="sxs-lookup"><span data-stu-id="50d31-149">No</span></span> |



## <a name="enabling-elliptic-curves"></a><span data-ttu-id="50d31-150">Abilitazione di curve ellittiche</span><span class="sxs-lookup"><span data-stu-id="50d31-150">Enabling Elliptic Curves</span></span>

<span data-ttu-id="50d31-151">Per aggiungere curve ellittiche, distribuire un criterio di gruppo o usare i cmdlet di TLS:</span><span class="sxs-lookup"><span data-stu-id="50d31-151">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="50d31-152">Per usare criteri di gruppo, [configurare l'ordine di curva ecc](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) in configurazione Computer > modelli amministrativi > rete > impostazioni di configurazione SSL con l'elenco di priorità per tutte le curve ellittiche che si vuole abilitare.</span><span class="sxs-lookup"><span data-stu-id="50d31-152">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="50d31-153">Per usare PowerShell, vedere [cmdlet TLS](/powershell/module/tls) per un elenco completo della sintassi e delle descrizioni dei cmdlet TLS.</span><span class="sxs-lookup"><span data-stu-id="50d31-153">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="50d31-154">Prima di Windows 10, le stringhe del pacchetto di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva.</span><span class="sxs-lookup"><span data-stu-id="50d31-154">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="50d31-155">Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica, quindi il suffisso della curva ellittica non è obbligatorio e viene sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di utilizzare criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.</span><span class="sxs-lookup"><span data-stu-id="50d31-155">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="50d31-156">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="50d31-156">See Also</span></span>

[<span data-ttu-id="50d31-157">Configurazione dell'ordine delle curve TLS ECC</span><span class="sxs-lookup"><span data-stu-id="50d31-157">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="50d31-158">Gestione dell'ordine di TLS</span><span class="sxs-lookup"><span data-stu-id="50d31-158">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="50d31-159">Gestione delle curve ECC di Windows con Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="50d31-159">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="50d31-160">Cmdlet TLS</span><span class="sxs-lookup"><span data-stu-id="50d31-160">TLS cmdlets</span></span>](/powershell/module/tls)
