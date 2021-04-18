---
description: Elenca i tipi ACE attualmente definiti.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310952"
---
# <a name="ace"></a><span data-ttu-id="829b0-103">ACE</span><span class="sxs-lookup"><span data-stu-id="829b0-103">ACE</span></span>

<span data-ttu-id="829b0-104">Una voce **ACE** è una [*voce di controllo*](/windows/desktop/SecGloss/a-gly) di accesso in un elenco di controllo di [*accesso*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="829b0-104">An **ACE** is an [*access control entry*](/windows/desktop/SecGloss/a-gly) in an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL).</span></span>

<span data-ttu-id="829b0-105">Nella tabella seguente sono elencati i tipi **ACE** attualmente definiti.</span><span class="sxs-lookup"><span data-stu-id="829b0-105">The following table lists the currently defined **ACE** types.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="829b0-106">Tipo ACE</span><span class="sxs-lookup"><span data-stu-id="829b0-106">ACE type</span></span></th>
<th><span data-ttu-id="829b0-107">Struttura</span><span class="sxs-lookup"><span data-stu-id="829b0-107">Structure</span></span></th>
<th><span data-ttu-id="829b0-108">Tipo ACL</span><span class="sxs-lookup"><span data-stu-id="829b0-108">ACL type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-109">Accesso consentito</span><span class="sxs-lookup"><span data-stu-id="829b0-109">Access allowed</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-110"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-111">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-111">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-112">Accesso consentito</span><span class="sxs-lookup"><span data-stu-id="829b0-112">Access allowed</span></span></li>
<li><span data-ttu-id="829b0-113">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-113">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-114"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-115">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-115">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-116">Accesso consentito</span><span class="sxs-lookup"><span data-stu-id="829b0-116">Access allowed</span></span></li>
<li><span data-ttu-id="829b0-117">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-117">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-118"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-119">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-119">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-120">Accesso consentito</span><span class="sxs-lookup"><span data-stu-id="829b0-120">Access allowed</span></span></li>
<li><span data-ttu-id="829b0-121">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-121">Object specific</span></span></li>
<li><span data-ttu-id="829b0-122">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-122">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-123"><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-124">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-124">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-125">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="829b0-125">Access denied</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-126"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-127">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-127">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-128">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="829b0-128">Access denied</span></span></li>
<li><span data-ttu-id="829b0-129">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-129">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-130"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-131">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-131">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-132">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="829b0-132">Access denied</span></span></li>
<li><span data-ttu-id="829b0-133">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-133">Object specific</span></span></li>
<li><span data-ttu-id="829b0-134">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-134">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-135"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-136">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-136">Discretionary</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-137">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="829b0-137">Access denied</span></span></li>
<li><span data-ttu-id="829b0-138">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-138">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-139"><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-140">Discrezionale</span><span class="sxs-lookup"><span data-stu-id="829b0-140">Discretionary</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-141">Allarme di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-141">System alarm</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-142"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-143">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-143">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-144">Allarme di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-144">System alarm</span></span></li>
<li><span data-ttu-id="829b0-145">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-145">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-146"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-147">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-147">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-148">Allarme di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-148">System alarm</span></span></li>
<li><span data-ttu-id="829b0-149">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-149">Object specific</span></span></li>
<li><span data-ttu-id="829b0-150">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-150">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-151"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-152">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-152">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-153">Allarme di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-153">System alarm</span></span></li>
<li><span data-ttu-id="829b0-154">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-154">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-155"><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-156">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-156">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-157">Controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-157">System audit</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-158"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-159">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-159">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-160">Controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-160">System audit</span></span></li>
<li><span data-ttu-id="829b0-161">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-161">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-162"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-163">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-163">System</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="829b0-164">Controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-164">System audit</span></span></li>
<li><span data-ttu-id="829b0-165">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-165">Object specific</span></span></li>
<li><span data-ttu-id="829b0-166">Consente il callback durante il controllo di accesso</span><span class="sxs-lookup"><span data-stu-id="829b0-166">Allows callback during access check</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-167"><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-168">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-168">System</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="829b0-169">Controllo di sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-169">System audit</span></span></li>
<li><span data-ttu-id="829b0-170">Specifico dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="829b0-170">Object specific</span></span></li>
</ul></td>
<td><span data-ttu-id="829b0-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="829b0-171"><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></span></span></td>
<td><span data-ttu-id="829b0-172">Sistema</span><span class="sxs-lookup"><span data-stu-id="829b0-172">System</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="829b0-173">Gli assi di allarme di sistema e di sistema specifici dell'oggetto non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="829b0-173">System-alarm and object-specific system-alarm ACEs are not currently supported.</span></span>

> [!Note]  
> <span data-ttu-id="829b0-174">Ogni voce ACE inizia con una struttura di [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) .</span><span class="sxs-lookup"><span data-stu-id="829b0-174">Each ACE starts with an [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure.</span></span> <span data-ttu-id="829b0-175">Il formato dei dati che seguono l'intestazione varia a seconda del tipo di voce ACE specificato nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="829b0-175">The format of the data following the header varies according to the ACE type specified in the header.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="829b0-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="829b0-176">Requirements</span></span>



| <span data-ttu-id="829b0-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="829b0-177">Requirement</span></span> | <span data-ttu-id="829b0-178">Valore</span><span class="sxs-lookup"><span data-stu-id="829b0-178">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="829b0-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="829b0-179">Minimum supported client</span></span><br/> | <span data-ttu-id="829b0-180">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="829b0-180">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="829b0-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="829b0-181">Minimum supported server</span></span><br/> | <span data-ttu-id="829b0-182">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="829b0-182">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="829b0-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="829b0-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="829b0-184"><dt>Winnt. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="829b0-184"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829b0-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="829b0-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829b0-186">**AddAce**</span><span class="sxs-lookup"><span data-stu-id="829b0-186">**AddAce**</span></span>](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[<span data-ttu-id="829b0-187">**\_ACE consentito per l'accesso \_**</span><span class="sxs-lookup"><span data-stu-id="829b0-187">**ACCESS\_ALLOWED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[<span data-ttu-id="829b0-188">**ACE di accesso \_ negato \_**</span><span class="sxs-lookup"><span data-stu-id="829b0-188">**ACCESS\_DENIED\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[<span data-ttu-id="829b0-189">**ACL**</span><span class="sxs-lookup"><span data-stu-id="829b0-189">**ACL**</span></span>](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[<span data-ttu-id="829b0-190">**\_ACE allarme \_ sistema**</span><span class="sxs-lookup"><span data-stu-id="829b0-190">**SYSTEM\_ALARM\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[<span data-ttu-id="829b0-191">**\_ACE di controllo del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="829b0-191">**SYSTEM\_AUDIT\_ACE**</span></span>](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

