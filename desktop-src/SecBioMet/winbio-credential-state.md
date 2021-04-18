---
title: Enumerazione WINBIO_CREDENTIAL_STATE ( \_ tipi WINBIO. h)
description: Definisce i valori che specificano se una credenziale è stata associata ai dati biometrici per un utente finale.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE enumerazione Windows Biometric Framework API
- Puntatore di enumerazione PWINBIO_CREDENTIAL_STATE Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340423"
---
# <a name="winbio_credential_state-enumeration"></a><span data-ttu-id="f461c-105">\_ \_ Enumerazione dello stato delle credenziali WINBIO</span><span class="sxs-lookup"><span data-stu-id="f461c-105">WINBIO\_CREDENTIAL\_STATE enumeration</span></span>

<span data-ttu-id="f461c-106">Definisce i valori che specificano se una credenziale è stata associata ai dati biometrici per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="f461c-106">Defines values that specify whether a credential has been associated with the biometric data for an end user.</span></span> <span data-ttu-id="f461c-107">Questa enumerazione viene utilizzata dalla funzione [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="f461c-107">This enumeration is used by the [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f461c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f461c-108">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a><span data-ttu-id="f461c-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="f461c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f461c-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_credenziali WINBIO \_ non \_ impostate**</span><span class="sxs-lookup"><span data-stu-id="f461c-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**WINBIO\_CREDENTIAL\_NOT\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="f461c-111">Una credenziale è stata associata all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="f461c-111">A credential has been associated with the end user.</span></span>

</dd> <dt>

<span data-ttu-id="f461c-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_set di credenziali WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="f461c-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO\_CREDENTIAL\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="f461c-113">Una credenziale non è stata associata all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="f461c-113">A credential has not been associated with the end user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f461c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f461c-114">Requirements</span></span>



| <span data-ttu-id="f461c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f461c-115">Requirement</span></span> | <span data-ttu-id="f461c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f461c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f461c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f461c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f461c-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f461c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f461c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f461c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f461c-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f461c-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f461c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f461c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f461c-122"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f461c-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f461c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f461c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f461c-124">Enumerazioni delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="f461c-124">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="f461c-125">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="f461c-125">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





