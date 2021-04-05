---
title: Come le applicazioni devono usare gli identificatori di visualizzazione
description: Per visualizzare Dominio di Active Directory oggetti servizio, usare gli identificatori di visualizzazione per ottenere i dati di visualizzazione localizzati per gli oggetti classe e attributo.
ms.assetid: 2ba62906-47ae-4aab-8cb1-a5734eae5984
ms.tgt_platform: multiple
keywords:
- Come le applicazioni devono usare gli identificatori di visualizzazione AD
- Visualizza gli identificatori di Active Directory, come le applicazioni devono usare gli identificatori di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f7045b03da282a9c64b216031e3da03a427268
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734818"
---
# <a name="how-applications-should-use-display-specifiers"></a><span data-ttu-id="55885-105">Come le applicazioni devono usare gli identificatori di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="55885-105">How Applications Should Use Display Specifiers</span></span>

<span data-ttu-id="55885-106">Per visualizzare Dominio di Active Directory oggetti servizio, usare gli identificatori di visualizzazione per ottenere i dati di visualizzazione localizzati per gli oggetti classe e attributo.</span><span class="sxs-lookup"><span data-stu-id="55885-106">To display Active Directory Domain Service objects, use display specifiers to obtain localized display data for class and attribute objects.</span></span> <span data-ttu-id="55885-107">In questo modo è possibile utilizzare i nomi visualizzati e le icone localizzati ed evitare la localizzazione non necessaria dei dati visualizzati.</span><span class="sxs-lookup"><span data-stu-id="55885-107">This enables localized display names and icons to be used and avoids unnecessary localization of the display data.</span></span>

## <a name="display-names"></a><span data-ttu-id="55885-108">Nomi visualizzati</span><span class="sxs-lookup"><span data-stu-id="55885-108">Display Names</span></span>

<span data-ttu-id="55885-109">È necessario usare le proprietà **classDisplayName** e **nell'attributeDisplayNames** degli oggetti identificatore di visualizzazione per le impostazioni locali appropriate per ottenere il testo visualizzato per i nomi di classe e di attributo.</span><span class="sxs-lookup"><span data-stu-id="55885-109">The **classDisplayName** and **attributeDisplayNames** properties of the display specifier objects for the appropriate locale should be used to obtain display text for class and attribute names.</span></span> <span data-ttu-id="55885-110">Non usare le proprietà **CN**, **classDisplayName** o **ldapDisplayName** degli oggetti **classSchema** o **attributeSchema** per ottenere le etichette di testo da visualizzare perché tali valori non sono localizzati.</span><span class="sxs-lookup"><span data-stu-id="55885-110">Do not use the **cn**, **classDisplayName** or **ldapDisplayName** properties of the **classSchema** or **attributeSchema** objects to obtain display text labels because these values are not localized.</span></span> <span data-ttu-id="55885-111">Per ulteriori informazioni su come recuperare il testo localizzato per un oggetto classe, vedere il codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="55885-111">For more information about how to retrieve localized text for a class object, see the following sample code.</span></span>

## <a name="icons"></a><span data-ttu-id="55885-112">Icone</span><span class="sxs-lookup"><span data-stu-id="55885-112">Icons</span></span>

<span data-ttu-id="55885-113">Per ottenere l'icona da visualizzare per un oggetto classe, è necessario utilizzare la proprietà **iconPath** degli oggetti identificatore di visualizzazione per le impostazioni locali appropriate.</span><span class="sxs-lookup"><span data-stu-id="55885-113">The **iconPath** property of the display specifier objects for the appropriate locale should be used to obtain the icon to display for a class object.</span></span> <span data-ttu-id="55885-114">Per altre informazioni, vedere [Icone di classe](class-icons.md).</span><span class="sxs-lookup"><span data-stu-id="55885-114">For more information, see [Class Icons](class-icons.md).</span></span> <span data-ttu-id="55885-115">Se per un oggetto classe non viene specificata alcuna icona localizzata, per l'elemento deve essere visualizzata un'icona predefinita.</span><span class="sxs-lookup"><span data-stu-id="55885-115">If no localized icon is specified for a class object, a default icon should be displayed for the item.</span></span>

## <a name="creating-new-objects"></a><span data-ttu-id="55885-116">Creazione di nuovi oggetti</span><span class="sxs-lookup"><span data-stu-id="55885-116">Creating New Objects</span></span>

