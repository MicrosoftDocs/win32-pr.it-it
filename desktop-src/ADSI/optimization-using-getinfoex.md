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
# <a name="optimization-using-getinfoex"></a><span data-ttu-id="afafb-106">Ottimizzazione con GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="afafb-106">Optimization Using GetInfoEx</span></span>

<span data-ttu-id="afafb-107">Il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) viene usato per caricare valori di attributo specifici nella cache locale dal servizio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="afafb-107">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method is used to load specific attribute values into the local cache from the underlying directory service.</span></span> <span data-ttu-id="afafb-108">Questo metodo carica solo i valori di attributo specificati nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="afafb-108">This method only loads the specified attribute values into the local cache.</span></span> <span data-ttu-id="afafb-109">Il metodo [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) viene usato per caricare tutti i valori di attributo nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="afafb-109">The [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is used to load all attribute values into the local cache.</span></span>

<span data-ttu-id="afafb-110">Il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) ottiene valori correnti specifici per le proprietà di un oggetto Active Directory dall'archivio directory sottostante, aggiornando i valori memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="afafb-110">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method gets specific current values for the properties of an Active Directory object from the underlying directory store, refreshing the cached values.</span></span>

<span data-ttu-id="afafb-111">Se un valore esiste già nella cache delle proprietà, tuttavia, la chiamata al metodo [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs. GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) senza prima chiamare [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) per tale attributo recupererà il valore memorizzato nella cache anziché il valore più attuale dalla directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="afafb-111">If a value already exists in the property cache, however, calling the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) method without first calling [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) for that attribute will retrieve the cached value rather than the most current value from the underlying directory.</span></span> <span data-ttu-id="afafb-112">Questo può causare la sovrascrittura dei valori degli attributi aggiornati se la cache locale è stata modificata, ma non è stato eseguito il commit dei valori nel servizio directory sottostante con una chiamata al metodo [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="afafb-112">This can cause updated attribute values to be overwritten if the local cache has been modified, but the values have not been committed to the underlying directory service with a call to the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span> <span data-ttu-id="afafb-113">Il metodo consigliato per evitare problemi di memorizzazione nella cache consiste nell'eseguire sempre il commit delle modifiche dei valori di attributo chiamando **IADs. seinfo** prima di chiamare [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span><span class="sxs-lookup"><span data-stu-id="afafb-113">The suggested method for avoiding caching problems is to always commit attribute value changes by calling **IADs.SetInfo** before calling [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).</span></span>


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



## <a name="retrieving-active-directory-constructed-attributes"></a><span data-ttu-id="afafb-114">Recupero di attributi Active Directory costruiti</span><span class="sxs-lookup"><span data-stu-id="afafb-114">Retrieving Active Directory Constructed Attributes</span></span>

<span data-ttu-id="afafb-115">In Active Directory la maggior parte degli attributi costruiti viene recuperata e memorizzata nella cache quando viene chiamato il metodo [**IADs. GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ([**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) esegue una chiamata **IADs. GetInfo** implicita se la cache è vuota).</span><span class="sxs-lookup"><span data-stu-id="afafb-115">In Active Directory, most of the constructed attributes are retrieved and cached when the [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) performs an implicit **IADs.GetInfo** call if the cache is empty).</span></span> <span data-ttu-id="afafb-116">Alcuni attributi costruiti, tuttavia, non vengono recuperati automaticamente e memorizzati nella cache e pertanto richiedono che il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) venga chiamato in modo esplicito per recuperarli.</span><span class="sxs-lookup"><span data-stu-id="afafb-116">Some constructed attributes, however, are not automatically retrieved and cached and, therefore, require that the [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method be called explicitly to retrieve them.</span></span> <span data-ttu-id="afafb-117">Ad esempio, in Active Directory, l'attributo [**CanonicalName**](/windows/desktop/ADSchema/a-canonicalname) non viene recuperato quando viene chiamato il metodo **IADs. GetInfo** e **IADs. Get** restituirà **la \_ proprietà e Ads \_ non è \_ \_ stata trovata**.</span><span class="sxs-lookup"><span data-stu-id="afafb-117">For example, in Active Directory, the [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) attribute is not retrieved when the **IADs.GetInfo** method is called and **IADs.Get** will return **E\_ADS\_PROPERTY\_NOT\_FOUND**.</span></span> <span data-ttu-id="afafb-118">Per recuperare l'attributo **CanonicalName** , è necessario chiamare il metodo **IADs. GetInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="afafb-118">The **IADs.GetInfoEx** method must be called to retrieve the **canonicalName** attribute.</span></span> <span data-ttu-id="afafb-119">Questi stessi attributi costruiti non verranno recuperati anche tramite l'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) per enumerare gli attributi.</span><span class="sxs-lookup"><span data-stu-id="afafb-119">These same constructed attributes will also not be retrieved using the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface to enumerate the attributes.</span></span>

<span data-ttu-id="afafb-120">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come recuperare tutti i valori di attributo, vedere [codice di esempio per la lettura di un attributo costruito](example-code-for-reading-a-constructed-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="afafb-120">For more information and a code example that shows how to retrieve all attribute values, see [Example Code for Reading a Constructed Attribute](example-code-for-reading-a-constructed-attribute.md).</span></span>

 

 