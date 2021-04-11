---
title: Enumerazione WINBIO_CREDENTIAL_FORMAT ( \_ tipi WINBIO. h)
description: Definisce i flag che possono essere utilizzati per specificare il formato delle credenziali dell'utente finale.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT enumerazione Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119782"
---
# <a name="winbio_credential_format-enumeration"></a><span data-ttu-id="586a6-104">Enumerazione del formato delle \_ credenziali WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="586a6-104">WINBIO\_CREDENTIAL\_FORMAT enumeration</span></span>

<span data-ttu-id="586a6-105">Definisce i flag che possono essere utilizzati per specificare il formato delle credenziali dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="586a6-105">Defines flags that can be used to specify the end-user credential format.</span></span> <span data-ttu-id="586a6-106">Questa enumerazione viene utilizzata dalla funzione [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .</span><span class="sxs-lookup"><span data-stu-id="586a6-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="586a6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="586a6-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="586a6-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="586a6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="586a6-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ password \_ generico**</span><span class="sxs-lookup"><span data-stu-id="586a6-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO\_PASSWORD\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="586a6-110">Il formato della password è generico.</span><span class="sxs-lookup"><span data-stu-id="586a6-110">The password is in a generic format.</span></span>

</dd> <dt>

<span data-ttu-id="586a6-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**\_password \_ compressa WINBIO**</span><span class="sxs-lookup"><span data-stu-id="586a6-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO\_PASSWORD\_PACKED**</span></span>
</dt> <dd>

<span data-ttu-id="586a6-112">La password è in un formato compresso.</span><span class="sxs-lookup"><span data-stu-id="586a6-112">The password is in a compressed format.</span></span>

</dd> <dt>

<span data-ttu-id="586a6-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ password \_ protetta**</span><span class="sxs-lookup"><span data-stu-id="586a6-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO\_PASSWORD\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="586a6-114">La credenziale della password è stata incapsulata con [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span><span class="sxs-lookup"><span data-stu-id="586a6-114">The password credential was wrapped with [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="586a6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="586a6-115">Requirements</span></span>



| <span data-ttu-id="586a6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="586a6-116">Requirement</span></span> | <span data-ttu-id="586a6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="586a6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="586a6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="586a6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="586a6-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="586a6-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="586a6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="586a6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="586a6-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="586a6-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="586a6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="586a6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="586a6-123"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="586a6-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="586a6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="586a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="586a6-125">Enumerazioni delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="586a6-125">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="586a6-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="586a6-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

