---
description: Rinomina un computer.
ms.assetid: 9d338ebe-caf0-42c4-995f-fd750e5664df
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ca60021c921e47de3c7afd5b8ee0bb2ea5e6d12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049095"
---
# <a name="rename-method-of-the-win32_computersystem-class"></a><span data-ttu-id="fd0df-103">Rinominare il metodo della \_ classe Win32 ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="fd0df-103">Rename method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="fd0df-104">Il metodo **Rename Rinomina** un computer.</span><span class="sxs-lookup"><span data-stu-id="fd0df-104">The **Rename** method renames a computer.</span></span>

<span data-ttu-id="fd0df-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fd0df-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fd0df-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fd0df-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd0df-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd0df-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name,
  [in] string Password,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="fd0df-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd0df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd0df-109">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd0df-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0df-110">Nuovo nome del computer.</span><span class="sxs-lookup"><span data-stu-id="fd0df-110">New computer name.</span></span> <span data-ttu-id="fd0df-111">Il valore di questo parametro non può includere caratteri di controllo, spazi iniziali o finali o uno dei caratteri seguenti:/ \\ \\ \[ \] .</span><span class="sxs-lookup"><span data-stu-id="fd0df-111">The value of this parameter cannot include control characters, leading or trailing spaces, or any of the following characters: / \\\\ \[ \].</span></span>

</dd> <dt>

<span data-ttu-id="fd0df-112">*Password* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fd0df-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0df-113">Password da utilizzare per la connessione al controller di dominio se il parametro *username* specifica un nome di account.</span><span class="sxs-lookup"><span data-stu-id="fd0df-113">Password to use when connecting to the domain controller if the *UserName* parameter specifies an account name.</span></span> <span data-ttu-id="fd0df-114">In caso contrario, questo parametro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="fd0df-114">Otherwise, this parameter must be **NULL**.</span></span> <span data-ttu-id="fd0df-115">Per ulteriori informazioni sui parametri *password* e *username* , vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="fd0df-115">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="fd0df-116">*Nome utente* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd0df-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd0df-117">Stringa che specifica il nome dell'account da utilizzare per la connessione al controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="fd0df-117">String that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="fd0df-118">La stringa deve essere con terminazione **null** e deve specificare un nome NetBIOS di dominio e un account utente, ad esempio "DomainName \\ username" o " someone@domainname.com ", che è un nome dell'entità utente (UPN).</span><span class="sxs-lookup"><span data-stu-id="fd0df-118">The string must be **null**-terminated, and must specify a domain NetBIOS name and user account for example, "DOMAINNAME\\username" or "someone@domainname.com", which is a user principal name (UPN).</span></span> <span data-ttu-id="fd0df-119">Se il parametro **username** è **null**, WMI usa il contesto del chiamante.</span><span class="sxs-lookup"><span data-stu-id="fd0df-119">If the **UserName** parameter is **NULL**, WMI uses the context of the caller.</span></span> <span data-ttu-id="fd0df-120">Per ulteriori informazioni sui parametri *password* e *username* , vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="fd0df-120">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd0df-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd0df-121">Return value</span></span>

<span data-ttu-id="fd0df-122">Restituisce 0 (zero) se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fd0df-122">Returns a 0 (zero) if successful.</span></span> <span data-ttu-id="fd0df-123">Un valore restituito diverso da zero indica un errore.</span><span class="sxs-lookup"><span data-stu-id="fd0df-123">A nonzero return value indicates an error.</span></span> <span data-ttu-id="fd0df-124">Se l'operazione ha esito positivo, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="fd0df-124">If successful, a reboot is required.</span></span> <span data-ttu-id="fd0df-125">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fd0df-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fd0df-126">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fd0df-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fd0df-127">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="fd0df-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fd0df-128">**Altro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="fd0df-128">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fd0df-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd0df-129">Remarks</span></span>

<span data-ttu-id="fd0df-130">È possibile utilizzare il metodo **Rename** per rinominare un computer se si è un membro del gruppo Administrators locale.</span><span class="sxs-lookup"><span data-stu-id="fd0df-130">You can use the **Rename** method to rename a computer if you are a member of the local administrator group.</span></span> <span data-ttu-id="fd0df-131">Tuttavia, non è possibile usare il metodo in remoto per i computer del dominio.</span><span class="sxs-lookup"><span data-stu-id="fd0df-131">However, you cannot use the method remotely for domain computers.</span></span>

<span data-ttu-id="fd0df-132">Se vengono specificati i parametri *password* e *username* , la connessione a WMI deve usare il livello di autenticazione **\_ \_ \_ \_ PKT \_ privacy** (**wbemAuthenticationLevelPktPrivacy** for script and Visual Basic (VB)) RPC C.</span><span class="sxs-lookup"><span data-stu-id="fd0df-132">If the *Password* and *UserName* parameters are specified, the connection to WMI must use the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy** for script and Visual Basic (VB)) authentication level.</span></span>

