---
description: Scarica la firma del file CAB, verifica le autorizzazioni associate ai pacchetti e le esegue in base all'autenticazione.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJavaEX (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328567"
---
# <a name="downloadjavaex-function"></a><span data-ttu-id="64cbf-103">DownloadJavaEX (funzione)</span><span class="sxs-lookup"><span data-stu-id="64cbf-103">DownloadJavaEX function</span></span>

<span data-ttu-id="64cbf-104">Scarica la firma del file CAB, verifica le autorizzazioni associate ai pacchetti e le esegue in base all'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="64cbf-104">Downloads the .cab file signature, verifies the permissions associated with the packages, and executes them based on authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="64cbf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64cbf-105">Syntax</span></span>


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a><span data-ttu-id="64cbf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64cbf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64cbf-107">*Riservato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64cbf-107">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cbf-108">Questo parametro è riservato.</span><span class="sxs-lookup"><span data-stu-id="64cbf-108">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="64cbf-109">*pProviderData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64cbf-109">*pProviderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cbf-110">Struttura [**di \_ \_ dati del provider di crittografia**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) che contiene i dati del certificato, ad esempio le autorizzazioni per file e zone.</span><span class="sxs-lookup"><span data-stu-id="64cbf-110">A [**CRYPT\_PROVIDER\_DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) structure that contains certificate data such as file and zone permissions.</span></span>

</dd> <dt>

<span data-ttu-id="64cbf-111">*pJava* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64cbf-111">*pJava* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cbf-112">Struttura [**del \_ \_ provider di criteri Java**](/previous-versions//bb432350(v=vs.85)) che contiene i dati relativi al provider di criteri.</span><span class="sxs-lookup"><span data-stu-id="64cbf-112">A [**JAVA\_POLICY\_PROVIDER**](/previous-versions//bb432350(v=vs.85)) structure that contains data related to the policy provider.</span></span>

</dd> <dt>

<span data-ttu-id="64cbf-113">*pFunctions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64cbf-113">*pFunctions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cbf-114">Struttura [**di \_ \_ funzioni del provider di crittografia**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) contenente un elenco di metodi per verificare gli oggetti certificato, le firme e i criteri finali.</span><span class="sxs-lookup"><span data-stu-id="64cbf-114">A [**CRYPT\_PROVIDER\_FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) structure that contains a list of methods to verify certificate objects, signatures, and final policies.</span></span>

</dd> <dt>

<span data-ttu-id="64cbf-115">*fCertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64cbf-115">*fCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cbf-116">Se è presente un certificato, questo parametro è **true**.</span><span class="sxs-lookup"><span data-stu-id="64cbf-116">If a certificate is present, this parameter is **TRUE**.</span></span> <span data-ttu-id="64cbf-117">In caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="64cbf-117">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="64cbf-118">*pTrust* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64cbf-118">*pTrust* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64cbf-119">Struttura [**di \_ attendibilità Java**](/windows/desktop/api/Capi/ns-capi-java_trust) che contiene informazioni sull'attendibilità, ad esempio autorizzazione codificata, firma del codificatore e codice dei criteri di restituzione autentico.</span><span class="sxs-lookup"><span data-stu-id="64cbf-119">A [**JAVA\_TRUST**](/windows/desktop/api/Capi/ns-capi-java_trust) structure that contains trust information such as encoded permission, encoder signature, and authentic return policy code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64cbf-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64cbf-120">Return value</span></span>

<span data-ttu-id="64cbf-121">Se la funzione ha esito positivo, il valore restituito è **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="64cbf-121">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="64cbf-122">In caso contrario, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="64cbf-122">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="64cbf-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="64cbf-123">Remarks</span></span>

<span data-ttu-id="64cbf-124">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="64cbf-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="64cbf-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64cbf-125">Requirements</span></span>



| <span data-ttu-id="64cbf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="64cbf-126">Requirement</span></span> | <span data-ttu-id="64cbf-127">Valore</span><span class="sxs-lookup"><span data-stu-id="64cbf-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64cbf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="64cbf-128">DLL</span></span><br/> | <dl> <span data-ttu-id="64cbf-129"><dt>Javacypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64cbf-129"><dt>Javacypt.dll</dt></span></span> </dl> |



 

 
