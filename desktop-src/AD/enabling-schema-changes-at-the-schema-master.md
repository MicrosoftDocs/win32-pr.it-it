---
title: Abilitazione delle modifiche dello schema nel master schema
description: Per impostazione predefinita, la modifica dello schema è disabilitata in tutti i controller di dominio Windows 2000.
ms.assetid: 08806a9e-283c-48d9-9557-bcb9719fc13c
ms.tgt_platform: multiple
keywords:
- Abilitazione delle modifiche dello schema nell'annuncio master dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4840c9928011179ce303c83f4d00ef598f38eb64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955149"
---
# <a name="enabling-schema-changes-at-the-schema-master"></a><span data-ttu-id="2db03-104">Abilitazione delle modifiche dello schema nel master schema</span><span class="sxs-lookup"><span data-stu-id="2db03-104">Enabling Schema Changes at the Schema Master</span></span>

<span data-ttu-id="2db03-105">Per impostazione predefinita, la modifica dello schema è disabilitata in tutti i controller di dominio Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2db03-105">By default, schema modification is disabled on all Windows 2000 domain controllers.</span></span> <span data-ttu-id="2db03-106">La possibilità di aggiornare lo schema è controllata dal valore del registro di sistema seguente nel controller di dominio master dello schema:</span><span class="sxs-lookup"><span data-stu-id="2db03-106">The ability to update the schema is controlled by the following registry value on the schema master domain controller:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            NTDS
               Parameters
                  Schema Update Allowed
```

<span data-ttu-id="2db03-107">Questo valore del registro di sistema è un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2db03-107">This registry value is a **REG\_DWORD** value.</span></span> <span data-ttu-id="2db03-108">Se questo valore non è presente o contiene zero (0), la modifica dello schema è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="2db03-108">If this value is not present or contains zero (0), then schema modification is disabled.</span></span> <span data-ttu-id="2db03-109">Se questo valore è presente e contiene un valore diverso da zero, la modifica dello schema è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2db03-109">If this value is present and contains a value other than zero, then schema modification is enabled.</span></span>

<span data-ttu-id="2db03-110">Lo snap-in MMC di gestione dello schema consente all'utente di abilitare o disabilitare manualmente la modifica dello schema.</span><span class="sxs-lookup"><span data-stu-id="2db03-110">The Schema Manager MMC snap-in provides the user with the ability to manually enable or disable schema modification.</span></span> <span data-ttu-id="2db03-111">La modifica dello schema può essere abilitata o disabilitata a livello di codice modificando questo valore del registro di sistema nel controller di dominio master dello schema.</span><span class="sxs-lookup"><span data-stu-id="2db03-111">Schema modification can be enabled or disabled programmatically by modifying this registry value on the schema master domain controller.</span></span>

<span data-ttu-id="2db03-112">Nella funzione C++ seguente viene illustrato come determinare se lo schema può essere modificato in un master schema specificato.</span><span class="sxs-lookup"><span data-stu-id="2db03-112">The following C++ function shows how to determine if the schema can be modified on a specified schema master.</span></span>


```C++
HRESULT IsSchemaUpdateEnabled(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL *pfEnabled)
{
    *pfEnabled = FALSE;
  
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    tcscpy_s(pszPath, szPrefix);
    tcscat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szKeyPath, 
            0, 
            KEY_READ, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwType;
            DWORD dwValue;
            DWORD dwSize;

            dwSize = sizeof(dwValue);
            lReturn = RegQueryValueEx(
                hKeyParameters, 
                szValueName, 
                0, 
                &dwType, 
                (LPBYTE)&dwValue, 
                &dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                *pfEnabled = (0 != dwValue);
                
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
  
    return hr;
}
```



<span data-ttu-id="2db03-113">La seguente funzione C++ illustra come abilitare o disabilitare la modifica dello schema in un master schema specificato.</span><span class="sxs-lookup"><span data-stu-id="2db03-113">The following C++ function shows how to enable or disable schema modification on a specified schema master.</span></span>


```C++
HRESULT EnableSchemaUpdate(
    LPTSTR pszSchemaMasterComputerName, 
    BOOL fEnabled)
{
    
    LPTSTR szPrefix = "\\\\";
    LPTSTR pszPath = new TCHAR[lstrlen(szPrefix) + 
        lstrlen(pszSchemaMasterComputerName) + 1];
    if(!pszPath)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = E_FAIL;
    LONG lReturn;
    HKEY hKeyMachine;

    strcpy_s(pszPath, szPrefix);
    strcat_s(pszPath, pszSchemaMasterComputerName);
    lReturn = RegConnectRegistry(
        pszPath, 
        HKEY_LOCAL_MACHINE, 
        &hKeyMachine);
    
    delete [] pszPath;

    if (ERROR_SUCCESS == lReturn)
    {
        HKEY hKeyParameters;
        LPTSTR szRelKeyPath = 
          TEXT("System\\CurrentControlSet\\Services\\NTDS\\Parameters");
        LPTSTR szValueName = TEXT("Schema Update Allowed");

        lReturn = RegOpenKeyEx(
            hKeyMachine, 
            szRelKeyPath, 
            0, 
            KEY_SET_VALUE, 
            &hKeyParameters);
        if (ERROR_SUCCESS == lReturn)
        {
            DWORD dwValue;
            DWORD dwSize;

            if(fEnabled)
            {
                dwValue = 1;
            }
            else
            {
                dwValue = 0;
            }
            
            dwSize = sizeof(dwValue);
            lReturn = RegSetValueEx(
                hKeyParameters, 
                szValueName, 
                0L, 
                REG_DWORD, 
                (LPBYTE)&dwValue, 
                dwSize);
            if (ERROR_SUCCESS == lReturn)
            {
                hr = S_OK;
            }
            
            RegCloseKey(hKeyParameters);
        }
    
        RegCloseKey(hKeyMachine);
    }
    
    return hr;
}
```



 

 




