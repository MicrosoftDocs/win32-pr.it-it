---
description: Per la maggior parte delle funzioni dei criteri LSA è necessario un handle per l'oggetto criteri per il sistema in cui eseguire query o modifiche. Per ottenere un handle per un oggetto criteri, chiamare LsaOpenPolicy e specificare il nome del sistema a cui si desidera accedere e il set di autorizzazioni di accesso necessarie.
ms.assetid: 66fdc878-d9c4-421c-b79f-9df08984611c
title: Apertura di un handle di oggetto Criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c187720692db4937b6e1299dd2bb63fac647852
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318230"
---
# <a name="opening-a-policy-object-handle"></a><span data-ttu-id="3a6a1-104">Apertura di un handle di oggetto Criteri</span><span class="sxs-lookup"><span data-stu-id="3a6a1-104">Opening a Policy Object Handle</span></span>

<span data-ttu-id="3a6a1-105">Per la maggior parte delle funzioni dei criteri LSA è necessario un handle per l'oggetto [**criteri**](policy-object.md) per il sistema in cui eseguire query o modifiche.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-105">Most LSA Policy functions require a handle to the [**Policy**](policy-object.md) object for the system to query or modify.</span></span> <span data-ttu-id="3a6a1-106">Per ottenere un handle per un oggetto **criteri** , chiamare [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) e specificare il nome del sistema a cui si desidera accedere e il set di autorizzazioni di accesso necessarie.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-106">To obtain a handle to a **Policy** object, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) and specify the name of the system you want to access and the set of access permissions required.</span></span>

<span data-ttu-id="3a6a1-107">Le autorizzazioni di accesso necessarie per l'applicazione dipendono dalle azioni eseguite.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-107">The access permissions required for your application depend on the actions it performs.</span></span> <span data-ttu-id="3a6a1-108">Per informazioni dettagliate sulle autorizzazioni necessarie per ogni funzione, vedere la descrizione di tale funzione nelle [funzioni dei criteri LSA](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3a6a1-108">For details about the permissions required for each function, see the description of that function in [LSA Policy Functions](management-functions.md).</span></span>

<span data-ttu-id="3a6a1-109">Se la chiamata a [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) ha esito positivo, restituisce un handle all'oggetto [**criteri**](policy-object.md) per il sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-109">If the call to [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy) is successful, it returns a handle to the [**Policy**](policy-object.md) object for the specified system.</span></span> <span data-ttu-id="3a6a1-110">L'applicazione passa quindi questo handle nelle chiamate di funzione dei criteri LSA successive.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-110">Your application then passes this handle in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="3a6a1-111">Quando l'applicazione non necessita più dell'handle, deve chiamare [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) per liberarlo.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-111">When your application no longer needs the handle, it should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) to free it.</span></span>

<span data-ttu-id="3a6a1-112">Nell'esempio seguente viene illustrato come aprire un handle di oggetto [**criteri**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a6a1-112">The following example shows how to open a [**Policy**](policy-object.md) object handle.</span></span>


```C++
#include <windows.h>

#define TARGET_SYSTEM_NAME L"mysystem"

LSA_HANDLE GetPolicyHandle()
{
  LSA_OBJECT_ATTRIBUTES ObjectAttributes;
  WCHAR SystemName[] = TARGET_SYSTEM_NAME;
  USHORT SystemNameLength;
  LSA_UNICODE_STRING lusSystemName;
  NTSTATUS ntsResult;
  LSA_HANDLE lsahPolicyHandle;

  // Object attributes are reserved, so initialize to zeros.
  ZeroMemory(&ObjectAttributes, sizeof(ObjectAttributes));

  //Initialize an LSA_UNICODE_STRING to the server name.
  SystemNameLength = wcslen(SystemName);
  lusSystemName.Buffer = SystemName;
  lusSystemName.Length = SystemNameLength * sizeof(WCHAR);
  lusSystemName.MaximumLength = (SystemNameLength+1) * sizeof(WCHAR);

  // Get a handle to the Policy object.
  ntsResult = LsaOpenPolicy(
        &lusSystemName,    //Name of the target system.
        &ObjectAttributes, //Object attributes.
        POLICY_ALL_ACCESS, //Desired access permissions.
        &lsahPolicyHandle  //Receives the policy handle.
    );

  if (ntsResult != STATUS_SUCCESS)
  {
    // An error occurred. Display it as a win32 error code.
    wprintf(L"OpenPolicy returned %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return NULL;
  } 
  return lsahPolicyHandle;
}
```



<span data-ttu-id="3a6a1-113">Nell'esempio precedente, l'applicazione ha richiesto ai criteri \_ tutti i \_ [*privilegi*](/windows/desktop/SecGloss/p-gly)di accesso.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-113">In the preceding example, the application requested POLICY\_ALL\_ACCESS [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="3a6a1-114">Per informazioni dettagliate sulle autorizzazioni che l'applicazione deve richiedere quando si chiama [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), vedere le descrizioni delle funzioni a cui l'applicazione passerà l'handle dell'oggetto [**criteri**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3a6a1-114">For details about which permissions your application should request when calling [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), see the descriptions of the functions that your application will pass the [**Policy**](policy-object.md) object handle to.</span></span>

<span data-ttu-id="3a6a1-115">Per aprire un handle per l'oggetto [**criteri**](policy-object.md) di un dominio trusted, chiamare [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (per creare una nuova relazione di trust con un dominio) o chiamare [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (per accedere a un dominio trusted esistente).</span><span class="sxs-lookup"><span data-stu-id="3a6a1-115">To open a handle to the [**Policy**](policy-object.md) object of a trusted domain, call [**LsaCreateTrustedDomainEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacreatetrusteddomainex) (to create a new trust relationship with a domain) or call [**LsaOpenTrustedDomainByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaopentrusteddomainbyname) (to access an existing trusted domain).</span></span> <span data-ttu-id="3a6a1-116">Entrambe queste funzioni impostano un puntatore a [**un \_ handle LSA**](lsa-handle.md), che è quindi possibile specificare nelle successive chiamate di funzione dei criteri LSA.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-116">Both of these functions set a pointer to an [**LSA\_HANDLE**](lsa-handle.md), which you can then specify in subsequent LSA Policy function calls.</span></span> <span data-ttu-id="3a6a1-117">Come per [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), l'applicazione deve chiamare [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) quando non necessita più dell'handle per l'oggetto **criterio** del dominio attendibile.</span><span class="sxs-lookup"><span data-stu-id="3a6a1-117">As with [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy), your application should call [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose) when it no longer needs the handle to the trusted domain's **Policy** object.</span></span>

 

 
