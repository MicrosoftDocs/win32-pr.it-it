---
description: Recupera le informazioni sul pacchetto di crittografia per un protocollo, un pacchetto di crittografia e un tipo di chiave specificati.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Funzione SslLookupCipherSuiteInfo (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885661"
---
# <a name="ssllookupciphersuiteinfo-function"></a><span data-ttu-id="87382-103">SslLookupCipherSuiteInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="87382-103">SslLookupCipherSuiteInfo function</span></span>

<span data-ttu-id="87382-104">La funzione **SslLookupCipherSuiteInfo** recupera le informazioni sul pacchetto di crittografia per un protocollo specificato, un pacchetto di crittografia e un set di tipi di chiave.</span><span class="sxs-lookup"><span data-stu-id="87382-104">The **SslLookupCipherSuiteInfo** function retrieves the cipher suite information for a specified protocol, cipher suite, and key type set.</span></span>

## <a name="syntax"></a><span data-ttu-id="87382-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87382-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="87382-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87382-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87382-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87382-108">Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="87382-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="87382-109">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87382-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87382-110">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="87382-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="87382-111">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87382-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87382-112">Uno dei valori degli [**identificatori del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="87382-112">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="87382-113">*dwKeyType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87382-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87382-114">Uno dei valori [**identificatori del tipo di chiave del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="87382-114">One of the [**CNG SSL Provider Key Type Identifiers**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="87382-115">*pCipherSuite* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="87382-115">*pCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87382-116">Indirizzo di un buffer che contiene una struttura [**del \_ \_ \_ pacchetto di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) in cui scrivere le informazioni sul pacchetto di crittografia.</span><span class="sxs-lookup"><span data-stu-id="87382-116">The address of a buffer that contains a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure in which to write the cipher suite information.</span></span>

</dd> <dt>

<span data-ttu-id="87382-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87382-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87382-118">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="87382-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87382-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87382-119">Return value</span></span>

<span data-ttu-id="87382-120">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="87382-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="87382-121">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="87382-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="87382-122">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="87382-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="87382-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="87382-123">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="87382-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87382-124">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="87382-125"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="87382-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="87382-126">Handle *hSslProvider* non valido.</span><span class="sxs-lookup"><span data-stu-id="87382-126">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="87382-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87382-127">Requirements</span></span>



| <span data-ttu-id="87382-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="87382-128">Requirement</span></span> | <span data-ttu-id="87382-129">Valore</span><span class="sxs-lookup"><span data-stu-id="87382-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87382-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87382-130">Minimum supported client</span></span><br/> | <span data-ttu-id="87382-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87382-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="87382-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87382-132">Minimum supported server</span></span><br/> | <span data-ttu-id="87382-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87382-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="87382-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87382-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="87382-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="87382-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="87382-136">DLL</span><span class="sxs-lookup"><span data-stu-id="87382-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87382-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87382-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