<span data-ttu-id="fd0df-133">Per connettersi a un computer remoto e specificare le credenziali, utilizzare la connessione all'oggetto Locator, ovvero IWbemLocator per C++, e SWbemLocator per script e VB.</span><span class="sxs-lookup"><span data-stu-id="fd0df-133">To connect to a remote computer and specify credentials, use the locator object connection, which is IWbemLocator for C++, and SWbemLocator for script and VB.</span></span> <span data-ttu-id="fd0df-134">Non utilizzare la connessione del moniker.</span><span class="sxs-lookup"><span data-stu-id="fd0df-134">Do not use the moniker connection.</span></span>

<span data-ttu-id="fd0df-135">Per connettersi a un computer locale, non è possibile specificare una password o un'autorità di autenticazione, ad esempio Kerberos.</span><span class="sxs-lookup"><span data-stu-id="fd0df-135">To connect to a local computer, you cannot specify a password or an authentication authority, such as Kerberos.</span></span> <span data-ttu-id="fd0df-136">È possibile specificare la password e l'autorità solo in connessioni ai computer remoti.</span><span class="sxs-lookup"><span data-stu-id="fd0df-136">You can only specify the password and authority in connections to remote computers.</span></span>

<span data-ttu-id="fd0df-137">Se il livello di autenticazione è troppo basso quando si specificano una *password* e un *nome utente* , WMI restituisce l'errore richiesto per la **connessione a WBEM \_ e \_ crittografata \_ \_** per C/C++ e **wbemErrEncryptedConnectionRequired** per lo script e VB.</span><span class="sxs-lookup"><span data-stu-id="fd0df-137">If the authentication level is too low when a *Password* and *UserName* are specified, then WMI returns the **WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED** error for C/C++, and **wbemErrEncryptedConnectionRequired** for script and VB.</span></span>

<span data-ttu-id="fd0df-138">Per altre informazioni, vedere [**SWbemLocator \_ ConnectServer,**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator:: ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver)e [costruzione di una stringa del moniker](/windows/desktop/WmiSdk/constructing-a-moniker-string).</span><span class="sxs-lookup"><span data-stu-id="fd0df-138">For more information, see [**SWbemLocator\_ConnectServer,**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator::ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver), and [Constructing a Moniker String](/windows/desktop/WmiSdk/constructing-a-moniker-string).</span></span>

## <a name="examples"></a><span data-ttu-id="fd0df-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="fd0df-139">Examples</span></span>

<span data-ttu-id="fd0df-140">Lo script seguente illustra come rinominare un computer locale.</span><span class="sxs-lookup"><span data-stu-id="fd0df-140">The following script shows you how to rename a local computer.</span></span>


```VB
Name = "name"
Password = "password"
Username = "username"

Set objWMIService = GetObject("Winmgmts:root\cimv2")

' Call always gets only one Win32_ComputerSystem object.
For Each objComputer in _
    objWMIService.InstancesOf("Win32_ComputerSystem")

        Return = objComputer.rename(Name,Password,Username)
        If Return <> 0 Then
           WScript.Echo "Rename failed. Error = " & Err.Number
        Else
           WScript.Echo "Rename succeeded." & _
               " Reboot for new name to go into effect"
        End If

Next
```



<span data-ttu-id="fd0df-141">Il seguente esempio di codice C++ Rinomina un computer.</span><span class="sxs-lookup"><span data-stu-id="fd0df-141">The following C++ code sample renames a computer system.</span></span>


