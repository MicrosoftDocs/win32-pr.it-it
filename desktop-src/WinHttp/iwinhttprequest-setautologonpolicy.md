---
description: Imposta i criteri di accesso automatici correnti.
ms.assetid: bc8e8c9c-574e-4392-b336-2c06947022ee
title: 'Metodo IWinHttpRequest:: SetAutoLogonPolicy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetAutoLogonPolicy
- WinHttpRequest.SetAutoLogonPolicy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: cad8bd0080d10a1395a0a9d275951ff961a60bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316004"
---
# <a name="iwinhttprequestsetautologonpolicy-method"></a><span data-ttu-id="c4f72-103">Metodo IWinHttpRequest:: SetAutoLogonPolicy</span><span class="sxs-lookup"><span data-stu-id="c4f72-103">IWinHttpRequest::SetAutoLogonPolicy method</span></span>

<span data-ttu-id="c4f72-104">Il metodo **SetAutoLogonPolicy** imposta i [criteri di accesso automatici](authentication-in-winhttp.md)correnti.</span><span class="sxs-lookup"><span data-stu-id="c4f72-104">The **SetAutoLogonPolicy** method sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4f72-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4f72-105">Syntax</span></span>


```C++
HRESULT SetAutoLogonPolicy(
  [in] WinHttpRequestAutoLogonPolicy AutoLogonPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="c4f72-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4f72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4f72-107">*AutoLogonPolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4f72-107">*AutoLogonPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4f72-108">Specifica i criteri di accesso automatici correnti.</span><span class="sxs-lookup"><span data-stu-id="c4f72-108">Specifies the current automatic logon policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4f72-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4f72-109">Return value</span></span>

<span data-ttu-id="c4f72-110">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="c4f72-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4f72-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4f72-111">Remarks</span></span>

<span data-ttu-id="c4f72-112">Il criterio predefinito è [**AutoLogonPolicy \_ OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span><span class="sxs-lookup"><span data-stu-id="c4f72-112">The default policy is [**AutoLogonPolicy\_OnlyIfBypassProxy**](winhttprequestautologonpolicy.md).</span></span>

<span data-ttu-id="c4f72-113">Chiamare **SetAutoLogonPolicy** per impostare i criteri di accesso automatici prima di chiamare [**Send**](iwinhttprequest-send.md) per inviare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c4f72-113">Call **SetAutoLogonPolicy** to set the automatic logon policy before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

> [!Note]  
> <span data-ttu-id="c4f72-114">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c4f72-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c4f72-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="c4f72-115">Examples</span></span>

<span data-ttu-id="c4f72-116">Nell'esempio di script seguente viene illustrato come impostare i criteri di accesso automatici in modo da non utilizzare mai NTLM o negoziare automaticamente l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c4f72-116">The following scripting example shows how to set the automatic logon policy to never use NTLM or Negotiate authentication automatically.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Do not automatically send user credentials.
HttpReq.SetAutoLogonPolicy(2);

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="c4f72-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4f72-117">Requirements</span></span>



| <span data-ttu-id="c4f72-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4f72-118">Requirement</span></span> | <span data-ttu-id="c4f72-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c4f72-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4f72-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4f72-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c4f72-121">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c4f72-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c4f72-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4f72-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c4f72-123">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c4f72-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c4f72-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c4f72-124">Redistributable</span></span><br/>          | <span data-ttu-id="c4f72-125">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c4f72-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c4f72-126">IDL</span><span class="sxs-lookup"><span data-stu-id="c4f72-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4f72-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4f72-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="c4f72-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4f72-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4f72-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4f72-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="c4f72-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c4f72-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4f72-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4f72-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c4f72-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4f72-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4f72-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c4f72-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="c4f72-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c4f72-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="c4f72-135">Autenticazione in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c4f72-135">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="c4f72-136">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c4f72-136">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




