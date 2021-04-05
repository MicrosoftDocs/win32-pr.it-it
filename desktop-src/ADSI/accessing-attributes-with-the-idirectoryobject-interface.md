---
title: Accesso agli attributi con l'interfaccia IDirectoryObject
description: L'interfaccia IDirectoryObject fornisce un'applicazione client scritta in C e C++ con accesso diretto agli oggetti del servizio directory.
ms.assetid: 006be48e-222f-4f77-ac91-58830f2b7363
ms.tgt_platform: multiple
keywords:
- Accesso agli attributi con l'interfaccia IDirectoryObject ADSI
- IDirectoryObject ADSI, accesso agli attributi con
- ADSI ADSI, utilizzo di, utilizzo dell'interfaccia IDirectoryObject per l'accesso agli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1da62b6a5cf7e1389276475c46faac6455672790
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955123"
---
# <a name="accessing-attributes-with-the-idirectoryobject-interface"></a><span data-ttu-id="a0524-106">Accesso agli attributi con l'interfaccia IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="a0524-106">Accessing Attributes With the IDirectoryObject Interface</span></span>

<span data-ttu-id="a0524-107">L'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) fornisce un'applicazione client scritta in C e C++ con accesso diretto agli oggetti del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="a0524-107">The [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface provides a client application written in C and C++ with direct access to directory service objects.</span></span> <span data-ttu-id="a0524-108">L'interfaccia consente l'accesso per mezzo di un protocollo di rete diretto, anziché tramite la cache degli attributi ADSI.</span><span class="sxs-lookup"><span data-stu-id="a0524-108">The interface enables access by means of a direct network protocol, rather than through the ADSI attribute cache.</span></span> <span data-ttu-id="a0524-109">Al posto delle proprietà supportate dall'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , **IDirectoryObject** fornisce metodi che supportano un subset critico dei metodi di manutenzione di un oggetto e forniscono l'accesso ai relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="a0524-109">In place of the properties supported by the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface, **IDirectoryObject** provides methods that support a critical subset of an object's maintenance methods and provide access to its attributes.</span></span> <span data-ttu-id="a0524-110">Con **IDirectoryObject**, un client può ottenere o impostare un numero qualsiasi di attributi di oggetto con una chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="a0524-110">With **IDirectoryObject**, a client can get or set any number of object attributes with one method call.</span></span> <span data-ttu-id="a0524-111">A differenza dei metodi di automazione corrispondenti, che vengono in batch, quelli di **IDirectoryObject** vengono eseguiti quando vengono chiamati.</span><span class="sxs-lookup"><span data-stu-id="a0524-111">Unlike the corresponding Automation methods, which are batched, those of **IDirectoryObject** are executed when called.</span></span> <span data-ttu-id="a0524-112">Poiché i metodi su questa interfaccia non richiedono la creazione di un'istanza di un oggetto directory di automazione, il sovraccarico delle prestazioni è ridotto.</span><span class="sxs-lookup"><span data-stu-id="a0524-112">Because methods on this interface do not require creating an instance of an Automation directory object, the performance overhead is small.</span></span>

<span data-ttu-id="a0524-113">I client scritti in linguaggi come C e C++ devono usare i metodi dell'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per ottimizzare le prestazioni e sfruttare le interfacce del servizio directory native.</span><span class="sxs-lookup"><span data-stu-id="a0524-113">Clients written in languages such as C and C++ should use the methods of the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface to optimize performance and take advantage of native directory service interfaces.</span></span> <span data-ttu-id="a0524-114">I client di automazione non possono usare **IDirectoryObject**.</span><span class="sxs-lookup"><span data-stu-id="a0524-114">Automation clients cannot use **IDirectoryObject**.</span></span> <span data-ttu-id="a0524-115">Ma devono usare l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="a0524-115">Instead, they should use the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>

<span data-ttu-id="a0524-116">Il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) recupera gli attributi con valori singoli e multipli.</span><span class="sxs-lookup"><span data-stu-id="a0524-116">The [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method retrieves attributes with both single and multiple values.</span></span> <span data-ttu-id="a0524-117">Questo metodo accetta un elenco di attributi richiesti e restituisce una [**struttura \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) .</span><span class="sxs-lookup"><span data-stu-id="a0524-117">This method takes a list of requested attributes and returns an [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure.</span></span> <span data-ttu-id="a0524-118">ADSI alloca questa struttura; il chiamante deve liberare questa memoria quando non è più necessaria mediante la funzione [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) .</span><span class="sxs-lookup"><span data-stu-id="a0524-118">ADSI allocates this structure; the caller must free this memory when it is no longer required using the [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem) function.</span></span>

<span data-ttu-id="a0524-119">L'ordine dei valori di attributo restituiti non corrisponde necessariamente all'ordine in cui gli attributi sono stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="a0524-119">The order of returned attribute values is not necessarily the same as the order in which the attributes were requested.</span></span> <span data-ttu-id="a0524-120">È pertanto necessario confrontare i nomi di attributo restituiti da ADSI.</span><span class="sxs-lookup"><span data-stu-id="a0524-120">Therefore, it is necessary to compare the attribute names returned from ADSI.</span></span>

> [!Note]  
> <span data-ttu-id="a0524-121">La struttura di [**\_ \_ informazioni attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) non restituisce tutti gli attributi richiesti.</span><span class="sxs-lookup"><span data-stu-id="a0524-121">The [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure does not return all of the attributes requested.</span></span> <span data-ttu-id="a0524-122">Solo gli attributi che contengono valori fanno parte della struttura restituita.</span><span class="sxs-lookup"><span data-stu-id="a0524-122">Only those attributes that contain values are part of the returned structure.</span></span>

 

<span data-ttu-id="a0524-123">Il numero di attributi restituiti è determinato dal parametro *dwNumberAttributes* passato al metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="a0524-123">The number of attributes returned is determined by the *dwNumberAttributes* parameter passed to the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method.</span></span>

<span data-ttu-id="a0524-124">Nell'esempio di codice seguente viene associato a un oggetto e viene utilizzato il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) per recuperare gli attributi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a0524-124">The following code example binds to an object and uses the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) method to retrieve attributes of the object.</span></span>


```C++
HRESULT hr;
IDirectoryObject *pDirObject;

CoInitialize(NULL);

hr = ADsGetObject(
       L"LDAP://CN=Jeff Smith,OU=Users,DC=Fabrikam,DC=com",
       IID_IDirectoryObject, 
       (void**)&pDirObject);

if(SUCCEEDED(hr))
{
  ADS_ATTR_INFO *pAttrInfo = NULL;
  LPWSTR pAttrNames[] = {L"cn", L"title", L"otherTelephone"};
  DWORD dwNumAttr = sizeof(pAttrNames)/sizeof(LPWSTR);
  DWORD dwReturn;

  //////////////////////////////////////////////////
  // Get attribute values requested.
  // Be aware that the order is not necessarily the 
  // same as requested using pAttrNames.
  //////////////////////////////////////////////////
  hr = pDirObject->GetObjectAttributes(pAttrNames, 
                                       dwNumAttr, 
                                       &pAttrInfo, 
                                       &dwReturn);
     
  if(SUCCEEDED(hr))
  {
    for(DWORD idx = 0; idx < dwReturn; idx++)
      {
        if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"cn") == 0)
        {
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Common Name: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, L"title") == 0)
        {
          if(pAttrInfo->dwADsType == ADSTYPE_CASE_IGNORE_STRING)
          {
            wprintf(L"Title: %s\n", 
                    pAttrInfo[idx].pADsValues[0].CaseIgnoreString);
          }
        }
        else if(_wcsicmp(pAttrInfo[idx].pszAttrName, 
                L"otherTelephone") == 0)
        {  
          // Print the multi-valued property, "Other Telephones".
          if(pAttrInfo[idx].dwADsType == ADSTYPE_CASE_IGNORE_STRING)
        {
          wprintf(L"Other Telephones:");
          for(DWORD val = 0; val < pAttrInfo[idx].dwNumValues; val++) 
          {
            wprintf(L"  %s\n", 
                    pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
          }
        }
      }
    }

    FreeADsMem(pAttrInfo);
  }
     
  pDirObject->Release();
}

CoUninitialize();
```



 

 




