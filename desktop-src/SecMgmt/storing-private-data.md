---
description: I criteri LSA forniscono due funzioni che è possibile utilizzare per impostare e recuperare i dati privati.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Archiviazione di dati privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6281f77e66a4217bda534b34342d6cefd92bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401648"
---
# <a name="storing-private-data"></a><span data-ttu-id="dd13a-103">Archiviazione di dati privati</span><span class="sxs-lookup"><span data-stu-id="dd13a-103">Storing Private Data</span></span>

<span data-ttu-id="dd13a-104">I criteri LSA forniscono due funzioni che è possibile utilizzare per impostare e recuperare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="dd13a-104">LSA Policy provides two functions that you can use to set and retrieve private data.</span></span> <span data-ttu-id="dd13a-105">Questi dati vengono archiviati come stringa crittografata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dd13a-105">This data is stored as an encrypted string in the registry.</span></span> <span data-ttu-id="dd13a-106">Ad esempio, è possibile usare queste funzioni per archiviare le password degli account del server e altre informazioni riservate.</span><span class="sxs-lookup"><span data-stu-id="dd13a-106">For example, you can use these functions to store server account passwords and other sensitive information.</span></span>

<span data-ttu-id="dd13a-107">Chiamare la funzione [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) per archiviare e crittografare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="dd13a-107">Call the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function to store and encrypt private data.</span></span> <span data-ttu-id="dd13a-108">Come descritto in [oggetto dati privato](private-data-object.md), gli oggetti dati privati includono tre tipi specializzati: locale, globale e computer.</span><span class="sxs-lookup"><span data-stu-id="dd13a-108">As described in [Private Data Object](private-data-object.md), private data objects include three specialized types: local, global, and machine.</span></span> <span data-ttu-id="dd13a-109">Per creare un oggetto specializzato, aggiungere un prefisso al nome della chiave passato a **LsaStorePrivateData**: "L $" per gli oggetti locali, "G $" per gli oggetti globali e "M $" per gli oggetti computer.</span><span class="sxs-lookup"><span data-stu-id="dd13a-109">To create a specialized object, add a prefix to the key name passed to **LsaStorePrivateData**: "L$" for local objects, "G$" for global objects, and "M$" for machine objects.</span></span> <span data-ttu-id="dd13a-110">Se non si crea uno di questi tipi specializzati, non è necessario specificare un prefisso per il nome della chiave.</span><span class="sxs-lookup"><span data-stu-id="dd13a-110">If you are not creating one of these specialized types, you do not need to specify a key name prefix.</span></span>

<span data-ttu-id="dd13a-111">Per recuperare e decodificare i dati privati archiviati in precedenza, chiamare [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span><span class="sxs-lookup"><span data-stu-id="dd13a-111">To retrieve and decode previously stored private data, call [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata).</span></span> <span data-ttu-id="dd13a-112">Si noti che non è possibile recuperare oggetti dati privati del computer; è possibile recuperare gli oggetti computer solo dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dd13a-112">Note that you cannot retrieve machine private data objects; machine objects can be retrieved only by the operating system.</span></span>

<span data-ttu-id="dd13a-113">Prima di poter archiviare o recuperare dati privati, l'applicazione deve ottenere un handle per l'oggetto [**criteri**](policy-object.md) locale, come illustrato in [apertura di un handle di oggetto Criteri](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="dd13a-113">Before you can store or retrieve private data, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="dd13a-114">Nell'esempio seguente viene creato un oggetto dati privato locale.</span><span class="sxs-lookup"><span data-stu-id="dd13a-114">The following example creates a local private data object.</span></span> <span data-ttu-id="dd13a-115">Si noti che la funzione InitLsaString converte una stringa [*Unicode*](/windows/desktop/SecGloss/u-gly) in una struttura di [**\_ \_ stringhe Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="dd13a-115">Note that the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="dd13a-116">Il codice per questa funzione è illustrato in [uso di stringhe Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="dd13a-116">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="dd13a-117">I dati archiviati dalla funzione [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) non sono assolutamente protetti.</span><span class="sxs-lookup"><span data-stu-id="dd13a-117">The data stored by the [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) function is not absolutely protected.</span></span> <span data-ttu-id="dd13a-118">La chiave, tuttavia, ha un [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) che consente solo al creatore e agli amministratori di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="dd13a-118">The key, however, has a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) that allows only the creator and administrators to read the data.</span></span>

 

 

 
