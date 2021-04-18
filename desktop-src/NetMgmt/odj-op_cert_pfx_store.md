---
title: OP_CERT_PFX_STORE
description: Definizione di OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "106300650"
---
# <a name="op_cert_pfx_store-structure"></a><span data-ttu-id="85fad-103">Struttura OP_CERT_PFX_STORE</span><span class="sxs-lookup"><span data-stu-id="85fad-103">OP_CERT_PFX_STORE structure</span></span>

<span data-ttu-id="85fad-104">Contiene una struttura PFX serializzata.</span><span class="sxs-lookup"><span data-stu-id="85fad-104">Contains a serialized PFX structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="85fad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85fad-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a><span data-ttu-id="85fad-106">Members</span><span class="sxs-lookup"><span data-stu-id="85fad-106">Members</span></span>

### <a name="ptemplatename"></a><span data-ttu-id="85fad-107">pTemplateName</span><span class="sxs-lookup"><span data-stu-id="85fad-107">pTemplateName</span></span>

<span data-ttu-id="85fad-108">Deve essere impostato sul nome del modello di certificato utilizzato per creare il certificato.</span><span class="sxs-lookup"><span data-stu-id="85fad-108">Must be set to the name of the certificate template used to create the certificate.</span></span>

### <a name="ulprivatekeyexportpolicy"></a><span data-ttu-id="85fad-109">ulPrivateKeyExportPolicy</span><span class="sxs-lookup"><span data-stu-id="85fad-109">ulPrivateKeyExportPolicy</span></span>

<span data-ttu-id="85fad-110">Contiene un valore dell'enumerazione [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .</span><span class="sxs-lookup"><span data-stu-id="85fad-110">Contains one value from the [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) enumeration.</span></span>

### <a name="ppolicyserverurl"></a><span data-ttu-id="85fad-111">pPolicyServerUrl</span><span class="sxs-lookup"><span data-stu-id="85fad-111">pPolicyServerUrl</span></span>

<span data-ttu-id="85fad-112">È necessario impostare l'URL del server dei criteri.</span><span class="sxs-lookup"><span data-stu-id="85fad-112">Must be set the URL of the policy server.</span></span>

### <a name="ulpolicyserverurlflags"></a><span data-ttu-id="85fad-113">ulPolicyServerUrlFlags</span><span class="sxs-lookup"><span data-stu-id="85fad-113">ulPolicyServerUrlFlags</span></span>

<span data-ttu-id="85fad-114">Contiene un valore dell'enumerazione [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .</span><span class="sxs-lookup"><span data-stu-id="85fad-114">Contains one value from the [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) enumeration.</span></span>

### <a name="ppolicyserverid"></a><span data-ttu-id="85fad-115">pPolicyServerId</span><span class="sxs-lookup"><span data-stu-id="85fad-115">pPolicyServerId</span></span>

<span data-ttu-id="85fad-116">Contiene una stringa che identifica in modo univoco il server dei criteri</span><span class="sxs-lookup"><span data-stu-id="85fad-116">Contains a string that uniquely identifies the policy server</span></span>

### <a name="cbpfx"></a><span data-ttu-id="85fad-117">cbPfx</span><span class="sxs-lookup"><span data-stu-id="85fad-117">cbPfx</span></span>

<span data-ttu-id="85fad-118">Contiene la dimensione di pPfx in byte.</span><span class="sxs-lookup"><span data-stu-id="85fad-118">Contains the size of pPfx in bytes.</span></span>

### <a name="ppfx"></a><span data-ttu-id="85fad-119">pPfx</span><span class="sxs-lookup"><span data-stu-id="85fad-119">pPfx</span></span>

<span data-ttu-id="85fad-120">Contiene una struttura PFX serializzata (vedere [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="85fad-120">Contains a serialized PFX structure (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="85fad-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85fad-121">See also</span></span>

[<span data-ttu-id="85fad-122">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="85fad-122">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
