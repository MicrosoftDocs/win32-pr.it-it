---
description: Utilizzo di script delle regole business in C++ per fornire la logica di run-time per il controllo dell'accesso.
ms.assetid: 058086ab-8ebd-4ff6-b552-8d3c19ae5d38
title: Qualificazione dell'accesso con la logica di business in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e176fb9cbb221fb52404e22c7ba61d272897082c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129914"
---
# <a name="qualifying-access-with-business-logic-in-c"></a><span data-ttu-id="8dc0e-103">Qualificazione dell'accesso con la logica di business in C++</span><span class="sxs-lookup"><span data-stu-id="8dc0e-103">Qualifying Access with Business Logic in C++</span></span>

<span data-ttu-id="8dc0e-104">Usare gli script delle regole business per fornire la logica di run-time per il controllo dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-104">Use business rule scripts to provide run-time logic for checking access.</span></span> <span data-ttu-id="8dc0e-105">Per ulteriori informazioni sulle regole business, vedere [regole business](business-rules.md).</span><span class="sxs-lookup"><span data-stu-id="8dc0e-105">For more information about business rules, see [Business Rules](business-rules.md).</span></span>

<span data-ttu-id="8dc0e-106">Per assegnare una regola business a un'attività, impostare innanzitutto la proprietà [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) dell'oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) che rappresenta l'attività.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-106">To assign a business rule to a task, first set the [**BizRuleLanguage**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrulelanguage) property of the [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object that represents the task.</span></span> <span data-ttu-id="8dc0e-107">Lo script deve essere in Visual Basic Scripting Edition o JScript.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-107">The script must be in Visual Basic Scripting Edition or JScript.</span></span> <span data-ttu-id="8dc0e-108">Dopo aver specificato il linguaggio di script, impostare la proprietà [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) dell'oggetto **IAzTask** con una rappresentazione di stringa dello script.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-108">After you specify the script language, set the [**BizRule**](/windows/desktop/api/Azroles/nf-azroles-iaztask-get_bizrule) property of the **IAzTask** object with a string representation of the script.</span></span>

<span data-ttu-id="8dc0e-109">Quando si verifica l'accesso per un'operazione contenuta da un'attività a cui è associata una regola business, l'applicazione deve creare due matrici con le stesse dimensioni da passare come parametri *varParameterNames* e *VarParameterValues* del metodo [**IAzClientContext:: AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) .</span><span class="sxs-lookup"><span data-stu-id="8dc0e-109">When checking access for an operation contained by a task that has an associated business rule, the application must create two arrays of the same size to be passed as the *varParameterNames* and *varParameterValues* parameters of the [**IAzClientContext::AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method.</span></span> <span data-ttu-id="8dc0e-110">Per informazioni sulla creazione di un contesto client, vedere [definizione di un contesto client con gestione autorizzazioni in C++](establishing-a-client-context-with-authorization-manager-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="8dc0e-110">For information about creating a client context, see [Establishing a Client Context with Authorization Manager in C++](establishing-a-client-context-with-authorization-manager-in-c--.md).</span></span>

<span data-ttu-id="8dc0e-111">Il metodo [**IAzClientContext:: AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) crea un oggetto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) che viene passato allo script della regola business.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-111">The [**IAzClientContext::AccessCheck**](/windows/desktop/api/Azroles/nf-azroles-iazclientcontext-accesscheck) method creates an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is passed to the business rule script.</span></span> <span data-ttu-id="8dc0e-112">Lo script imposta quindi la proprietà [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) dell'oggetto **AzBizRuleContext** .</span><span class="sxs-lookup"><span data-stu-id="8dc0e-112">The script then sets the [**BusinessRuleResult**](/windows/desktop/api/Azroles/nf-azroles-iazbizrulecontext-put_businessruleresult) property of the **AzBizRuleContext** object.</span></span> <span data-ttu-id="8dc0e-113">Il valore **true** indica che è stato concesso l'accesso e il valore **false** indica che l'accesso è stato negato.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-113">A value of **TRUE** indicates that access is granted, and a value of **FALSE** indicates that access is denied.</span></span>

<span data-ttu-id="8dc0e-114">Non è possibile assegnare uno script della regola business a un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) contenuto in un oggetto [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) delegato.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-114">A business rule script cannot be assigned to an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object contained by a delegated [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span>

<span data-ttu-id="8dc0e-115">Nell'esempio seguente viene illustrato come utilizzare uno script della regola business per controllare l'accesso di un client a un'operazione.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-115">The following example shows how to use a business rule script to check a client's access to an operation.</span></span> <span data-ttu-id="8dc0e-116">Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense, un'attività denominata Submit Expense e un'operazione denominata UseFormControl e che la variabile hToken contiene un token client valido.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-116">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, a task named Submit Expense, and an operation named UseFormControl, and that the variable hToken contains a valid client token.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <azroles.h>

