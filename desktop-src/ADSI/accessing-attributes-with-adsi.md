---
title: Accesso agli attributi con ADSI
description: I metodi IADs.Get e IADs.GetEx vengono usati per recuperare i valori degli attributi denominati.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Attributi, accesso con ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e37c63b61986a56e7b22f114b5956d9e047f1ae45b5dc2e653074ea35440f10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024129"
---
# <a name="accessing-attributes-with-adsi"></a>Accesso agli attributi con ADSI

I [**metodi IADs.Get e**](/windows/desktop/api/Iads/nf-iads-iads-get) [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) vengono usati per recuperare i valori degli attributi denominati. Entrambi i metodi restituiscono [**un valore VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) Questi metodi sono disponibili solo per le directory che supportano uno schema. Quando si accede a oggetti in una directory senza uno schema, è necessario usare le interfacce [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) per modificare i valori degli attributi.

I [**metodi IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituiscono una [**variant**](/windows/win32/api/oaidl/ns-oaidl-variant) che può essere o meno una matrice **VARIANT** a seconda del numero di valori restituiti dal server. Ad esempio, se dal server viene restituito un solo valore, indipendentemente dal fatto che si tratta di un attributo singolo o multivalore, il metodo restituisce un singolo **variant**. Viceversa, se vengono restituiti più valori, viene **restituita una** matrice VARIANT. Se viene restituita una matrice **VARIANT,** il membro **vt** della struttura **VARIANT** contiene i flag **\_ VT VARIANT/vbVariant** e **VT \_ ARRAY/vbArray.**

I [**metodi IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) possono anche restituire un oggetto COM usando [**l'interfaccia IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) In questo caso, il **membro vt** della [**struttura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) contiene il flag **\_ VT DISPATCH/vbObject.** Per accedere all'oggetto COM, chiamare il [**metodo QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia **IDispatch** per ottenere l'interfaccia desiderata.

Un altro tipo di dati restituito dai metodi [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) [**e IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) è dato da dati binari. In questo caso, i dati vengono forniti come matrice contigua di byte e il membro **vt** della struttura [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) conterrà i flag **VT \_ UI1/vbByte** e **VT \_ ARRAY/vbArray.**

> [!Note]  
> Microsoft Visual Basic, Scripting Edition supporta solo matrici [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) e **VARIANT.** Per questo problema, non è possibile usare VBScript per leggere i valori delle proprietà binarie.

 

Molte interfacce ADSI definiscono proprietà specifiche dell'interfaccia. Ad esempio, [**l'interfaccia IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) definisce la [**proprietà Location.**](iadscomputer-property-methods.md) Queste proprietà definite dall'interfaccia possono contenere dati identici a uno degli attributi denominati, ma le proprietà sono specifiche del tipo di oggetto a cui fa riferimento l'interfaccia. Nei linguaggi che supportano l'automazione, è possibile accedere a queste proprietà definite dall'interfaccia usando la notazione del punto, come illustrato nell'esempio di codice seguente.

## <a name="examples"></a>Esempio

L'esempio di codice seguente illustra come accedere alla proprietà ADsPath nell'interfaccia IADs.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



Nei linguaggi non di automazione, i metodi di accesso alle proprietà devono essere usati per accedere alle proprietà definite dall'interfaccia. Ad esempio, il [**metodo IADsComputer::get \_ Location**](iadscomputer-property-methods.md) viene usato per recuperare la **proprietà IADsComputer.Location.**

L'esempio di codice C++ seguente illustra come usare il metodo di accesso alle proprietà in C++ per recuperare il valore ADsPath di un utente.


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



Per altre informazioni sull'accesso agli attributi con ADSI, vedere:

-   [Metodo Get](the-get-method.md)
-   [Metodo GetEx](the-getex-method.md)
-   [Metodo GetInfo](the-getinfo-method.md)
-   [Ottimizzazione tramite GetInfoEx](optimization-using-getinfoex.md)
-   [Accesso agli attributi con l'interfaccia IDirectoryObject](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Codice di esempio per la lettura degli attributi](example-code-for-reading-attributes.md)

 

 