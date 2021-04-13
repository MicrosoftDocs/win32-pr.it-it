---
title: Ottimizzazione con GetInfoEx
description: Utilizzato per caricare valori di attributo specifici nella cache locale dal servizio directory sottostante.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Ottimizzazione con GetInfoEx ADSI
- GetInfoEx ADSI, ottimizzazione con IADs GetInfoEx
- ADSI ADSI, uso, ottimizzazione con il metodo IADs GetInfoEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339231"
---
# <a name="optimization-using-getinfoex"></a>Ottimizzazione con GetInfoEx

Il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) viene usato per caricare valori di attributo specifici nella cache locale dal servizio directory sottostante. Questo metodo carica solo i valori di attributo specificati nella cache locale. Il metodo [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) viene usato per caricare tutti i valori di attributo nella cache locale.

Il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) ottiene valori correnti specifici per le proprietà di un oggetto Active Directory dall'archivio directory sottostante, aggiornando i valori memorizzati nella cache.

Se un valore esiste già nella cache delle proprietà, tuttavia, la chiamata al metodo [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) senza prima chiamare [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) per tale attributo recupererà il valore memorizzato nella cache anziché il valore più attuale dalla directory sottostante. Questo può causare la sovrascrittura dei valori degli attributi aggiornati se la cache locale è stata modificata, ma non è stato eseguito il commit dei valori nel servizio directory sottostante con una chiamata al metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Il metodo consigliato per evitare problemi di memorizzazione nella cache consiste nell'eseguire sempre il commit delle modifiche dei valori di attributo chiamando **IADs. seinfo** prima di chiamare [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a>Recupero di attributi Active Directory costruiti

In Active Directory la maggior parte degli attributi costruiti viene recuperata e memorizzata nella cache quando viene chiamato il metodo [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ([**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) esegue una chiamata **IADs. GetInfo** implicita se la cache è vuota). Alcuni attributi costruiti, tuttavia, non vengono recuperati automaticamente e memorizzati nella cache e pertanto richiedono che il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) venga chiamato in modo esplicito per recuperarli. Ad esempio, in Active Directory, l'attributo [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname) non viene recuperato quando viene chiamato il metodo **IADs. GetInfo** e **IADs. Get** restituirà **la \_ proprietà e Ads \_ non è \_ \_ stata trovata**. Per recuperare l'attributo **CanonicalName** , è necessario chiamare il metodo **IADs. GetInfoEx** . Questi stessi attributi costruiti non verranno recuperati anche tramite l'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) per enumerare gli attributi.

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come recuperare tutti i valori di attributo, vedere [codice di esempio per la lettura di un attributo costruito](example-code-for-reading-a-constructed-attribute.md).

 

 