void CheckAccess(ULONGLONG hToken)
//  Void CheckAccess().
{
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzClientContext* pClientContext = NULL;
    IAzOperation* pOperation = NULL;
    IAzTask* pTask = NULL;
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR operationName = NULL;
    BSTR objectName = NULL;
    BSTR taskName = NULL;
    BSTR bizRule = NULL;
    BSTR bizRuleLanguage = NULL;
    LONG operationID;
    HRESULT hr;
    VARIANT varOperationIdArray;
    VARIANT varOperationId;
    VARIANT varResultsArray;
    VARIANT varResult;
    VARIANT varParamName;
    VARIANT varParamValue;
    VARIANT nameString;
    VARIANT expenseAmount;
    void MyHandleError(char *s);

    VARIANT myVar;
    VariantInit(&myVar);

    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");

    //  Allocate a string for the policy store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(0, storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a client context from a token handle.
    hr = pApp->InitializeClientContextFromToken(hToken, myVar,
          &pClientContext);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create client context.");

    //  Create a business rule for the Submit Expense task.

    //  Open the Submit Expense task.
    if(!(taskName = SysAllocString(L"Submit Expense")))
        MyHandleError("Could not allocate task name string.");
    hr = pApp->OpenTask(taskName, myVar, &pTask);

    //  Assign a business rule to the task.

    //  Set the business rule language to VBScript.
    if(!(bizRuleLanguage = SysAllocString(L"VBScript")))
        MyHandleError("Could not allocate business rule language string.");
    hr = pTask->put_BizRuleLanguage(bizRuleLanguage);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not allocate business rule language string.");

    //  Create a BSTR with the business rule code.
    if(!(bizRule = SysAllocString(
        L"Dim Amount \n"
        L"AzBizRuleContext.BusinessRuleResult = FALSE \n"
        L"Amount = AzBizRuleContext.GetParameter(\"ExpAmount\") \n"
        L"if Amount < 500 then AzBizRuleContext.BusinessRuleResult = TRUE"
        )))
         MyHandleError("Could not allocate business rule string.");

    
    hr = pTask->put_BizRule(bizRule);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not assign business rule.");

    //  Save the new task data to the store.
    hr = pTask->Submit(0, myVar);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data.");

    //  Set up parameters for access check.

    //  Set up the object name.
    if (!(operationName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");

    //  Get the ID of the operation to check.
    hr = pApp->OpenOperation(operationName, myVar, &pOperation);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open operation.");

    hr = pOperation->get_OperationID(&operationID);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not get operation ID.");

    //  Create a SAFEARRAY for the operation ID.
    varOperationIdArray.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);

    //  Create an array of indexes.
    LONG* index = new LONG[1];
    index[0] = 0;

    //  Populate a SAFEARRAY with the operation ID.
    varOperationId.vt = VT_I4;
    varOperationId.lVal = operationID;

    hr = SafeArrayPutElement(varOperationIdArray.parray, index,
          &varOperationId);
    if(!(SUCCEEDED(hr)))
        MyHandleError("Could not put operation ID in array.");
    
    //  Set SAFEARRAY type.
    varOperationIdArray.vt = VT_ARRAY | VT_VARIANT;

    //  Create business rule parameters.

    //  Create array of business rule parameter names.
    varParamName.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);
    varParamName.vt = VT_ARRAY | VT_VARIANT;
    nameString.vt = VT_BSTR;
    nameString.bstrVal = SysAllocString(L"ExpAmount");
    SafeArrayPutElement(varParamName.parray, index, &nameString);

    //  Create array of business rule parameter values.
    varParamValue.parray = SafeArrayCreateVector(VT_VARIANT, 0, 1);
    varParamValue.vt = VT_ARRAY | VT_VARIANT;
    expenseAmount.vt = VT_I4;
    expenseAmount.lVal = 100;  // access denied if 500 or more
    SafeArrayPutElement(varParamValue.parray, index, &expenseAmount);

    if(!(objectName = SysAllocString(L"UseFormControl")))//used for audit
        MyHandleError("Could not allocate object name string.");

    //  Check access.
    hr = pClientContext->AccessCheck(
        objectName,
        myVar,                  // use default application scope
        varOperationIdArray,
        varParamName,
        varParamValue,
        myVar,
        myVar,
        myVar,
        &varResultsArray);

    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not complete access check.");

    hr = SafeArrayGetElement(varResultsArray.parray, index, &varResult);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not get result from array.");

    if (varResult.lVal == 0)
        printf("Access granted.\n");
    else
        printf("Access denied.\n");
    

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pOperation->Release();
    pClientContext->Release();
    pTask->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    SysFreeString(operationName);
    SysFreeString(objectName);
    SysFreeString(taskName);
    SysFreeString(bizRule);
    SysFreeString(bizRuleLanguage);
    VariantClear(&myVar);
    VariantClear(&varOperationIdArray);
    VariantClear(&varOperationId);
    VariantClear(&varResultsArray);
    VariantClear(&varResult);
    VariantClear(&varParamName);
    VariantClear(&varParamValue);
    VariantClear(&nameString);
    VariantClear(&expenseAmount);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



