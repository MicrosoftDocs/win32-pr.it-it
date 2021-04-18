---
description: Consente di visualizzare un'interfaccia utente selezionabile che consente di selezionare un nome utente.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'Metodo ISCrdEnr:: selectUserName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316661"
---
# <a name="iscrdenrselectusername-method"></a><span data-ttu-id="8a21e-103">Metodo ISCrdEnr:: selectUserName</span><span class="sxs-lookup"><span data-stu-id="8a21e-103">ISCrdEnr::selectUserName method</span></span>

<span data-ttu-id="8a21e-104">Il metodo **selectUserName** Visualizza un'interfaccia **utente SELECT** , consentendo la selezione di un nome utente.</span><span class="sxs-lookup"><span data-stu-id="8a21e-104">The **selectUserName** method displays a **Select User** interface, allowing a user name to be selected.</span></span>

<span data-ttu-id="8a21e-105">Il nome utente viene applicato all'utente per conto del quale è destinata la registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="8a21e-105">The user name applies to the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a21e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a21e-106">Syntax</span></span>


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a><span data-ttu-id="8a21e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a21e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a21e-108">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-109">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="8a21e-109">Reserved for future use.</span></span> <span data-ttu-id="8a21e-110">Impostare questo valore su zero.</span><span class="sxs-lookup"><span data-stu-id="8a21e-110">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a21e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a21e-111">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="8a21e-112">VB</span><span class="sxs-lookup"><span data-stu-id="8a21e-112">VB</span></span>

<span data-ttu-id="8a21e-113">Se il metodo ha esito positivo, il metodo restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a21e-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="8a21e-114">Se il metodo ha esito negativo, restituisce un valore **HRESULT** che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="8a21e-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="8a21e-115">Per un elenco di codici di errore comuni, vedere [valori HRESULT comuni](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="8a21e-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a21e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a21e-116">Remarks</span></span>

<span data-ttu-id="8a21e-117">Utilizzare questo metodo per selezionare il nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8a21e-117">Use this method to select the name of the user.</span></span> <span data-ttu-id="8a21e-118">Dopo aver selezionato un nome utente, è possibile recuperarne il valore chiamando il metodo [**ISCrdEnr:: GetUserName**](iscrdenr-getusername.md) .</span><span class="sxs-lookup"><span data-stu-id="8a21e-118">After a user name has been selected, its value can be retrieved by calling the [**ISCrdEnr::getUserName**](iscrdenr-getusername.md) method.</span></span>

<span data-ttu-id="8a21e-119">Un'alternativa all'uso dell'interfaccia ' Seleziona utente ' consiste nel specificare un utente chiamando il metodo [**ISCrdEnr:: Seusername**](iscrdenr-setusername.md) .</span><span class="sxs-lookup"><span data-stu-id="8a21e-119">An alternative to using the 'Select User' interface is to specify a user by calling the [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a21e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a21e-120">Requirements</span></span>



| <span data-ttu-id="8a21e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a21e-121">Requirement</span></span> | <span data-ttu-id="8a21e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8a21e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a21e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a21e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8a21e-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8a21e-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="8a21e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a21e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8a21e-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8a21e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8a21e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a21e-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a21e-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a21e-129">IID</span><span class="sxs-lookup"><span data-stu-id="8a21e-129">IID</span></span><br/>                      | <span data-ttu-id="8a21e-130">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="8a21e-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8a21e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a21e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a21e-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="8a21e-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="8a21e-133">**ISCrdEnr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="8a21e-133">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="8a21e-134">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="8a21e-134">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="8a21e-135">**ISCrdEnr:: seusername**</span><span class="sxs-lookup"><span data-stu-id="8a21e-135">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




