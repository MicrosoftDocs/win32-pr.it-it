---
title: Enumerazione WINBIO_CREDENTIAL_TYPE ( \_ tipi WINBIO. h)
description: Definisce i flag che possono essere utilizzati per filtrare il tipo di credenziale.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- WINBIO_CREDENTIAL_TYPE enumerazione Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874549"
---
# <a name="winbio_credential_type-enumeration"></a><span data-ttu-id="67ba0-104">\_Enumerazione del tipo di credenziale WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="67ba0-104">WINBIO\_CREDENTIAL\_TYPE enumeration</span></span>

<span data-ttu-id="67ba0-105">Definisce i flag che possono essere utilizzati per filtrare il tipo di credenziale.</span><span class="sxs-lookup"><span data-stu-id="67ba0-105">Defines flags that can be used to filter on the credential type.</span></span> <span data-ttu-id="67ba0-106">Questa enumerazione viene utilizzata dalle funzioni [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)e [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="67ba0-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential), and [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ba0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67ba0-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a><span data-ttu-id="67ba0-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="67ba0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="67ba0-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**\_password credenziali \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="67ba0-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO\_CREDENTIAL\_PASSWORD**</span></span>
</dt> <dd>

<span data-ttu-id="67ba0-110">Filtra le credenziali della password.</span><span class="sxs-lookup"><span data-stu-id="67ba0-110">Filters password credentials.</span></span>

</dd> <dt>

<span data-ttu-id="67ba0-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO \_ \_ tutte le credenziali**</span><span class="sxs-lookup"><span data-stu-id="67ba0-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO\_CREDENTIAL\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="67ba0-112">Filtra tutte le credenziali.</span><span class="sxs-lookup"><span data-stu-id="67ba0-112">Filters all credentials.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="67ba0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67ba0-113">Requirements</span></span>



| <span data-ttu-id="67ba0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ba0-114">Requirement</span></span> | <span data-ttu-id="67ba0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="67ba0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ba0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67ba0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67ba0-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="67ba0-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="67ba0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67ba0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67ba0-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="67ba0-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="67ba0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67ba0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67ba0-121"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67ba0-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ba0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67ba0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ba0-123">Enumerazioni delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="67ba0-123">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="67ba0-124">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="67ba0-124">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[<span data-ttu-id="67ba0-125">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="67ba0-125">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[<span data-ttu-id="67ba0-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="67ba0-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





