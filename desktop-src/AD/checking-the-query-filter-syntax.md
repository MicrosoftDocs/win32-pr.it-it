---
title: Verifica della sintassi del filtro query
description: L'API LDAP fornisce una semplice funzione di verifica della sintassi. Tenere presente che verifica solo la sintassi e non l'esistenza delle proprietà specificate nel filtro.
ms.assetid: 4e564cd9-2f8b-4e70-928c-3a8bd804aeba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da2c15052309bc2acbcff9d6bdabea95337db1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044013"
---
# <a name="checking-the-query-filter-syntax"></a><span data-ttu-id="a7f3c-104">Verifica della sintassi del filtro query</span><span class="sxs-lookup"><span data-stu-id="a7f3c-104">Checking the Query Filter Syntax</span></span>

<span data-ttu-id="a7f3c-105">L'API LDAP fornisce una semplice funzione di verifica della sintassi.</span><span class="sxs-lookup"><span data-stu-id="a7f3c-105">The LDAP API provides a simple syntax-verification function.</span></span> <span data-ttu-id="a7f3c-106">Tenere presente che verifica solo la sintassi e non l'esistenza delle proprietà specificate nel filtro.</span><span class="sxs-lookup"><span data-stu-id="a7f3c-106">Be aware that it only verifies the syntax and not the existence of the properties specified in the filter.</span></span>

<span data-ttu-id="a7f3c-107">La funzione seguente verifica la sintassi del filtro di query e restituisce **\_ OK** se il filtro è valido o s false in \_ caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a7f3c-107">The following function verifies the syntax of the query filter and returns **S\_OK** if the filter is valid or S\_FALSE if it is not.</span></span>


```C++
HRESULT CheckFilterSyntax(
    LPOLESTR szServer, // NULL binds to a DC in the current domain.
    LPOLESTR szFilter) // Filter to check.
{
HRESULT hr = S_OK;
DWORD dwReturn;
LDAP *hConnect = NULL;  // Connection handle
 
if (!szFilter)
  return E_POINTER;
 
// LDAP_PORT is the default port, 389
 
hConnect  = ldap_open(szServer,  LDAP_PORT);
 
// Bind using the preferred authentication method on Windows 2000
// and the calling thread's security context.
 
dwReturn = ldap_bind_s( hConnect, NULL, NULL, LDAP_AUTH_NEGOTIATE );
if (dwReturn==LDAP_SUCCESS) {
    dwReturn = ldap_check_filter(hConnect, szFilter);
    if (dwReturn==LDAP_SUCCESS)
        hr = S_OK;
    else
        hr = S_FALSE;
}
 
// Unbind to free the connection.
 
ldap_unbind( hConnect );
 
return hr;
}
```



 

 




