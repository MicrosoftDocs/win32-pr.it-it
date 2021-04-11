---
title: Lettura di oggetti attributeSchema e classSchema
description: In questo argomento vengono forniti esempi di codice e linee guida per la lettura diretta dagli oggetti attributeSchema e classSchema nel contenitore dello schema.
ms.assetid: a60558e1-88a1-493c-9340-a90143b11f60
ms.tgt_platform: multiple
keywords:
- Lettura di oggetti attributeSchema e classSchema AD
- oggetti AD, lettura degli oggetti attributeSchema e classSchema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910d387809f7be8af22d494974021e5e6a47d0ab
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117543"
---
# <a name="reading-attributeschema-and-classschema-objects"></a><span data-ttu-id="3bfee-105">Lettura di oggetti attributeSchema e classSchema</span><span class="sxs-lookup"><span data-stu-id="3bfee-105">Reading attributeSchema and classSchema Objects</span></span>

<span data-ttu-id="3bfee-106">In questo argomento vengono forniti esempi di codice e linee guida per la lettura diretta dagli oggetti **attributeSchema** e **classSchema** nel contenitore dello schema.</span><span class="sxs-lookup"><span data-stu-id="3bfee-106">This topic provides code examples and guidelines for reading directly from **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="3bfee-107">Tenere presente che, nella maggior parte delle situazioni di programmazione, quando è necessario leggere i dati relativi a una definizione di classe o attributo, è più efficace leggere i dati dallo schema astratto come descritto in [lettura dello schema astratto](reading-the-abstract-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3bfee-107">Be aware that, in most programming situations, when you must read data about a class or attribute definition, it is more effective to read data from the abstract schema as described in [Reading the Abstract Schema](reading-the-abstract-schema.md).</span></span>

<span data-ttu-id="3bfee-108">Le interfacce e le tecniche utilizzate per leggere dal contenitore dello schema sono quelle utilizzate per leggere qualsiasi oggetto in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="3bfee-108">The interfaces and techniques used to read from the schema container are those used to read any object in Active Directory Domain Services.</span></span> <span data-ttu-id="3bfee-109">Le linee guida includono:</span><span class="sxs-lookup"><span data-stu-id="3bfee-109">The guidelines include:</span></span>

-   <span data-ttu-id="3bfee-110">Per eseguire l'associazione al contenitore dello schema, ottenere il nome distinto che può essere recuperato tramite binding a rootDSE e leggendo la proprietà **schemaNamingContext** , come descritto in [binding senza server e RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="3bfee-110">To bind to the schema container, obtain its distinguished name which can be retrieved by binding to rootDSE and reading the **schemaNamingContext** property, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>
-   <span data-ttu-id="3bfee-111">Usare un puntatore [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) per il contenitore dello schema per enumerare gli oggetti **attributeSchema** e **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="3bfee-111">Use an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer for the schema container to enumerate the **attributeSchema** and **classSchema** objects.</span></span>
-   <span data-ttu-id="3bfee-112">Utilizzare l'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) per recuperare le proprietà di un oggetto **attributeSchema** e **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="3bfee-112">Use the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) or [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface to retrieve the properties of an **attributeSchema** and **classSchema** object.</span></span>
-   <span data-ttu-id="3bfee-113">Usare le funzioni [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) per eseguire il binding diretto a un oggetto **attributeSchema** o **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="3bfee-113">Use the [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) functions to bind directly to an **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="3bfee-114">Se si leggono più oggetti **attributeSchema** o **classSchema** , è possibile migliorare le prestazioni associando a un puntatore [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) sul contenitore dello schema e usando il metodo [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) per eseguire il binding ai singoli oggetti classe e attributo.</span><span class="sxs-lookup"><span data-stu-id="3bfee-114">If you are reading multiple **attributeSchema** or **classSchema** objects, you can increase performance by binding to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the schema container and using the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to bind to the individual class and attribute objects.</span></span> <span data-ttu-id="3bfee-115">Questa operazione è più efficiente rispetto all'esecuzione di chiamate [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) o [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) ripetute per l'associazione ai singoli oggetti classe e attributo.</span><span class="sxs-lookup"><span data-stu-id="3bfee-115">This is more efficient than making repeated [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) or [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) calls to bind to the individual class and attribute objects.</span></span> <span data-ttu-id="3bfee-116">Usare l'attributo **CN** per compilare il percorso relativo per la chiamata a **IADsContainer. GetObject** (ad esempio, "CN = User" per l'oggetto **classSchema** per la classe User).</span><span class="sxs-lookup"><span data-stu-id="3bfee-116">Use the **cn** attribute to build the relative path for the **IADsContainer.GetObject** call (for example, "cn=user" for the **classSchema** object for the user class).</span></span>
-   <span data-ttu-id="3bfee-117">Utilizzare un puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per il contenitore dello schema per eseguire una query sullo schema per gli attributi o le classi che corrispondono a un filtro di ricerca.</span><span class="sxs-lookup"><span data-stu-id="3bfee-117">Use an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer for the schema container to query the schema for attributes or classes that match a search filter.</span></span>

