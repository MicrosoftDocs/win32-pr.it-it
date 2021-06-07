---
description: Restituisce le credenziali per autenticare un contenitore non aggiunto a un dominio con Active Directory.
title: Metodo ICcgDomainAuthCredentials::GetPasswordCredentials (ccgplugins.h)
ms.topic: reference
ms.date: 10/21/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials.GetPasswordCredentials
api_type:
- COM
api_location:
- ccgplugins.h
ms.openlocfilehash: abd70a109e491773b374ae32787760d265167baa
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387824"
---
# <a name="iccgdomainauthcredentialsgetpasswordcredentials-method"></a><span data-ttu-id="a193f-103">Metodo ICcgDomainAuthCredentials::GetPasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="a193f-103">ICcgDomainAuthCredentials::GetPasswordCredentials method</span></span>

<span data-ttu-id="a193f-104">Restituisce le credenziali per autenticare un contenitore non aggiunto a un dominio con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a193f-104">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a193f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a193f-105">Syntax</span></span>


```C++
HRESULT GetPasswordCredentials(
[in] LPCWSTR pluginInput, 
[out] LPWSTR* domainName, 
[out] LPWSTR* username, 
[out] LPWSTR* password);
);
```



## <a name="parameters"></a><span data-ttu-id="a193f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a193f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a193f-107">*pluginInput* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a193f-107">*pluginInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a193f-108">Stringa di input passata dal runtime del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a193f-108">An input string passed in by the container runtime.</span></span> <span data-ttu-id="a193f-109">L'implementazione client usa la stringa di input fornita per recuperare le credenziali di autenticazione, in genere da un provider di archiviazione sicuro, restituite nei parametri di output.</span><span class="sxs-lookup"><span data-stu-id="a193f-109">The client implementation uses the provided input string to retrieve authentication credentials, typically from a secure storage provider, that are returned in the output parameters.</span></span> <span data-ttu-id="a193f-110">La stringa di input viene fornita all'host Servizi di calcolo (HCS) in un file di specifica delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="a193f-110">The input string is provided to the Host Compute Services (HCS) in a credential specification file.</span></span> <span data-ttu-id="a193f-111">Per altre informazioni, vedere **la sezione** Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a193f-111">For more information, see the **Remarks** section.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a193f-112">*domainName* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a193f-112">*domainName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a193f-113">Nome di dominio per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="a193f-113">The domain name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a193f-114">*nome utente* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a193f-114">*username* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a193f-115">Nome utente per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="a193f-115">The user name for the credentials.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a193f-116">*password* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a193f-116">*password* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a193f-117">Password per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="a193f-117">The password for the credentials.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a193f-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a193f-118">Return value</span></span>

<span data-ttu-id="a193f-119">Il valore restituito è **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a193f-119">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a193f-120">Il valore S \_ OK indica che la chiamata è riuscita.</span><span class="sxs-lookup"><span data-stu-id="a193f-120">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a193f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a193f-121">Remarks</span></span>

<span data-ttu-id="a193f-122">L'API può essere chiamata contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="a193f-122">The API may be called concurrently.</span></span> <span data-ttu-id="a193f-123">Pertanto, lo sviluppatore deve assicurarsi che l'implementazione sia thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a193f-123">Therefore, the developer needs to ensure that their implementation is thread safe.</span></span> <span data-ttu-id="a193f-124">Inoltre, l'oggetto COM verrà attivato out-of-process e deve essere registrato in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="a193f-124">Additionally, the COM object will be activated out-of-proc and it must be registered appropriately.</span></span> 

<span data-ttu-id="a193f-125">L'implementatore deve aggiungere una chiave in "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses" per il CLSID COM.</span><span class="sxs-lookup"><span data-stu-id="a193f-125">The implementer must add a key under “HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\CCG\COMClasses” for their COM CLSID.</span></span> <span data-ttu-id="a193f-126">L'accesso in scrittura a "CCG\COMClasses" è limitato agli account SYSTEM e Administrator.</span><span class="sxs-lookup"><span data-stu-id="a193f-126">Write access to “CCG\COMClasses” is restricted to SYSTEM and Administrator accounts.</span></span> 

<span data-ttu-id="a193f-127">Di seguito è riportato un esempio di file di specifica delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="a193f-127">The following is an example credential specification file.</span></span> <span data-ttu-id="a193f-128">Per informazioni su come fornire questo file a Docker, vedere Eseguire un contenitore con un [account del servizio gestito del gruppo.](/virtualization/windowscontainers/manage-containers/gmsa-run-container)</span><span class="sxs-lookup"><span data-stu-id="a193f-128">For information on supplying this file to Docker, see [Run a container with a gMSA](/virtualization/windowscontainers/manage-containers/gmsa-run-container).</span></span>

