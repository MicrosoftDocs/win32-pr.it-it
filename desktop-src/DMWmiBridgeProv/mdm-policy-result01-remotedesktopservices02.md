---
title: Classe MDM_Policy_Result01_RemoteDesktopServices02
description: La \_ \_ classe Result01 RemoteDesktopServices02 dei criteri MDM \_ rappresenta i criteri di Servizi Desktop remoto.
ms.assetid: 015fe30d-2b76-4df5-a81f-65e488db3526
keywords:
- Classe MDM_Policy_Result01_RemoteDesktopServices02
- Classe MDM_Policy_Result01_RemoteDesktopServices02, descritta
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteDesktopServices02
- MDM_Policy_Result01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Result01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0488308a557f1b872de299bda12487287e1081c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963795"
---
# <a name="mdm_policy_result01_remotedesktopservices02-class"></a><span data-ttu-id="17366-105">\_ \_ Classe Result01 RemoteDesktopServices02 di criteri \_ MDM</span><span class="sxs-lookup"><span data-stu-id="17366-105">MDM\_Policy\_Result01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="17366-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="17366-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="17366-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="17366-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="17366-108">La \_ \_ classe Result01 RemoteDesktopServices02 dei criteri MDM \_ rappresenta i criteri di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="17366-108">The MDM\_Policy\_Result01\_RemoteDesktopServices02 class represents the remote desktop services policies.</span></span>

<span data-ttu-id="17366-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="17366-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="17366-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17366-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteDesktopServices02
{
  string InstanceID;
  string ParentID;
  string AllowUsersToConnectRemotely;
  string ClientConnectionEncryptionLevel;
  string DoNotAllowDriveRedirection;
  string DoNotAllowPasswordSaving;
  string PromptForPasswordUponConnection;
  string RequireSecureRPCCommunication;
};
```

## <a name="members"></a><span data-ttu-id="17366-111">Members</span><span class="sxs-lookup"><span data-stu-id="17366-111">Members</span></span>

<span data-ttu-id="17366-112">La **classe \_ \_ Result01 \_ RemoteDesktopServices02 dei criteri MDM** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="17366-112">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="17366-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17366-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17366-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="17366-114">Properties</span></span>

<span data-ttu-id="17366-115">La **classe \_ \_ \_ RemoteDesktopServices02 dei criteri MDM Result01** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="17366-115">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="17366-116">AllowUsersToConnectRemotely</span><span class="sxs-lookup"><span data-stu-id="17366-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="17366-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17366-119">ClientConnectionEncryptionLevel</span><span class="sxs-lookup"><span data-stu-id="17366-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="17366-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17366-122">DoNotAllowDriveRedirection</span><span class="sxs-lookup"><span data-stu-id="17366-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="17366-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17366-125">DoNotAllowPasswordSaving</span><span class="sxs-lookup"><span data-stu-id="17366-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="17366-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="17366-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="17366-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17366-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17366-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17366-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="17366-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="17366-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="17366-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17366-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="17366-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17366-136">PromptForPasswordUponConnection</span><span class="sxs-lookup"><span data-stu-id="17366-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="17366-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="17366-139">RequireSecureRPCCommunication</span><span class="sxs-lookup"><span data-stu-id="17366-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="17366-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="17366-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="17366-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="17366-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17366-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17366-142">Requirements</span></span>



| <span data-ttu-id="17366-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="17366-143">Requirement</span></span> | <span data-ttu-id="17366-144">Valore</span><span class="sxs-lookup"><span data-stu-id="17366-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17366-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17366-145">Minimum supported client</span></span><br/> | <span data-ttu-id="17366-146">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="17366-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17366-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17366-147">Minimum supported server</span></span><br/> | <span data-ttu-id="17366-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="17366-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="17366-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17366-149">Namespace</span></span><br/>                | <span data-ttu-id="17366-150">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="17366-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="17366-151">MOF</span><span class="sxs-lookup"><span data-stu-id="17366-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17366-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17366-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="17366-153">DLL</span><span class="sxs-lookup"><span data-stu-id="17366-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17366-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17366-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

