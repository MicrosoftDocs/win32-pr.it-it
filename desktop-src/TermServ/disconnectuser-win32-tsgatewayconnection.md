---
title: Metodo DisconnectUser della classe Win32_TSGatewayConnection (Tsgauthenticationengine. h)
description: Disconnette tutte le connessioni dell'utente specificato dal server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 3c5d66b6-c1f0-4a91-bf93-be886d8e2391
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DisconnectUser
- Metodo DisconnectUser Servizi Desktop remoto, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, metodo DisconnectUser
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.DisconnectUser
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e223a2de36ad6c2a6fcabc446fe88cad27dc5da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742151"
---
# <a name="disconnectuser-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="8d445-106">Metodo DisconnectUser della \_ classe TSGatewayConnection Win32</span><span class="sxs-lookup"><span data-stu-id="8d445-106">DisconnectUser method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="8d445-107">Disconnette tutte le connessioni dell'utente specificato dal server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="8d445-107">Disconnects all connections of the specified user from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d445-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d445-108">Syntax</span></span>


```mof
uint32 DisconnectUser(
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="8d445-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d445-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d445-110">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8d445-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d445-111">Nome utente, nel formato \* domain \* **\\** _username_ , le cui connessioni devono essere disconnesse.</span><span class="sxs-lookup"><span data-stu-id="8d445-111">The user name, in \*Domain\***\\**_UserName_ format, whose connections are to be disconnected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d445-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d445-112">Return value</span></span>

<span data-ttu-id="8d445-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8d445-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8d445-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8d445-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8d445-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8d445-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8d445-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d445-116">Remarks</span></span>

<span data-ttu-id="8d445-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="8d445-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8d445-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8d445-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8d445-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8d445-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8d445-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8d445-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8d445-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8d445-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d445-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d445-122">Requirements</span></span>



| <span data-ttu-id="8d445-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d445-123">Requirement</span></span> | <span data-ttu-id="8d445-124">Valore</span><span class="sxs-lookup"><span data-stu-id="8d445-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d445-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d445-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8d445-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8d445-126">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="8d445-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d445-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8d445-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d445-128">Windows Server 2008</span></span><br/>                                                                       |
| <span data-ttu-id="8d445-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8d445-129">Namespace</span></span><br/>                | <span data-ttu-id="8d445-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8d445-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                             |
| <span data-ttu-id="8d445-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d445-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d445-132"><dt>Tsgauthenticationengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d445-132"><dt>Tsgauthenticationengine.h</dt></span></span> </dl> |
| <span data-ttu-id="8d445-133">MOF</span><span class="sxs-lookup"><span data-stu-id="8d445-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d445-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d445-134"><dt>TSGateway.mof</dt></span></span> </dl>             |
| <span data-ttu-id="8d445-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8d445-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d445-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d445-136"><dt>AagWmi.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="8d445-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d445-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d445-138">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="8d445-138">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 

