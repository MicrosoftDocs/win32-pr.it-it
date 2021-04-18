---
title: Metodo IsLSPreventUpgradeGPEnabled della classe Win32_TSLicenseServer
description: Recupera un valore che indica se \ 0034; Impedisci l'aggiornamento della licenza \ 0034; l'impostazione di criteri di gruppo è abilitata nel server licenze Desktop remoto.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSPreventUpgradeGPEnabled
- Metodo IsLSPreventUpgradeGPEnabled Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301868"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="1e021-106">Metodo IsLSPreventUpgradeGPEnabled della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="1e021-106">IsLSPreventUpgradeGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="1e021-107">Recupera un valore che indica se l'impostazione di criteri di gruppo "Impedisci aggiornamento licenza" è abilitata nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1e021-107">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e021-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e021-108">Syntax</span></span>


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="1e021-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e021-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e021-110">*Abilitato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1e021-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e021-111">Valore booleano che indica se l'impostazione dei criteri "Impedisci aggiornamento licenza" è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1e021-111">Boolean value that indicates whether the "prevent license upgrade" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e021-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e021-112">Return value</span></span>

<span data-ttu-id="1e021-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1e021-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1e021-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1e021-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1e021-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1e021-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1e021-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e021-116">Remarks</span></span>

<span data-ttu-id="1e021-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="1e021-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="1e021-118">Se è abilitata l'impostazione dei criteri "Impedisci aggiornamento licenza", il server licenze emetterà solo una licenza di autorizzazione Servizi Desktop remoto temporanea per il client se non è disponibile una licenza CAL Servizi Desktop remoto appropriata per il server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="1e021-118">If the "prevent license upgrade" policy setting is enabled, the license server will only issue a temporary RDS CAL to the client if an appropriate RDS CAL for the Remote Desktop Session Host (RD Session Host) server is not available.</span></span>

<span data-ttu-id="1e021-119">L'impostazione dei criteri si trova nel nodo seguente di Editor criteri di gruppo locali:</span><span class="sxs-lookup"><span data-stu-id="1e021-119">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="1e021-120">Configurazione computer \\ modelli amministrativi \\ componenti di \\ Servizi Terminal Servizi terminal di Windows \\</span><span class="sxs-lookup"><span data-stu-id="1e021-120">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="1e021-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1e021-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e021-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1e021-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1e021-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1e021-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e021-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1e021-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e021-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e021-125">Requirements</span></span>



| <span data-ttu-id="1e021-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e021-126">Requirement</span></span> | <span data-ttu-id="1e021-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1e021-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e021-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e021-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1e021-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1e021-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1e021-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e021-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1e021-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e021-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="1e021-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e021-132">Namespace</span></span><br/>                | <span data-ttu-id="1e021-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1e021-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1e021-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1e021-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e021-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e021-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e021-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1e021-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e021-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e021-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e021-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e021-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e021-139">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="1e021-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

