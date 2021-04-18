---
description: Dettare l'autorità del pacchetto dell'applicazione.
ms.assetid: 047439EA-789B-41CF-87C2-66CFB3F20908
title: Costanti SID del contenitore di app (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 300b5ed110bbdc88d32efb76b20f5ec0f8454970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315840"
---
# <a name="app-container-sid-constants"></a><span data-ttu-id="d392a-103">Costanti SID del contenitore di app</span><span class="sxs-lookup"><span data-stu-id="d392a-103">App Container SID Constants</span></span>

<span data-ttu-id="d392a-104">Le costanti SID specifiche del contenitore dell'app stabiliscono l'autorità del pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d392a-104">The app container specific SID constants dictate the application package authority.</span></span> <span data-ttu-id="d392a-105">Sebbene uno sviluppatore possa usare queste costanti direttamente, la maggior parte degli sviluppatori non ha la necessità di definire questi SID del contenitore di app.</span><span class="sxs-lookup"><span data-stu-id="d392a-105">While a developer can use these constants directly, most developers do not need to define these app container SIDs.</span></span>

<dl> <span data-ttu-id="d392a-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**Sicurezza \_ \_ \_ Autorità** del pacchetto dell'app ( {0,0,0,0,0,15} ) sicurezza pacchetto dell'app di <span id="SECURITY_APP_PACKAGE_BASE_RID"></span> <span id="security_app_package_base_rid"></span> **\_ \_ \_ base \_ RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span> <span id="security_builtin_app_package_rid_count"></span> **sicurezza \_ Builtin app del pacchetto \_ \_ \_ RID \_** conteggio RID (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span> <span id="security_app_package_rid_count"></span> **sicurezza pacchetto \_ app \_ \_ RID \_ conteggio** (8L) sicurezza <span id="SECURITY_CAPABILITY_BASE_RID"></span> <span id="security_capability_base_rid"></span> **\_ funzionalità \_ base \_ RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span> <span id="security_builtin_capability_rid_count"></span> **sicurezza \_ Builtin \_ capacità \_ RID \_ conteggio** (2L) sicurezza <span id="SECURITY_CAPABILITY_RID_COUNT"></span> <span id="security_capability_rid_count"></span> **\_ funzionalità \_ RID \_ conteggio** (5L) sicurezza builtin pacchetto <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span> <span id="security_builtin_package_any_package"></span> **\_ \_ \_ qualsiasi \_ pacchetto** (0x00000001L)</span><span class="sxs-lookup"><span data-stu-id="d392a-106"><span id="SECURITY_APP_PACKAGE_AUTHORITY"></span><span id="security_app_package_authority"></span>**SECURITY\_APP\_PACKAGE\_AUTHORITY** ({0,0,0,0,0,15}) <span id="SECURITY_APP_PACKAGE_BASE_RID"></span><span id="security_app_package_base_rid"></span>**SECURITY\_APP\_PACKAGE\_BASE\_RID** (0x00000002L) <span id="SECURITY_BUILTIN_APP_PACKAGE_RID_COUNT"></span><span id="security_builtin_app_package_rid_count"></span>**SECURITY\_BUILTIN\_APP\_PACKAGE\_RID\_COUNT** (2L) <span id="SECURITY_APP_PACKAGE_RID_COUNT"></span><span id="security_app_package_rid_count"></span>**SECURITY\_APP\_PACKAGE\_RID\_COUNT** (8L) <span id="SECURITY_CAPABILITY_BASE_RID"></span><span id="security_capability_base_rid"></span>**SECURITY\_CAPABILITY\_BASE\_RID** (0x00000003L) <span id="SECURITY_BUILTIN_CAPABILITY_RID_COUNT"></span><span id="security_builtin_capability_rid_count"></span>**SECURITY\_BUILTIN\_CAPABILITY\_RID\_COUNT** (2L) <span id="SECURITY_CAPABILITY_RID_COUNT"></span><span id="security_capability_rid_count"></span>**SECURITY\_CAPABILITY\_RID\_COUNT** (5L) <span id="SECURITY_BUILTIN_PACKAGE_ANY_PACKAGE"></span><span id="security_builtin_package_any_package"></span>**SECURITY\_BUILTIN\_PACKAGE\_ANY\_PACKAGE** (0x00000001L)</span></span>
</dl>

## <a name="requirements"></a><span data-ttu-id="d392a-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d392a-107">Requirements</span></span>



| <span data-ttu-id="d392a-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d392a-108">Requirement</span></span> | <span data-ttu-id="d392a-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d392a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d392a-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d392a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d392a-111">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d392a-111">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d392a-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d392a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d392a-113">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d392a-113">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d392a-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d392a-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="d392a-115"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="d392a-115"><dt>Winnt.h</dt></span></span> </dl> |



 

 