```json
{
    "CmsPlugins": [
        "ActiveDirectory"
    ],
    "DomainJoinConfig": {
        "Sid": "S-1-5-21-3700119848-2853083131-2094573802",
        "MachineAccountName": "gmsa1",
        "Guid": "630a7dd3-2d3e-4471-ae91-1d9ea2556cd5",
        "DnsTreeName": "contoso.com",
        "DnsName": "contoso.com",
        "NetBiosName": "CONTOSO"
    },
    "ActiveDirectoryConfig": {
        "GroupManagedServiceAccounts": [
            {
                "Name": "gmsa1",
                "Scope": "contoso.com"
            },
            {
                "Name": "gmsa1",
                "Scope": "CONTOSO"
            }
        ],
        "HostAccountConfig": {
            "PortableCcgVersion": "1",
            "PluginGUID": "{CFCA0441-511D-4B2A-862E-20348A78760B}",
            "PluginInput": "contoso.com:gmsaccg:<password>"
        }
    }
}

```

## <a name="examples"></a><span data-ttu-id="a193f-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="a193f-129">Examples</span></span>

<span data-ttu-id="a193f-130">L'esempio seguente illustra una semplice implementazione **di ICcgDomainAuthCredentials.**</span><span class="sxs-lookup"><span data-stu-id="a193f-130">The following example shows a simple implementation of **ICcgDomainAuthCredentials**.</span></span> <span data-ttu-id="a193f-131">Si noti che, a scopo illustrativo, questo esempio ottiene le credenziali semplicemente analizzando la stringa di input.</span><span class="sxs-lookup"><span data-stu-id="a193f-131">Note that, for illustrative purposes, this sample obtains the credentials by simply parsing the input string.</span></span> <span data-ttu-id="a193f-132">Un'implementazione reale archivia le credenziali in un archivio dati sicuro e usa la stringa di input per individuare le informazioni sulle credenziali.</span><span class="sxs-lookup"><span data-stu-id="a193f-132">A real-world implementation would store the credentials in a secure data store and use the input string to locate the credential information.</span></span> <span data-ttu-id="a193f-133">Inoltre, le implementazioni standard del metodo COM sono state omesse da questo esempio per brevità.</span><span class="sxs-lookup"><span data-stu-id="a193f-133">Also, the standard COM method implementations have been omitted from this sample for brevity.</span></span>


```C++
// UUID generated by the developer
[uuid("cfca0441-511d-4b2a-862e-20348a78760b")] 
class CCGStubPlugin : public RuntimeClass<RuntimeClassFlags<RuntimeClassType::ClassicCom>, ICcgDomainAuthCredentials >
{
   public:
    CCGStubPlugin() {}

    ~CCGStubPlugin() {}

    IFACEMETHODIMP GetPasswordCredentials(
        _In_ LPCWSTR pluginInput,
        _Outptr_ LPWSTR *domainName,
        _Outptr_ LPWSTR *username,
        _Outptr_ LPWSTR *password)
    {
        std::wstring domainParsed, userParsed, passwordParsed; 
        try
        {
            if(domainName == NULL || username == NULL || password == NULL)
            {
                return STG_E_INVALIDPARAMETER;
            }
            *domainName = NULL;
            *username = NULL;
            *password = NULL;
            wstring pluginInputString(pluginInput);
            if (count(pluginInputString.begin(), pluginInputString.end(), ':') < 2)
            {
                return CO_E_NOT_SUPPORTED;
            }
            // Extract creds of this format Domain:Username:Password
            size_t sep1 = pluginInputString.find(L":");
            size_t sep2 = pluginInputString.find(L":", sep1 + 1);
            domainParsed = pluginInputString.substr(0, sep1);
            userParsed = pluginInputString.substr(sep1 + 1, sep2 - sep1 - 1);
            passwordParsed = pluginInputString.substr(sep2 + 1);
        }
        catch (...)
        {
            return EVENT_E_INTERNALERROR;
        }

        auto userCo = wil::make_cotaskmem_string_nothrow(userParsed.c_str());
        auto passwordCo = wil::make_cotaskmem_string_nothrow(passwordParsed.c_str());
        auto domainCo = wil::make_cotaskmem_string_nothrow(domainParsed.c_str());
        if (userCo == nullptr || passwordCo == nullptr || domainCo == nullptr)
        {
            return STG_E_INSUFFICIENTMEMORY;
        }

        *domainName = domainCo.release();
        *username = userCo.release();
        *password = passwordCo.release();
        return S_OK;
    }
};
CoCreatableClass(CCGStubPlugin);

```



## <a name="requirements"></a><span data-ttu-id="a193f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a193f-134">Requirements</span></span>




| <span data-ttu-id="a193f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a193f-135">Requirement</span></span> | <span data-ttu-id="a193f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="a193f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a193f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a193f-137">Minimum supported server</span></span> | <span data-ttu-id="a193f-138">Windows Server, versione 2004</span><span class="sxs-lookup"><span data-stu-id="a193f-138">Windows Server, version 2004</span></span>                                    |
| <span data-ttu-id="a193f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a193f-139">Header</span></span>                   | <span data-ttu-id="a193f-140">ccgplugins.h</span><span class="sxs-lookup"><span data-stu-id="a193f-140">ccgplugins.h</span></span>   |
| <span data-ttu-id="a193f-141">IID</span><span class="sxs-lookup"><span data-stu-id="a193f-141">IID</span></span>                    | <span data-ttu-id="a193f-142">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="a193f-142">6ecda518-2010-4437-8bc3-46e752b7b172</span></span>          |



 

