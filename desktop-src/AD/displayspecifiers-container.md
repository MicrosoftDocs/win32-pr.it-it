---
title: Contenitore DisplaySpecifiers
description: Gli identificatori di visualizzazione vengono archiviati, in base alle impostazioni locali, nel contenitore DisplaySpecifiers del contenitore di configurazione. Poiché il contenitore di configurazione viene replicato nell'intera foresta, gli identificatori di visualizzazione vengono propagati in tutti i domini di una foresta.
ms.assetid: d7647c50-f95c-41ef-8d67-dc72542cae5a
ms.tgt_platform: multiple
keywords:
- Contenitore DisplaySpecifiers
- Contenitori, identificatori di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406258a6c9983581491420a49621e3d10df4601e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472587"
---
# <a name="displayspecifiers-container"></a><span data-ttu-id="2b78c-106">Contenitore DisplaySpecifiers</span><span class="sxs-lookup"><span data-stu-id="2b78c-106">DisplaySpecifiers Container</span></span>

<span data-ttu-id="2b78c-107">Gli identificatori di visualizzazione vengono archiviati, in base alle impostazioni locali, nel contenitore DisplaySpecifiers del contenitore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="2b78c-107">Display specifiers are stored, by locale, in the DisplaySpecifiers container of the Configuration container.</span></span> <span data-ttu-id="2b78c-108">Poiché il contenitore di configurazione viene replicato nell'intera foresta, gli identificatori di visualizzazione vengono propagati in tutti i domini di una foresta.</span><span class="sxs-lookup"><span data-stu-id="2b78c-108">Because the Configuration container is replicated across the entire forest, display specifiers are propagated across all domains in a forest.</span></span>

<span data-ttu-id="2b78c-109">Il contenitore di configurazione archivia il contenitore DisplaySpecifiers, che quindi archivia i contenitori che corrispondono a ciascuna impostazione locale.</span><span class="sxs-lookup"><span data-stu-id="2b78c-109">The Configuration container stores the DisplaySpecifiers container, which then stores containers that correspond to each locale.</span></span> <span data-ttu-id="2b78c-110">Questi contenitori di impostazioni locali vengono denominati usando la rappresentazione esadecimale dell'identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="2b78c-110">These locale containers are named using the hexadecimal representation of the locale identifier.</span></span> <span data-ttu-id="2b78c-111">Ad esempio, il contenitore delle impostazioni locali US/English è denominato 409, il contenitore delle impostazioni locali per la lingua tedesca è denominato 407 e il contenitore delle impostazioni locali giapponesi è denominato 411.</span><span class="sxs-lookup"><span data-stu-id="2b78c-111">For example, the US/English locale container is named 409, the German locale's container is named 407, and the Japanese locale's container is named 411.</span></span> <span data-ttu-id="2b78c-112">Per ulteriori informazioni e per un elenco di identificatori di lingua possibili, vedere [costanti e stringhe dell'identificatore di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="2b78c-112">For more information, and a list of possible language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

<span data-ttu-id="2b78c-113">Ogni contenitore delle impostazioni locali Archivia oggetti della classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) .</span><span class="sxs-lookup"><span data-stu-id="2b78c-113">Each locale container stores objects of the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) class.</span></span>

<span data-ttu-id="2b78c-114">Per elencare tutti gli identificatori di visualizzazione per le impostazioni locali, enumerare tutti gli oggetti [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) nel contenitore delle impostazioni locali specificato all'interno del contenitore DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="2b78c-114">To list all display specifiers for a locale, enumerate all the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) objects in the specified locale container within the DisplaySpecifiers container.</span></span>

<span data-ttu-id="2b78c-115">L'esempio di codice seguente contiene una funzione associata al contenitore dell'identificatore di visualizzazione per le impostazioni locali specificate:</span><span class="sxs-lookup"><span data-stu-id="2b78c-115">The following code example contains a function that binds to the display specifier container for the specified locale:</span></span>


```C++
/**********
This function returns a pointer to the display specifier container 
for the specified locale.

If locale is NULL, use default system locale and then return the 
locale in the locale parameter.
***********/
HRESULT BindToDisplaySpecifiersContainerByLocale(
    LCID *locale,
    IADs **ppDispSpecCont)
{
HRESULT hr = E_FAIL;
 
if ((!ppDispSpecCont)||(!locale))
    return E_POINTER;
 
// If no locale is specified, use the default system locale.
if (!(*locale))
{
    *locale = GetSystemDefaultLCID();
    if (!(*locale))
        return E_FAIL;
}
 
// Be sure that the locale is valid.
if (!IsValidLocale(*locale, LCID_SUPPORTED))
    return E_INVALIDARG;
 
LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
IADs *pObj = NULL;
VARIANT var;
 
hr = ADsOpenObject(L"LDAP://rootDSE",
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)&pObj);
 
if (SUCCEEDED(hr))
{
    // Get the DN to the configuration container.
    hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
    if (SUCCEEDED(hr))
    {
        // Build the string to bind to the container for the
        // specified locale in the DisplaySpecifiers container.
        swprintf_s(
            szPath, 
            L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", 
            *locale, 
            var.bstrVal);

        // Bind to the container.
        *ppDispSpecCont = NULL;
        hr = ADsOpenObject(szPath,
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)ppDispSpecCont);
 
        if(FAILED(hr))
        {
            if ((*ppDispSpecCont))
            {
                (*ppDispSpecCont)->Release();
                (*ppDispSpecCont) = NULL;
            }
        }
    }
}
 
// Cleanup.
VariantClear(&var);
if (pObj)
    pObj->Release();
 
return hr;
}
```



 

 