---
description: Specifica il nome dell'utente per conto del quale è prevista la registrazione del certificato.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'Metodo ISCrdEnr:: seusername'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319355"
---
# <a name="iscrdenrsetusername-method"></a><span data-ttu-id="00689-103">Metodo ISCrdEnr:: seusername</span><span class="sxs-lookup"><span data-stu-id="00689-103">ISCrdEnr::setUserName method</span></span>

<span data-ttu-id="00689-104">Il metodo **Seusername** specifica il nome dell'utente per conto del quale è prevista la registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="00689-104">The **setUserName** method specifies the name of the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="00689-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00689-105">Syntax</span></span>


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="00689-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00689-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00689-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00689-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00689-108">Questo valore deve essere spaventato per la \_ registrazione \_ del \_ nome UPN (definito come 1) o per \_ registrare \_ il \_ nome compatibile con Sam \_ (definito come 2).</span><span class="sxs-lookup"><span data-stu-id="00689-108">This value must be either SCARD\_ENROLL\_UPN\_NAME (defined as 1) or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME (defined as 2).</span></span>

<span data-ttu-id="00689-109">Impostare questo valore su SCARd \_ Registra \_ \_ nome UPN, se il nome specificato in *bstrUserName* è il nome dell'entità universale dell'utente, ad esempio " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="00689-109">Set this value to SCARD\_ENROLL\_UPN\_NAME, if the name specified in *bstrUserName* is the user's Universal Principal Name, such as "someone@example.com".</span></span> <span data-ttu-id="00689-110">Il nome UPN dell'utente deve corrispondere a un nome SAM (Security Access Manager) esistente.</span><span class="sxs-lookup"><span data-stu-id="00689-110">The user's UPN name must correspond to an existing security access manager (SAM) name.</span></span>

<span data-ttu-id="00689-111">Impostare questo valore su SCARed \_ Registra \_ il \_ nome compatibile con Sam \_ , se il nome specificato in *bstrUserName* è il nome Sam dell'utente nel formato "dominio \\ utente".</span><span class="sxs-lookup"><span data-stu-id="00689-111">Set this value to SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, if the name specified in *bstrUserName* is the user's SAM name in the format of "DOMAIN\\USER".</span></span>

</dd> <dt>

<span data-ttu-id="00689-112">*bstrUserName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00689-112">*bstrUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00689-113">Nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="00689-113">Name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00689-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00689-114">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="00689-115">VB</span><span class="sxs-lookup"><span data-stu-id="00689-115">VB</span></span>

<span data-ttu-id="00689-116">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="00689-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="00689-117">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="00689-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="00689-118">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="00689-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00689-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="00689-119">Remarks</span></span>

<span data-ttu-id="00689-120">Chiamare questo metodo per specificare il nome utente da emettere per la [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="00689-120">Call this method to specify the user name to be issued the [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="00689-121">Un'alternativa a **Seusername** è [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="00689-121">An alternative to **setUserName** is [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span>

<span data-ttu-id="00689-122">Dopo che è stato specificato un nome utente, è possibile recuperare il relativo valore chiamando [**GetUserName**](iscrdenr-getusername.md).</span><span class="sxs-lookup"><span data-stu-id="00689-122">After a user name has been specified, its value can be retrieved by calling [**getUserName**](iscrdenr-getusername.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00689-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00689-123">Requirements</span></span>



| <span data-ttu-id="00689-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="00689-124">Requirement</span></span> | <span data-ttu-id="00689-125">Valore</span><span class="sxs-lookup"><span data-stu-id="00689-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00689-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00689-126">Minimum supported client</span></span><br/> | <span data-ttu-id="00689-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="00689-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="00689-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00689-128">Minimum supported server</span></span><br/> | <span data-ttu-id="00689-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00689-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00689-130">DLL</span><span class="sxs-lookup"><span data-stu-id="00689-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00689-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00689-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="00689-132">IID</span><span class="sxs-lookup"><span data-stu-id="00689-132">IID</span></span><br/>                      | <span data-ttu-id="00689-133">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="00689-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="00689-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00689-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00689-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="00689-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="00689-136">**ISCrdEnr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="00689-136">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="00689-137">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="00689-137">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="00689-138">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="00689-138">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> </dl>

 

 
