---
description: 'Recupera il nome del certificato risultante da una chiamata precedente riuscita a ISCrdEnr:: registra.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'Metodo ISCrdEnr:: getEnrolledCertificateName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316147"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a><span data-ttu-id="341a9-103">Metodo ISCrdEnr:: getEnrolledCertificateName</span><span class="sxs-lookup"><span data-stu-id="341a9-103">ISCrdEnr::getEnrolledCertificateName method</span></span>

<span data-ttu-id="341a9-104">Il metodo **getEnrolledCertificateName** Recupera il nome del certificato risultante da una chiamata precedente riuscita a [**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="341a9-104">The **getEnrolledCertificateName** method retrieves the name of the certificate resulting from an earlier successful call to [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span></span>

<span data-ttu-id="341a9-105">Questo metodo può essere utilizzato anche per visualizzare il certificato in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="341a9-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="341a9-106">Questo metodo chiama la [](../secgloss/c-gly.md) funzione CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="341a9-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="341a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="341a9-107">Syntax</span></span>


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="341a9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="341a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="341a9-109">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="341a9-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="341a9-110">Valore che determina se il certificato viene visualizzato in una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="341a9-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="341a9-111">Se questo valore viene spaventato \_ \_ \_ , nessun \_ certificato di visualizzazione (definito come 0x01), il certificato registrato non viene visualizzato. eventuali altri valori determinano la visualizzazione del certificato registrato nella finestra di dialogo **certificato** .</span><span class="sxs-lookup"><span data-stu-id="341a9-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the enrolled certificate is not displayed; any other values cause the enrolled certificate to be displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="341a9-112">*pBstrCertName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="341a9-112">*pBstrCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="341a9-113">Puntatore a una stringa che restituisce il nome del certificato recuperato.</span><span class="sxs-lookup"><span data-stu-id="341a9-113">A pointer to a string that returns the retrieved certificate name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="341a9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="341a9-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="341a9-115">C++</span><span class="sxs-lookup"><span data-stu-id="341a9-115">C++</span></span>

<span data-ttu-id="341a9-116">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="341a9-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="341a9-117">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="341a9-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="341a9-118">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="341a9-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="341a9-119">VB</span><span class="sxs-lookup"><span data-stu-id="341a9-119">VB</span></span>

<span data-ttu-id="341a9-120">Stringa che rappresenta il nome del certificato recuperato.</span><span class="sxs-lookup"><span data-stu-id="341a9-120">A string that represents the retrieved certificate name.</span></span>

## <a name="remarks"></a><span data-ttu-id="341a9-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="341a9-121">Remarks</span></span>

<span data-ttu-id="341a9-122">Poiché questo metodo agisce su un certificato esistente, è necessario avere chiamato correttamente [**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) prima di poter chiamare **getEnrolledCertificateName**.</span><span class="sxs-lookup"><span data-stu-id="341a9-122">Because this method operates on an existing certificate, you must have successfully called [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) before you can call **getEnrolledCertificateName**.</span></span>

<span data-ttu-id="341a9-123">Il metodo **getEnrolledCertificateName** chiama la funzione [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) per recuperare il nome del certificato in base alla sequenza descritta per il nome del certificato \_ \_ \_ \_ del tipo di visualizzazione semplice del parametro *dwType* di **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="341a9-123">The **getEnrolledCertificateName** method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the certificate name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="341a9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="341a9-124">Requirements</span></span>



| <span data-ttu-id="341a9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="341a9-125">Requirement</span></span> | <span data-ttu-id="341a9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="341a9-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="341a9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="341a9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="341a9-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="341a9-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="341a9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="341a9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="341a9-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="341a9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="341a9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="341a9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="341a9-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="341a9-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="341a9-133">IID</span><span class="sxs-lookup"><span data-stu-id="341a9-133">IID</span></span><br/>                      | <span data-ttu-id="341a9-134">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="341a9-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="341a9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="341a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="341a9-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="341a9-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="341a9-137">[**ISCrdEnr:: registra**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="341a9-137">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
