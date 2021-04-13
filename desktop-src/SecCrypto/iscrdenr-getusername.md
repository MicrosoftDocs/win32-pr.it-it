---
description: Recupera il nome dell'utente per conto del quale è prevista la registrazione del certificato.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'Metodo ISCrdEnr:: GetUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348506"
---
# <a name="iscrdenrgetusername-method"></a><span data-ttu-id="afc94-103">Metodo ISCrdEnr:: GetUserName</span><span class="sxs-lookup"><span data-stu-id="afc94-103">ISCrdEnr::getUserName method</span></span>

<span data-ttu-id="afc94-104">Il metodo **GetUserName** Recupera il nome dell'utente per conto del quale è prevista la registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="afc94-104">The **getUserName** method retrieves the name of the user on whose behalf the certificate enrollment is intended.</span></span>

<span data-ttu-id="afc94-105">Prima di chiamare questo metodo, è necessario specificare il nome utente in una chiamata a [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md) o [**ISCrdEnr:: seusername**](iscrdenr-setusername.md).</span><span class="sxs-lookup"><span data-stu-id="afc94-105">Before calling this method, you must specify the user name in a call to [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) or [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="afc94-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afc94-106">Syntax</span></span>


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="afc94-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="afc94-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc94-108">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc94-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc94-109">Questo valore deve essere pari a zero (0), il nome UPN per la registrazione è stato spaventato \_ \_ o il \_ \_ \_ \_ nome compatibile con Sam per la registrazione \_ .</span><span class="sxs-lookup"><span data-stu-id="afc94-109">This value must be either zero (0), SCARD\_ENROLL\_UPN\_NAME, or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME.</span></span>

<span data-ttu-id="afc94-110">Se questo valore è SCARed \_ Registra \_ \_ nome UPN, **GetUserName** restituisce il nome dell'entità universale (UPN) dell'utente, ad esempio " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="afc94-110">If this value is SCARD\_ENROLL\_UPN\_NAME, **getUserName** returns the user's Universal Principal Name (UPN), such as "someone@example.com".</span></span>

<span data-ttu-id="afc94-111">Se questo valore viene spaventato \_ , registra \_ il \_ nome compatibile con Sam \_ , il metodo restituisce il nome di gestione Access Manager (Sam) dell'utente nel formato "dominio \\ utente".</span><span class="sxs-lookup"><span data-stu-id="afc94-111">If this value is SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, the method returns the user's security access manager (SAM) name in the format "DOMAIN\\USER".</span></span>

<span data-ttu-id="afc94-112">Se questo valore è zero, il metodo restituisce il nome UPN dell'utente, se esistente.</span><span class="sxs-lookup"><span data-stu-id="afc94-112">If this value is zero, the method returns the user's UPN name if it exists.</span></span> <span data-ttu-id="afc94-113">Se l'utente non dispone di un nome UPN, il metodo restituisce il nome SAM dell'utente.</span><span class="sxs-lookup"><span data-stu-id="afc94-113">If the user does not have a UPN name, the method returns the user's SAM name.</span></span>

</dd> <dt>

<span data-ttu-id="afc94-114">*pbstrUserName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="afc94-114">*pbstrUserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afc94-115">Puntatore a una stringa che restituisce il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="afc94-115">A pointer to a string that returns the name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc94-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afc94-116">Return value</span></span>

### <a name="c"></a><span data-ttu-id="afc94-117">C++</span><span class="sxs-lookup"><span data-stu-id="afc94-117">C++</span></span>

<span data-ttu-id="afc94-118">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="afc94-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="afc94-119">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="afc94-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="afc94-120">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="afc94-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="afc94-121">VB</span><span class="sxs-lookup"><span data-stu-id="afc94-121">VB</span></span>

<span data-ttu-id="afc94-122">Stringa che rappresenta il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="afc94-122">String that represents the name of the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="afc94-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="afc94-123">Remarks</span></span>

<span data-ttu-id="afc94-124">È possibile specificare il nome dell'utente a cui viene rilasciata la [*Smart Card*](../secgloss/s-gly.md) chiamando [**ISCrdEnr:: seusername**](iscrdenr-setusername.md) o [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="afc94-124">You can specify the name of the user to whom the [*smart card*](../secgloss/s-gly.md) is issued by calling either [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) or [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span> <span data-ttu-id="afc94-125">Dopo che è stato specificato un nome utente, è possibile recuperare il relativo valore chiamando **GetUserName**.</span><span class="sxs-lookup"><span data-stu-id="afc94-125">After a user name has been specified, its value can be retrieved by calling **getUserName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc94-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afc94-126">Requirements</span></span>



| <span data-ttu-id="afc94-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc94-127">Requirement</span></span> | <span data-ttu-id="afc94-128">Valore</span><span class="sxs-lookup"><span data-stu-id="afc94-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc94-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afc94-129">Minimum supported client</span></span><br/> | <span data-ttu-id="afc94-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="afc94-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="afc94-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afc94-131">Minimum supported server</span></span><br/> | <span data-ttu-id="afc94-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="afc94-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="afc94-133">DLL</span><span class="sxs-lookup"><span data-stu-id="afc94-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afc94-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afc94-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="afc94-135">IID</span><span class="sxs-lookup"><span data-stu-id="afc94-135">IID</span></span><br/>                      | <span data-ttu-id="afc94-136">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="afc94-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="afc94-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afc94-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc94-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="afc94-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="afc94-139">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="afc94-139">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="afc94-140">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="afc94-140">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="afc94-141">**ISCrdEnr:: seusername**</span><span class="sxs-lookup"><span data-stu-id="afc94-141">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 