<span data-ttu-id="3bfee-118">Per un esempio di codice in cui vengono illustrati i diversi metodi di ricerca degli oggetti dello schema, vedere il [codice di esempio per la ricerca di oggetti dello schema](example-code-for-searching-for-schema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3bfee-118">For a code example that demonstrates different methods of searching for schema objects, see [Example Code for Searching for Schema Objects](example-code-for-searching-for-schema-objects.md).</span></span>

<span data-ttu-id="3bfee-119">Nell'esempio di codice C++ riportato di seguito viene associato un puntatore [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) sul contenitore dello schema, quindi vengono utilizzate le funzioni [**ADsBuildEnumerator**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) e [**ADsEnumerateNext**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) per enumerarne il contenuto.</span><span class="sxs-lookup"><span data-stu-id="3bfee-119">The following C++ code example binds to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the schema container and then uses the [**ADsBuildEnumerator**](/windows/desktop/api/adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext) functions to enumerate its contents.</span></span> <span data-ttu-id="3bfee-120">Tenere presente che l'enumerazione include tutti gli oggetti **attributeSchema** e **classSchema** , oltre a un singolo oggetto **sottoschema** , ovvero lo schema astratto.</span><span class="sxs-lookup"><span data-stu-id="3bfee-120">Be aware that the enumeration includes all **attributeSchema** and **classSchema** objects as well as a single **subSchema** object, which is the abstract schema.</span></span>

<span data-ttu-id="3bfee-121">Per ogni oggetto enumerato, nell'esempio di codice viene usata la proprietà [**IADs. Class**](/windows/desktop/ADSI/iads-property-methods) per determinare se si tratta di un oggetto **attributeSchema** o **classSchema** .</span><span class="sxs-lookup"><span data-stu-id="3bfee-121">For each enumerated object, the code example uses the [**IADs.Class**](/windows/desktop/ADSI/iads-property-methods) property to determine whether it is an **attributeSchema** or **classSchema** object.</span></span> <span data-ttu-id="3bfee-122">Nell'esempio di codice viene illustrato come leggere le proprietà che non sono disponibili dallo schema astratto.</span><span class="sxs-lookup"><span data-stu-id="3bfee-122">The code example shows how to read the properties that are unavailable from the abstract schema.</span></span>


```C++
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <windows.h>
#include <stdio.h>
#include <ole2.h>
#include <activeds.h>
#include <atlbase.h>

//  Forward declarations.
void ProcessAttribute(IADs *pChild);
void ProcessClass(IADs *pChild);

//  Entry point for the application.
int wmain(int argc, WCHAR* argv[])
{
    HRESULT hr;

    hr = CoInitialize(NULL);
    if(SUCCEEDED(hr))
    {
        CComBSTR sbstrDSPath;
        CComVariant svar;
        IADs *pRootDSE = NULL;
        IADsContainer *pSchema = NULL;  
        IEnumVARIANT *pEnum = NULL;
        ULONG lFetch;
        CComBSTR sbstrClass; 
        DWORD dwClasses = 0, dwAttributes = 0, dwUnknownClass = 0;

        //  Bind to rootDSE to get the schemaNamingContext property.
        hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (void**)&pRootDSE);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = pRootDSE->Get(CComBSTR("schemaNamingContext"), &svar);
        sbstrDSPath = "LDAP://";
        sbstrDSPath += svar.bstrVal;

        //  Bind to the actual schema container.
        wprintf(L"Binding to %s\n", sbstrDSPath);
        hr = ADsGetObject(sbstrDSPath, IID_IADsContainer, (void**) &pSchema);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsGetObject to schema failed: 0x%x\n", hr);
            goto cleanup;
        }

        //  Enumerate the attribute and class objects in the schema container.
        hr = ADsBuildEnumerator(pSchema, &pEnum);
        if (FAILED(hr)) 
        {
            wprintf(L"ADsBuildEnumerator failed: 0x%x\n", hr);
            goto cleanup;
        }

        hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        while(S_OK == hr && 1 == lFetch)
        {
            IADs *pChild = NULL;

            //  Get an IADs pointer on the child object.
            hr = V_DISPATCH(&svar)->QueryInterface(IID_IADs, (void**) &pChild);
            if (SUCCEEDED(hr)) 
            {
                //  Verify that this is a class, attribute, or subSchema object.
                hr = pChild->get_Class(&sbstrClass);
                if (SUCCEEDED(hr)) 
                {
                    //  Get data. This depends on type of schema element.
                    if (_wcsicmp(L"classSchema", sbstrClass) == 0)
                    {
                        dwClasses++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessClass(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"attributeSchema", sbstrClass) == 0)
                    {
                        dwAttributes++;
                        wprintf(L"%s\n", sbstrClass);
                        ProcessAttribute(pChild);
                        wprintf(L"\n");
                    }
                    else if (_wcsicmp(L"subSchema", sbstrClass) == 0) 
                    {
                        wprintf(L"abstract schema");
                        wprintf(L"\n");
                    }
                    else
                    {
                        dwUnknownClass++;
                    }
                }

                pChild->Release();
            }

            hr = ADsEnumerateNext(pEnum, 1, &svar, &lFetch);
        }

        wprintf(L"Classes: %u\nAttributes: %u\nUnknown: %u\n", dwClasses, dwAttributes, dwUnknownClass);

cleanup:
        if (pRootDSE)
        {
            pRootDSE->Release();
        }

        if (pEnum)
        {
            ADsFreeEnumerator(pEnum);
        }

        if (pSchema)
        {
            pSchema->Release();
        }

    }    

    CoUninitialize();

    return 0;
}


//  PrintGUIDFromVariant
//  Prints a GUID in string format.
void PrintGUIDFromVariant(VARIANT varGUID)
{
    HRESULT hr;
    void HUGEP *pArray;
    WCHAR szGUID[40];
    LPGUID pGUID;

    DWORD dwLen = sizeof(GUID);

    hr = SafeArrayAccessData(V_ARRAY(&varGUID), &pArray);
    if(SUCCEEDED(hr))
    {
        pGUID = (LPGUID)pArray;

        //  Convert GUID to string.
        StringFromGUID2(*pGUID, szGUID, 40); 

        //  Print GUID.
        wprintf(L",%s",szGUID);

        SafeArrayUnaccessData(V_ARRAY(&varGUID));
    }
}


// PrintADSPropertyValue
void PrintADSPropertyValue(VARIANT var, BSTR bstrPropName, HRESULT hr) 
{
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (FAILED(hr))
    {
        wprintf(L"get %s failed: 0x%x\n", bstrPropName, hr);
    }
    else 
    {
        switch (var.vt) 
        {
        case VT_BSTR:
            wprintf(L"%s\n", var.bstrVal);
            break;

        case VT_I4:
            wprintf(L"%u\n", var.iVal);
            break;

        case VT_BOOL:
            wprintf(L"%s\n", var.boolVal ? L"TRUE" : L"FALSE");
            break;

        default:
            wprintf(L"-- ??? --\n");
        }
    }
}

//  ProcessAttribute
//  Gets information about an attributeClass object.
void ProcessAttribute(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the attribute Common-Name (cn) property. 
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class linkID. 
    sbstrPropName = "linkID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if(SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSecurityGUID. 
    sbstrPropName = "attributeSecurityGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (E_ADS_PROPERTY_NOT_FOUND == hr)
    {
        wprintf(L"-- not set --\n");
    }
    else if (SUCCEEDED(hr))
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the attribute attributeSyntax property. 
    sbstrPropName = "attributeSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the attribute's oMSyntax property. 
    sbstrPropName = "oMSyntax";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}


//  ProcessClass
//  Gets information about a schema class.
void ProcessClass(IADs *pChild)
{
    HRESULT hr;
    CComVariant svar;
    CComBSTR sbstrPropName;

    //  Get the class cn.
    sbstrPropName = "cn";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class lDAPDisplayName.
    sbstrPropName = "lDAPDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class schemaIDGUID. 
    sbstrPropName = "schemaIDGUID";
    hr = pChild->Get(sbstrPropName, &svar);
    if (FAILED(hr))
    {
        wprintf(L",get schemaIDGUID failed: 0x%x", hr);
    }
    else 
    {
        PrintGUIDFromVariant(svar);
    }

    //  Get the class adminDescription property. 
    sbstrPropName = "adminDescription";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class adminDisplayName property. 
    sbstrPropName = "adminDisplayName";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class rDNAttID. 
    sbstrPropName = "rDNAttID";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultHidingValue. 
    sbstrPropName = "defaultHidingValue";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultObjectCategory. 
    sbstrPropName = "defaultObjectCategory";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class systemOnly value.
    sbstrPropName = "systemOnly";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);

    //  Get the class defaultSecurityDescriptor.
    sbstrPropName = "defaultSecurityDescriptor";
    hr = pChild->Get(sbstrPropName, &svar);
    PrintADSPropertyValue(svar, sbstrPropName, hr);
}
```



 

 