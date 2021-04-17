---
title: Accesso agli attributi con ADSI
description: I metodi IADs. Get e IADs. GetEx vengono usati per recuperare i valori degli attributi denominati.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Attributi, accesso con ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300425"
---
# <a name="accessing-attributes-with-adsi"></a>Accesso agli attributi con ADSI

I metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) vengono usati per recuperare i valori degli attributi denominati. Entrambi i metodi restituiscono un valore [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Questi metodi sono disponibili solo per le directory che supportano uno schema. Quando si accede a oggetti in una directory senza uno schema, è necessario utilizzare le interfacce [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) per modificare i valori degli attributi.

I metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) restituiscono una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) che può, o meno, essere una matrice **Variant** a seconda del numero di valori restituiti dal server. Se, ad esempio, dal server viene restituito un solo valore, indipendentemente dal fatto che si tratti di un attributo singolo o multivalore, il metodo restituisce una singola **variante**. Viceversa, se vengono restituiti più valori, viene restituita una matrice **Variant** . Se viene restituita una matrice **Variant** , il membro **VT** della struttura **Variant** contiene i flag **VT \_ Variant/vbVariant** e **VT \_ Array/VBArray** .

I metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) possono anche restituire un oggetto com usando l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . In questo caso, il membro **VT** della struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contiene il flag **di \_ invio/vbObject del VT** . Per accedere all'oggetto COM, chiamare il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sull'interfaccia **IDispatch** per ottenere l'interfaccia desiderata.

Un altro tipo di dati restituito dai metodi [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) è dati binari. In questo caso, i dati vengono forniti come matrice contigua di byte e il membro **VT** della struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) conterrà i flag **VT \_ Ui1/vbByte** e **VT \_ Array/VBArray** .

> [!Note]  
> Microsoft Visual Basic, Scripting Edition supporta solo [](/windows/win32/api/oaidl/ns-oaidl-variant) matrici Variant **e Variant.** Per questo motivo, non è possibile usare VBScript per leggere i valori delle proprietà binarie.

 

Molte interfacce ADSI definiscono proprietà specifiche dell'interfaccia. Ad esempio, l'interfaccia [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) definisce la proprietà [**location**](iadscomputer-property-methods.md) . Queste proprietà definite dall'interfaccia possono contenere dati identici a uno degli attributi denominati, ma le proprietà sono specifiche per il tipo di oggetto a cui fa riferimento l'interfaccia. Nei linguaggi che supportano l'automazione, è possibile accedere a queste proprietà definite dall'interfaccia usando la notazione del punto, come illustrato nell'esempio di codice seguente.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente viene illustrato come accedere alla proprietà ADsPath nell'interfaccia IADs.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



Nei linguaggi non di automazione, è necessario utilizzare i metodi di accesso alle proprietà per accedere alle proprietà definite dall'interfaccia. Ad esempio, il metodo [**IADsComputer:: Get \_ location**](iadscomputer-property-methods.md) viene usato per recuperare la proprietà **IADSComputer. location** .

Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare il metodo di accesso alle proprietà in C++ per recuperare il ADsPath di un utente.


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



Per ulteriori informazioni sull'accesso agli attributi con ADSI, vedere:

-   [Metodo Get](the-get-method.md)
-   [Metodo GetEx](the-getex-method.md)
-   [Metodo GetInfo](the-getinfo-method.md)
-   [Ottimizzazione con GetInfoEx](optimization-using-getinfoex.md)
-   [Accesso agli attributi con l'interfaccia IDirectoryObject](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Codice di esempio per la lettura degli attributi](example-code-for-reading-attributes.md)

 

 