<span data-ttu-id="55885-117">Quando possibile, utilizzare le procedure guidate di creazione di oggetti appropriate per creare nuovi oggetti.</span><span class="sxs-lookup"><span data-stu-id="55885-117">When possible, use the appropriate object creation wizards to create new objects.</span></span> <span data-ttu-id="55885-118">Per ulteriori informazioni, vedere [richiamo di creazioni guidate dall'applicazione](invoking-creation-wizards-from-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="55885-118">For more information, see [Invoking Creation Wizards from Your Application](invoking-creation-wizards-from-your-application.md).</span></span>


<span data-ttu-id="55885-119">Nell'esempio di codice seguente viene illustrato come ottenere il testo visualizzato per una classe e un attributo di una classe.</span><span class="sxs-lookup"><span data-stu-id="55885-119">The following code example shows how to obtain the display text for a class and an attribute of a class.</span></span>


```C++
#include <atlbase.h>

/**************************************************************************

    GetClassDisplaySpecifierContainer()

**************************************************************************/

HRESULT GetClassDisplaySpecifierContainer(LPWSTR pwszClass, 
                                          LCID locale, 
                                          IADs **ppads)
{
    if((NULL == pwszClass) || (NULL == ppads))
    {
        return E_INVALIDARG;
    }

    *ppads = NULL;
    
    // If no locale is specified, use the default system locale.
    if(0 == locale)
    {
        locale = GetSystemDefaultLCID();
        if(0 == locale)
        {
            return E_FAIL;
        }
    }
 
    // Verify that it is a valid locale.
    if(!IsValidLocale(locale, LCID_SUPPORTED))
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    IADs *padsRoot = NULL;
 
    hr = ADsOpenObject( L"LDAP://rootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&padsRoot);
 
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the DN to the configuration container.
        hr = padsRoot->Get(CComBSTR(L"configurationNamingContext"), &var);
        
        if(SUCCEEDED(hr))
        {
            WCHAR wszPath[MAX_PATH * 2];

            // Build the string to bind to the container for the
            // specified locale in the DisplaySpecifiers container.
            swprintf_s(wszPath, 
                L"LDAP://cn=%s-Display,cn=%x,cn=DisplaySpecifiers,%s", 
                pwszClass, 
                locale, 
                var.bstrVal);

            VariantClear(&var);
            
            // Bind to the container.
            hr = ADsOpenObject( wszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADs,
                                (void**)ppads);
 
        }

        padsRoot->Release();
    }

    return hr;
}

/**************************************************************************

    GetClassDisplayLabel()

**************************************************************************/

HRESULT GetClassDisplayLabel(LPWSTR pwszClass, 
                             LCID locale, 
                             BSTR *pbstrClassLabel)
{
    if((NULL == pwszClass) || (NULL == pbstrClassLabel))
    {
        return E_INVALIDARG;
    }

    *pbstrClassLabel = NULL;
    
    HRESULT hr;
    IADs *padsDispSpec;
    hr = GetClassDisplaySpecifierContainer(pwszClass, locale, &padsDispSpec);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the classDisplayName property value.
        hr = padsDispSpec->Get(CComBSTR(L"classDisplayName"), &var);
        
        if(SUCCEEDED(hr))
        {
            if(VT_BSTR == var.vt)
            {
                // Do not free the BSTR. The caller will handle it.
                *pbstrClassLabel = var.bstrVal;
            }
            else
            {
                VariantClear(&var);
                hr = E_FAIL;
            }
        }
        
        padsDispSpec->Release();
    }

    return hr;
}

/**************************************************************************

    GetAttributeDisplayLabel()

**************************************************************************/

HRESULT GetAttributeDisplayLabel(LPWSTR pwszClass, 
                                 LPWSTR pwszAttribute, 
                                 LCID locale, 
                                 BSTR *pbstrAttributeLabel)
{
    if( (NULL == pwszClass) || 
        (NULL == pwszAttribute) || 
        (NULL == pbstrAttributeLabel))
    {
        return E_INVALIDARG;
    }

    *pbstrAttributeLabel = NULL;
    
    HRESULT hr;
    IADs *padsDispSpec;
    hr = GetClassDisplaySpecifierContainer(pwszClass, locale, &padsDispSpec);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the attributeDisplayNames property values
        hr = padsDispSpec->GetEx(CComBSTR(L"attributeDisplayNames"), &var);
        
        if(SUCCEEDED(hr))
        {
            LONG        lStart, 
                        lEnd,
                        i;
            SAFEARRAY   *psa;
            VARIANT     varItem;

            VariantInit(&varItem);

            psa = V_ARRAY(&var);

            // Get the lower and upper bound.
            hr = SafeArrayGetLBound(psa, 1, &lStart);
            hr = SafeArrayGetUBound(psa, 1, &lEnd);

            /*
            The attributeDisplayNames values take the form 
            "<attribute name>,<display name>". Enumerate the values, looking 
            for the one that begins with the specified attribute name.
            */
            for(i = lStart; i <= lEnd; i++)
            {
                hr = SafeArrayGetElement(psa, &i, &varItem);
                if(SUCCEEDED(hr))
                {
                    WCHAR   wszTemp[MAX_PATH];

                    wcsncpy_s(wszTemp, 
                        V_BSTR(&varItem), 
                        lstrlenW(pwszAttribute) + 1);
                
                    if(0 == lstrcmpiW(pwszAttribute, wszTemp))
                    {
                        LPWSTR  pwszDisplayLabel;

                        /*
                        The proper value was found. Now, parse the value, looking 
                        for the first comma, which delimits the attribute name 
                        from the display name.
                        */
                        for(    pwszDisplayLabel = V_BSTR(&varItem); 
                                *pwszDisplayLabel; 
                                pwszDisplayLabel = CharNextW(pwszDisplayLabel))
                        {
                            if(',' == *pwszDisplayLabel)
                            {
                                /*
                                The delimiter was found. Set the string 
                                pointer to the next character, which is the 
                                first character of the display name.
                                */
                                pwszDisplayLabel = CharNextW(pwszDisplayLabel);
                                break;
                            }
                        }
                        
                        if(*pwszDisplayLabel)
                        {
                            // Copy the display name to the output.
                            *pbstrAttributeLabel = CComBSTR(pwszDisplayLabel).Detach();

                            hr = S_OK;
                        }

                        /*
                        Release the item variant because the break prevents 
                        it from getting released by the VariantClear call below.
                        */
                        VariantClear(&varItem);

                        break;
                    }

                    VariantClear(&varItem);
                }
            }
        }
        
        padsDispSpec->Release();
    }

    return hr;
}

```



 

 