```C++
int set_computer_name(const string &newname/*, const string &username, const string &password*/)
{
 HRESULT hres;


// Step 1: --------------------------------------------------
 // Initialize COM. ------------------------------------------


hres = CoInitializeEx(0, COINIT_MULTITHREADED); 
 if (FAILED(hres))
 {
 cout << "Failed to initialize COM library. Error code = 0x" 
 << hex << hres << endl;
 return 1; // Program has failed.
 }


// Step 2: --------------------------------------------------
 // Set general COM security levels --------------------------
 // Note: If you are using Windows 2000, you need to specify -
 // the default authentication credentials for a user by using
 // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
 // parameter of CoInitializeSecurity ------------------------


hres = CoInitializeSecurity(
 NULL, 
 -1, // COM authentication
 NULL, // Authentication services
 NULL, // Reserved
 RPC_C_AUTHN_LEVEL_DEFAULT, // Default authentication 
 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation 
 NULL, // Authentication info
 EOAC_NONE, // Additional capabilities 
 NULL // Reserved
 );




 if (FAILED(hres))
 {
 cout << "Failed to initialize security. Error code = 0x" 
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
 }

 // Step 3: ---------------------------------------------------
 // Obtain the initial locator to WMI -------------------------


IWbemLocator *pLoc = NULL;


hres = CoCreateInstance(
 CLSID_WbemLocator, 
 0, 
 CLSCTX_INPROC_SERVER, 
 IID_IWbemLocator, (LPVOID *) &pLoc);

 if (FAILED(hres))
 {
 cout << "Failed to create IWbemLocator object."
 << " Err code = 0x"
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 4: -----------------------------------------------------
 // Connect to WMI through the IWbemLocator::ConnectServer method


IWbemServices *pSvc = NULL;

 // Connect to the root\cimv2 namespace with
 // the current user and obtain pointer pSvc
 // to make IWbemServices calls.
 hres = pLoc->ConnectServer(
 _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
 NULL, // User name. NULL = current user
 NULL, // User password. NULL = current
 0, // Locale. NULL indicates current
 NULL, // Security flags.
 0, // Authority (e.g. Kerberos)
 0, // Context object 
 &pSvc // pointer to IWbemServices proxy
 );

 if (FAILED(hres))
 {
 cout << "Could not connect. Error code = 0x" 
 << hex << hres << endl;
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


/*cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;*/




 // Step 5: --------------------------------------------------
 // Set security levels on the proxy -------------------------


hres = CoSetProxyBlanket(
 pSvc, // Indicates the proxy to set
 RPC_C_AUTHN_WINNT, // RPC_C_AUTHN_xxx
 RPC_C_AUTHZ_NONE, // RPC_C_AUTHZ_xxx
 NULL, // Server principal name 
 RPC_C_AUTHN_LEVEL_CALL, // RPC_C_AUTHN_LEVEL_xxx 
 RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
 NULL, // client identity
 EOAC_NONE // proxy capabilities 
 );


if (FAILED(hres))
 {
 cout << "Could not set proxy blanket. Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 6: --------------------------------------------------
 // Use the IWbemServices pointer to make requests of WMI ----


// For example, get the name of the operating system
 IEnumWbemClassObject* pEnumerator = NULL;
 hres = pSvc->ExecQuery(
 bstr_t("WQL"), 
 bstr_t("SELECT * FROM Win32_ComputerSystem"),
 WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
 NULL,
 &pEnumerator);

 if (FAILED(hres))
 {
 cout << "Query for operating system name failed."
 << " Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release();
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 7: -------------------------------------------------
 // Get the data from the query in step 6 -------------------

 IWbemClassObject *pclsObj;
 ULONG uReturn = 0;

 while (pEnumerator)
 {
 HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
 &pclsObj, &uReturn);


if(0 == uReturn)
 {
 break;
 }


// set up to call the Win32_ComputerSystem::Rename method
 BSTR MethodName = SysAllocString(L"Rename");
 BSTR ClassName = SysAllocString(L"Win32_ComputerSystem");


IWbemClassObject* pClass = NULL;
 hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);


IWbemClassObject* pInParamsDefinition = NULL;
 hres = pClass->GetMethod(MethodName, 0, 
 &pInParamsDefinition, NULL);


IWbemClassObject* pClassInstance = NULL;
 hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);


// Create the values for the in parameters
 wstring val;
 BSTR NewName;
 val.assign(newname.begin(), newname.end());
 NewName = SysAllocString(val.c_str());


VARIANT varName;
 varName.vt = VT_BSTR;
 varName.bstrVal = NewName;


// Store the value for the in parameters
 hres = pClassInstance->Put(L"Name", 0,
 &varName, 0);
 wprintf(L"Set computer name to %s\n", V_BSTR(&varName));


VARIANT var;
 CIMTYPE pType;
 LONG pFlavor;
 pclsObj->Get(L"__PATH",0,&var,&pType,&pFlavor);


// Execute Method
 IWbemClassObject* pOutParams = NULL;
 hres = pSvc->ExecMethod(var.bstrVal, MethodName, 0,
 NULL, pClassInstance, &pOutParams, NULL);


if (FAILED(hres))
 {
 cout << "Could not execute method. Error code = 0x" 
 << hex << hres << endl;
 VariantClear(&varName);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 1; // Program has failed.
 }


// To see what the method returned,
 // use the following code. The return value will
 // be in &varReturnValue
 VARIANT varReturnValue;
 hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
 &varReturnValue, NULL, 0);




 // Clean up
 //--------------------------
 VariantClear(&varName);
 VariantClear(&varReturnValue);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 0;


}


// Cleanup
 // ========

 pSvc->Release();
 pLoc->Release();
 pEnumerator->Release();
 pclsObj->Release();
 CoUninitialize();


return 0; // Program successfully completed.
```



## <a name="requirements"></a><span data-ttu-id="fd0df-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd0df-142">Requirements</span></span>



| <span data-ttu-id="fd0df-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd0df-143">Requirement</span></span> | <span data-ttu-id="fd0df-144">Valore</span><span class="sxs-lookup"><span data-stu-id="fd0df-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd0df-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd0df-145">Minimum supported client</span></span><br/> | <span data-ttu-id="fd0df-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd0df-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd0df-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd0df-147">Minimum supported server</span></span><br/> | <span data-ttu-id="fd0df-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd0df-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd0df-149">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd0df-149">Namespace</span></span><br/>                | <span data-ttu-id="fd0df-150">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fd0df-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd0df-151">MOF</span><span class="sxs-lookup"><span data-stu-id="fd0df-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd0df-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd0df-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd0df-153">DLL</span><span class="sxs-lookup"><span data-stu-id="fd0df-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd0df-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd0df-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd0df-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd0df-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd0df-156">**\_ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="fd0df-156">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="fd0df-157">Attività WMI: account e domini</span><span class="sxs-lookup"><span data-stu-id="fd0df-157">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> </dl>

 

