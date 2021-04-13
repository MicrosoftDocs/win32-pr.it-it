---
title: Metodo CreateSelfSignedCertificate della classe Win32_TSGatewayServer
description: Crea un certificato autofirmato e restituisce l'hash del certificato come \ 0034; out \ 0034; parametro.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CreateSelfSignedCertificate
- Metodo CreateSelfSignedCertificate Servizi Desktop remoto, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Servizi Desktop remoto, metodo CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475640"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="bdca8-106">Metodo CreateSelfSignedCertificate della \_ classe TSGatewayServer Win32</span><span class="sxs-lookup"><span data-stu-id="bdca8-106">CreateSelfSignedCertificate method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="bdca8-107">Crea un certificato autofirmato e restituisce l'hash del certificato come parametro "out".</span><span class="sxs-lookup"><span data-stu-id="bdca8-107">Creates a self-signed certificate and returns the certificate hash as an "out" parameter.</span></span> <span data-ttu-id="bdca8-108">Inoltre, aggiunge il testo " \_ \_ \_ certificato autofirmato del gateway di Servizi terminal \_ " alla proprietà di contesto del certificato, in modo che il certificato venga riconosciuto come certificato del Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="bdca8-108">Also, adds the text "TS\_GATEWAY\_SELF\_SIGNED\_CERTIFICATE" to the certificate context property so that the certificate is recognized as a Remote Desktop Gateway (RD Gateway) certificate.</span></span> <span data-ttu-id="bdca8-109">Questo metodo usa un contenitore di chiavi specifico di Gateway Desktop remoto per creare il certificato.</span><span class="sxs-lookup"><span data-stu-id="bdca8-109">This method uses an RD Gateway-specific key container to create the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdca8-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdca8-110">Syntax</span></span>


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="bdca8-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdca8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdca8-112">*SubjectName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdca8-112">*SubjectName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdca8-113">Nome del soggetto del certificato autofirmato.</span><span class="sxs-lookup"><span data-stu-id="bdca8-113">Subject name of the self-signed certificate.</span></span>

</dd> <dt>

<span data-ttu-id="bdca8-114">*Certhash* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bdca8-114">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdca8-115">Hash del certificato.</span><span class="sxs-lookup"><span data-stu-id="bdca8-115">The certificate hash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bdca8-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdca8-116">Remarks</span></span>

<span data-ttu-id="bdca8-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="bdca8-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bdca8-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bdca8-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bdca8-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bdca8-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bdca8-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bdca8-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bdca8-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bdca8-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdca8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdca8-122">Requirements</span></span>



| <span data-ttu-id="bdca8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdca8-123">Requirement</span></span> | <span data-ttu-id="bdca8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bdca8-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdca8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdca8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bdca8-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bdca8-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bdca8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdca8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bdca8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdca8-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bdca8-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bdca8-129">Namespace</span></span><br/>                | <span data-ttu-id="bdca8-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bdca8-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bdca8-131">MOF</span><span class="sxs-lookup"><span data-stu-id="bdca8-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdca8-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bdca8-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bdca8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bdca8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdca8-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdca8-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bdca8-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdca8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdca8-136">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="bdca8-136">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

