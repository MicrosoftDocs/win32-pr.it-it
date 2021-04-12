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
# <a name="displayspecifiers-container"></a>Contenitore DisplaySpecifiers

Gli identificatori di visualizzazione vengono archiviati, in base alle impostazioni locali, nel contenitore DisplaySpecifiers del contenitore di configurazione. Poiché il contenitore di configurazione viene replicato nell'intera foresta, gli identificatori di visualizzazione vengono propagati in tutti i domini di una foresta.

Il contenitore di configurazione archivia il contenitore DisplaySpecifiers, che quindi archivia i contenitori che corrispondono a ciascuna impostazione locale. Questi contenitori di impostazioni locali vengono denominati usando la rappresentazione esadecimale dell'identificatore delle impostazioni locali. Ad esempio, il contenitore delle impostazioni locali US/English è denominato 409, il contenitore delle impostazioni locali per la lingua tedesca è denominato 407 e il contenitore delle impostazioni locali giapponesi è denominato 411. Per ulteriori informazioni e per un elenco di identificatori di lingua possibili, vedere [costanti e stringhe dell'identificatore di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings).

Ogni contenitore delle impostazioni locali Archivia oggetti della classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) .

Per elencare tutti gli identificatori di visualizzazione per le impostazioni locali, enumerare tutti gli oggetti [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) nel contenitore delle impostazioni locali specificato all'interno del contenitore DisplaySpecifiers.

L'esempio di codice seguente contiene una funzione associata al contenitore dell'identificatore di visualizzazione per le impostazioni locali specificate:


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



 

 