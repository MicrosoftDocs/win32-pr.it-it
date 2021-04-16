---
description: Seleziona un certificato client da inviare a un server Secure Hypertext Transfer Protocol (HTTPS).
ms.assetid: e76f1e76-5efe-46f2-9a21-064aa06fb3a8
title: 'Metodo IWinHttpRequest:: SetClientCertificate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetClientCertificate
- WinHttpRequest.SetClientCertificate
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0b346451e87b62116d7202b476e554c84604ea48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347206"
---
# <a name="iwinhttprequestsetclientcertificate-method"></a><span data-ttu-id="c50ad-103">Metodo IWinHttpRequest:: SetClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c50ad-103">IWinHttpRequest::SetClientCertificate method</span></span>

<span data-ttu-id="c50ad-104">Il metodo **SetClientCertificate** seleziona un certificato client da inviare a un server Secure HYPERTEXT Transfer Protocol (HTTPS).</span><span class="sxs-lookup"><span data-stu-id="c50ad-104">The **SetClientCertificate** method selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c50ad-105">Syntax</span></span>


```C++
HRESULT SetClientCertificate(
  [in] BSTR ClientCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="c50ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c50ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50ad-107">*ClientCertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c50ad-107">*ClientCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c50ad-108">Specifica il percorso, l' [*archivio certificati*](glossary.md)e l'oggetto di un certificato client.</span><span class="sxs-lookup"><span data-stu-id="c50ad-108">Specifies the location, [*certificate store*](glossary.md), and subject of a client certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50ad-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c50ad-109">Return value</span></span>

<span data-ttu-id="c50ad-110">Il valore restituito è **\_ OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="c50ad-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c50ad-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c50ad-111">Remarks</span></span>

<span data-ttu-id="c50ad-112">La stringa specificata nel parametro *ClientCertificate* è costituita dal percorso del certificato, dall'archivio certificati e dal nome soggetto delimitati da barre rovesciate.</span><span class="sxs-lookup"><span data-stu-id="c50ad-112">The string specified in the *ClientCertificate* parameter consists of the certificate location, certificate store, and subject name delimited by backslashes.</span></span> <span data-ttu-id="c50ad-113">Per ulteriori informazioni sui componenti della stringa del certificato, vedere [Client Certificates](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="c50ad-113">For more information about the components of the certificate string, see [Client Certificates](ssl-in-winhttp.md).</span></span>

<span data-ttu-id="c50ad-114">Il nome e il percorso dell'archivio certificati sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="c50ad-114">The certificate store name and location are optional.</span></span> <span data-ttu-id="c50ad-115">Tuttavia, se si specifica un archivio certificati, è necessario specificare anche il percorso dell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="c50ad-115">However, if you specify a certificate store, you must also specify the location of that certificate store.</span></span> <span data-ttu-id="c50ad-116">Il percorso predefinito è l' \_ utente corrente e l'archivio certificati predefinito è "My".</span><span class="sxs-lookup"><span data-stu-id="c50ad-116">The default location is CURRENT\_USER and the default certificate store is "MY".</span></span> <span data-ttu-id="c50ad-117">Un oggetto vuoto indica che deve essere utilizzato il primo certificato nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="c50ad-117">A blank subject indicates that the first certificate in the certificate store should be used.</span></span>

<span data-ttu-id="c50ad-118">Chiamare **SetClientCertificate** per selezionare un certificato prima di chiamare [**Send**](iwinhttprequest-send.md) per inviare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c50ad-118">Call **SetClientCertificate** to select a certificate before calling [**Send**](iwinhttprequest-send.md) to send the request.</span></span>

<span data-ttu-id="c50ad-119">I servizi HTTP di Microsoft Windows (WinHTTP) non forniscono certificati client per i server proxy che richiedono certificati per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="c50ad-119">Microsoft Windows HTTP Services (WinHTTP) does not provide client certificates to proxy servers that request certificates for authentication.</span></span>

> [!Note]  
> <span data-ttu-id="c50ad-120">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c50ad-120">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c50ad-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="c50ad-121">Examples</span></span>

<span data-ttu-id="c50ad-122">Nell'esempio di script seguente viene illustrato come selezionare un certificato client da inviare con una richiesta.</span><span class="sxs-lookup"><span data-stu-id="c50ad-122">The following scripting example shows how to select a client certificate to send with a request.</span></span> <span data-ttu-id="c50ad-123">Un certificato con l'oggetto "My Middle-Tier certificate" viene scelto dall'archivio certificati "personali" nel registro di sistema in **HKEY \_ Local \_ computer**.</span><span class="sxs-lookup"><span data-stu-id="c50ad-123">A certificate with the subject "My Middle-Tier Certificate" is chosen from the "Personal" certificate store in the registry under **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="c50ad-124">Poiché questo esempio di codice è specifico di Microsoft JScript, che usa la barra rovesciata come carattere di escape, sono necessarie due barre rovesciate adiacenti per delimitare i componenti della stringa del certificato.</span><span class="sxs-lookup"><span data-stu-id="c50ad-124">Because this code example is specific to Microsoft JScript, which uses the backslash as an escape character, two adjacent backslashes are required to delimit components of the certificate string.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var HttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
    
// Open an HTTP connection.
HttpReq.Open("GET", "https://www.fabrikam.com/", false);
    
// Select a client certificate.
HttpReq.SetClientCertificate(
            "LOCAL_MACHINE\\Personal\\My Middle-Tier Certificate");

// Send the HTTP Request.
HttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="c50ad-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c50ad-125">Requirements</span></span>



| <span data-ttu-id="c50ad-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c50ad-126">Requirement</span></span> | <span data-ttu-id="c50ad-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c50ad-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c50ad-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c50ad-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c50ad-129">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c50ad-129">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c50ad-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c50ad-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c50ad-131">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="c50ad-131">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c50ad-132">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c50ad-132">Redistributable</span></span><br/>          | <span data-ttu-id="c50ad-133">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c50ad-133">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c50ad-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c50ad-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c50ad-135"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c50ad-135"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="c50ad-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="c50ad-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="c50ad-137"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c50ad-137"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="c50ad-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c50ad-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c50ad-139"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50ad-139"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c50ad-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c50ad-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50ad-141">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c50ad-141">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="c50ad-142">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c50ad-142">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="c50ad-143">SSL in WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c50ad-143">SSL in WinHTTP</span></span>](ssl-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="c50ad-144">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c50ad-144">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




