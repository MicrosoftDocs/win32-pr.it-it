---
description: In generale, questo metodo verrà chiamato da DllUnregisterServer. Il codice di esempio seguente può essere inserito nel codice per DllUnregisterServer.
ms.assetid: a5567c3b-edc0-427a-9751-ba221611e92c
title: Annullare la registrazione di un terminale collegabile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3068cd6d749dda2f1b6618672a1aabaace72ba6c3ef137c1c47952209c87f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518111"
---
# <a name="unregister-a-pluggable-terminal"></a>Annullare la registrazione di un terminale collegabile

In generale, questo metodo verrà chiamato da **DllUnregisterServer.** Il codice di esempio seguente può essere inserito nel codice per **DllUnregisterServer**.

``` syntax
ITPluggableTerminalClassRegistration* pTerminal;

BSTR bstrTerminalSuperclass = SysAllocString(L"{F7438990-D6EB-11d0-82A6-00AA00B5CA1B}");

// If (NULL == bstrTermSuperclass) process the error here.

BSTR bstrTerminalClass = SysAllocString(L"{AED6483E-3304-11d2-86F1-006008B0E5D2}");

// If (NULL == bstrTerminalClass) process the error here.

HRESULT hr;
hr = CoCreateInstance( 
    CLSID_PluggableTerminalRegistration,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_ITPluggableTerminalClassRegistration,
    (void**)&pTerminal);

hr = pTerminal->put_TerminalClass( bstrTerminalClass );
// If (hr != S_OK) process the error here. 
hr = pTerminal->Delete( bstrTerminalSuperclass );
// If (hr != S_OK) process the error here. 

// Release the memory created by SysAllocString().
SysFreeString(bstrTerminalClass);
SysFreeString(bstrTerminalSuperclass);
```

 

 



