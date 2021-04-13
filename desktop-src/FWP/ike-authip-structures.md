---
title: Strutture IKE/AuthIP
description: Strutture IKE/AuthIP
ms.assetid: 3267EA3C-FD1F-4ED1-9794-92551222EFE1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1b5c8f69ec0ac667dee5fc541c84b8e9e66ceb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2020
ms.locfileid: "104398695"
---
# <a name="ikeauthip-structures"></a><span data-ttu-id="1af20-103">Strutture IKE/AuthIP</span><span class="sxs-lookup"><span data-stu-id="1af20-103">IKE/AuthIP Structures</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1af20-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1af20-104">In this section</span></span>

-   [<span data-ttu-id="1af20-105">**\_METHOD0 IKEEXT Authentication \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-105">**IKEEXT\_AUTHENTICATION\_METHOD0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method0)
-   [<span data-ttu-id="1af20-106">**\_METHOD1 IKEEXT Authentication \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-106">**IKEEXT\_AUTHENTICATION\_METHOD1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_authentication_method1)
-   [<span data-ttu-id="1af20-107">**\_METHOD2 IKEEXT Authentication \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-107">**IKEEXT\_AUTHENTICATION\_METHOD2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [<span data-ttu-id="1af20-108">**\_Certificato IKEEXT \_ EKUS0**</span><span class="sxs-lookup"><span data-stu-id="1af20-108">**IKEEXT\_CERT\_EKUS0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [<span data-ttu-id="1af20-109">**\_Certificato IKEEXT \_ NAME0**</span><span class="sxs-lookup"><span data-stu-id="1af20-109">**IKEEXT\_CERT\_NAME0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [<span data-ttu-id="1af20-110">**\_ \_ CONFIG0 radice certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-110">**IKEEXT\_CERT\_ROOT\_CONFIG0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cert_root_config0)
-   [<span data-ttu-id="1af20-111">**\_AUTHENTICATION0 certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-111">**IKEEXT\_CERTIFICATE\_AUTHENTICATION0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication0)
-   [<span data-ttu-id="1af20-112">**\_AUTHENTICATION1 certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-112">**IKEEXT\_CERTIFICATE\_AUTHENTICATION1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_authentication1)
-   [<span data-ttu-id="1af20-113">**\_Accodare certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-113">**IKEEXT\_CERTIFICATE\_AUTHENTICATION2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [<span data-ttu-id="1af20-114">**\_CREDENTIAL0 certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-114">**IKEEXT\_CERTIFICATE\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential0)
-   [<span data-ttu-id="1af20-115">**\_CREDENTIAL1 certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-115">**IKEEXT\_CERTIFICATE\_CREDENTIAL1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_certificate_credential1)
-   [<span data-ttu-id="1af20-116">**\_CRITERIA0 certificato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-116">**IKEEXT\_CERTIFICATE\_CRITERIA0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [<span data-ttu-id="1af20-117">**\_ALGORITHM0 di crittografia IKEEXT \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-117">**IKEEXT\_CIPHER\_ALGORITHM0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cipher_algorithm0)
-   [<span data-ttu-id="1af20-118">**\_STATISTICS0 comuni \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-118">**IKEEXT\_COMMON\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics0)
-   [<span data-ttu-id="1af20-119">**\_STATISTICS1 comuni \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-119">**IKEEXT\_COMMON\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_common_statistics1)
-   [<span data-ttu-id="1af20-120">**\_PAIR0 cookie \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-120">**IKEEXT\_COOKIE\_PAIR0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_cookie_pair0)
-   [<span data-ttu-id="1af20-121">**\_CREDENTIAL0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-121">**IKEEXT\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential0)
-   [<span data-ttu-id="1af20-122">**\_CREDENTIAL1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-122">**IKEEXT\_CREDENTIAL1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential1)
-   [<span data-ttu-id="1af20-123">**\_CREDENTIAL2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-123">**IKEEXT\_CREDENTIAL2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential2)
-   [<span data-ttu-id="1af20-124">**\_CREDENTIALS0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-124">**IKEEXT\_CREDENTIALS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials0)
-   [<span data-ttu-id="1af20-125">**\_CREDENTIALS1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-125">**IKEEXT\_CREDENTIALS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credentials1)
-   [<span data-ttu-id="1af20-126">**\_CREDENTIALS2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-126">**IKEEXT\_CREDENTIALS2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credentials2)
-   [<span data-ttu-id="1af20-127">**\_PAIR0 credenziali \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-127">**IKEEXT\_CREDENTIAL\_PAIR0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair0)
-   [<span data-ttu-id="1af20-128">**\_PAIR1 credenziali \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-128">**IKEEXT\_CREDENTIAL\_PAIR1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_credential_pair1)
-   [<span data-ttu-id="1af20-129">**\_Pair2 credenziali \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-129">**IKEEXT\_CREDENTIAL\_PAIR2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_credential_pair2)
-   [<span data-ttu-id="1af20-130">**IKEEXT \_ EAP \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="1af20-130">**IKEEXT\_EAP\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_eap_authentication0)
-   [<span data-ttu-id="1af20-131">**IKEEXT \_ em \_ POLICY0**</span><span class="sxs-lookup"><span data-stu-id="1af20-131">**IKEEXT\_EM\_POLICY0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy0)
-   [<span data-ttu-id="1af20-132">**IKEEXT \_ em \_ POLICY1**</span><span class="sxs-lookup"><span data-stu-id="1af20-132">**IKEEXT\_EM\_POLICY1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_em_policy1)
-   [<span data-ttu-id="1af20-133">**IKEEXT \_ em \_ POLICY2**</span><span class="sxs-lookup"><span data-stu-id="1af20-133">**IKEEXT\_EM\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [<span data-ttu-id="1af20-134">**\_ALGORITHM0 integrità \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-134">**IKEEXT\_INTEGRITY\_ALGORITHM0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_integrity_algorithm0)
-   [<span data-ttu-id="1af20-135">**\_STATISTICS0 IKEEXT \_ \_ comuni specifici \_ della versione IP \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-135">**IKEEXT\_IP\_VERSION\_SPECIFIC\_COMMON\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics0)
-   [<span data-ttu-id="1af20-136">**\_STATISTICS1 IKEEXT \_ \_ comuni specifici \_ della versione IP \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-136">**IKEEXT\_IP\_VERSION\_SPECIFIC\_COMMON\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_common_statistics1)
-   [<span data-ttu-id="1af20-137">**\_STATISTICS0 del \_ \_ modulo IKEEXT specifico della versione IP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-137">**IKEEXT\_IP\_VERSION\_SPECIFIC\_KEYMODULE\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics0)
-   [<span data-ttu-id="1af20-138">**\_STATISTICS1 del \_ \_ modulo IKEEXT specifico della versione IP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-138">**IKEEXT\_IP\_VERSION\_SPECIFIC\_KEYMODULE\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ip_version_specific_keymodule_statistics1)
-   [<span data-ttu-id="1af20-139">**\_ \_ AUTHENTICATION0 CGA IKEEXT per IPv6 \_**</span><span class="sxs-lookup"><span data-stu-id="1af20-139">**IKEEXT\_IPV6\_CGA\_AUTHENTICATION0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0)
-   [<span data-ttu-id="1af20-140">**\_AUTHENTICATION0 Kerberos \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-140">**IKEEXT\_KERBEROS\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0)
-   [<span data-ttu-id="1af20-141">**\_AUTHENTICATION1 Kerberos \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-141">**IKEEXT\_KERBEROS\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [<span data-ttu-id="1af20-142">**\_STATISTICS0 del modulo \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-142">**IKEEXT\_KEYMODULE\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics0)
-   [<span data-ttu-id="1af20-143">**\_STATISTICS1 del modulo \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-143">**IKEEXT\_KEYMODULE\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_keymodule_statistics1)
-   [<span data-ttu-id="1af20-144">**\_Nome IKEEXT \_ CREDENTIAL0**</span><span class="sxs-lookup"><span data-stu-id="1af20-144">**IKEEXT\_NAME\_CREDENTIAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_name_credential0)
-   [<span data-ttu-id="1af20-145">**IKEEXT \_ NTLM \_ v2 \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="1af20-145">**IKEEXT\_NTLM\_V2\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0)
-   [<span data-ttu-id="1af20-146">**\_POLICY0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-146">**IKEEXT\_POLICY0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy0)
-   [<span data-ttu-id="1af20-147">**\_POLICY1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-147">**IKEEXT\_POLICY1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_policy1)
-   [<span data-ttu-id="1af20-148">**\_POLICY2 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-148">**IKEEXT\_POLICY2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [<span data-ttu-id="1af20-149">**IKEEXT \_ chiave precondivisa \_ \_ AUTHENTICATION0**</span><span class="sxs-lookup"><span data-stu-id="1af20-149">**IKEEXT\_PRESHARED\_KEY\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0)
-   [<span data-ttu-id="1af20-150">**IKEEXT \_ chiave precondivisa \_ \_ AUTHENTICATION1**</span><span class="sxs-lookup"><span data-stu-id="1af20-150">**IKEEXT\_PRESHARED\_KEY\_AUTHENTICATION1**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication1)
-   [<span data-ttu-id="1af20-151">**\_PROPOSAL0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-151">**IKEEXT\_PROPOSAL0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_proposal0)
-   [<span data-ttu-id="1af20-152">**\_AUTHENTICATION0 riservato \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-152">**IKEEXT\_RESERVED\_AUTHENTICATION0**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_reserved_authentication0)
-   [<span data-ttu-id="1af20-153">**IKEEXT \_ sa \_ DETAILS0**</span><span class="sxs-lookup"><span data-stu-id="1af20-153">**IKEEXT\_SA\_DETAILS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details0)
-   [<span data-ttu-id="1af20-154">**IKEEXT \_ sa \_ Dettagli**</span><span class="sxs-lookup"><span data-stu-id="1af20-154">**IKEEXT\_SA\_DETAILS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_details1)
-   [<span data-ttu-id="1af20-155">**IKEEXT \_ sa \_ DETAILS2**</span><span class="sxs-lookup"><span data-stu-id="1af20-155">**IKEEXT\_SA\_DETAILS2**</span></span>](/windows/win32/api/iketypes/ns-iketypes-ikeext_sa_details2)
-   [<span data-ttu-id="1af20-156">**\_ \_ TEMPLATE0 enum IKEEXT \_ sa**</span><span class="sxs-lookup"><span data-stu-id="1af20-156">**IKEEXT\_SA\_ENUM\_TEMPLATE0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_sa_enum_template0)
-   [<span data-ttu-id="1af20-157">**\_STATISTICS0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-157">**IKEEXT\_STATISTICS0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics0)
-   [<span data-ttu-id="1af20-158">**\_STATISTICS1 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-158">**IKEEXT\_STATISTICS1**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_statistics1)
-   [<span data-ttu-id="1af20-159">**\_TRAFFIC0 IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="1af20-159">**IKEEXT\_TRAFFIC0**</span></span>](/windows/desktop/api/Iketypes/ns-iketypes-ikeext_traffic0)

 

 




