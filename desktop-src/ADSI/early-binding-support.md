---
title: Supporto per l'associazione anticipata
description: Nell'esempio di codice riportato di seguito viene presentato uno scenario con il supporto dell'associazione anticipata.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, supporto per l'associazione anticipata
- Binding AD, supporto dell'associazione anticipata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118450"
---
# <a name="early-binding-support"></a><span data-ttu-id="93503-105">Supporto per l'associazione anticipata</span><span class="sxs-lookup"><span data-stu-id="93503-105">Early Binding Support</span></span>

<span data-ttu-id="93503-106">Nell'esempio di codice riportato di seguito viene presentato uno scenario con il supporto dell'associazione anticipata.</span><span class="sxs-lookup"><span data-stu-id="93503-106">The following code example presents a scenario with early binding support in place.</span></span>


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



<span data-ttu-id="93503-107">In questo esempio di codice due componenti di estensione estendono un oggetto **utente** .</span><span class="sxs-lookup"><span data-stu-id="93503-107">In this code example, two extension components extend a **user** object.</span></span> <span data-ttu-id="93503-108">Ogni estensione pubblica una propria interfaccia.</span><span class="sxs-lookup"><span data-stu-id="93503-108">Each extension publishes its own interface.</span></span> <span data-ttu-id="93503-109">Ogni estensione non riconosce l'altra interfaccia di estensione. solo ADSI riconosce l'esistenza di entrambe le estensioni.</span><span class="sxs-lookup"><span data-stu-id="93503-109">Each extension does not recognize the other extension interface; only ADSI recognizes the existence of both extensions.</span></span> <span data-ttu-id="93503-110">Ogni estensione delega la relativa [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) a ADSI.</span><span class="sxs-lookup"><span data-stu-id="93503-110">Each extension delegates its [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to ADSI.</span></span> <span data-ttu-id="93503-111">ADSI funge da aggregatore per entrambe le estensioni e per qualsiasi altra estensione futura.</span><span class="sxs-lookup"><span data-stu-id="93503-111">ADSI acts as an aggregator for both extensions, and any other future extensions.</span></span> <span data-ttu-id="93503-112">L'esecuzione di query su un'interfaccia da qualsiasi estensione o da ADSI produce lo stesso risultato coerente.</span><span class="sxs-lookup"><span data-stu-id="93503-112">Querying an interface from any extension, or from ADSI, yields the same consistent result.</span></span>

<span data-ttu-id="93503-113">Nella procedura riportata di seguito viene descritto come creare un'estensione.</span><span class="sxs-lookup"><span data-stu-id="93503-113">The following procedure describes how to create an extension.</span></span>

## <a name="step-1-add-aggregation-to-your-component"></a><span data-ttu-id="93503-114">Passaggio 1: aggiungere l'aggregazione al componente</span><span class="sxs-lookup"><span data-stu-id="93503-114">Step 1: Add Aggregation to Your Component</span></span>

<span data-ttu-id="93503-115">Seguire la specifica COM per aggiungere l'aggregazione al componente.</span><span class="sxs-lookup"><span data-stu-id="93503-115">Follow the COM specification for adding aggregation to your component.</span></span> <span data-ttu-id="93503-116">In breve, è necessario accettare le richieste *pUnknown* al componente durante la **CreateInstance** e delegare il *pUnknown* a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) di aggregator se il componente è aggregato.</span><span class="sxs-lookup"><span data-stu-id="93503-116">In summary, you must accept the *pUnknown* requests to your component during **CreateInstance**, and delegate the *pUnknown* to the aggregator's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) if the component is aggregated.</span></span>

## <a name="step-2-register-your-extension"></a><span data-ttu-id="93503-117">Passaggio 2: registrare l'estensione</span><span class="sxs-lookup"><span data-stu-id="93503-117">Step 2: Register Your Extension</span></span>

<span data-ttu-id="93503-118">A questo punto è necessario decidere quale classe di directory estendere.</span><span class="sxs-lookup"><span data-stu-id="93503-118">Now you must decide which directory class to extend.</span></span> <span data-ttu-id="93503-119">Per eseguire questa operazione, è possibile utilizzare le stesse interfacce per un'interfaccia ADSI, ad esempio [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="93503-119">You cannot use the same interfaces to accomplish this that you would use for an ADSI interface, for example, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span></span> <span data-ttu-id="93503-120">Gli oggetti directory vengono mantenuti nella directory, mentre l'estensione e ADSI sono in esecuzione nel computer client.</span><span class="sxs-lookup"><span data-stu-id="93503-120">Directory objects are persisted in the directory, while your extension and ADSI are running on the client computer.</span></span> <span data-ttu-id="93503-121">Gli esempi di oggetti directory sono **User**, **computer**, **PrintQueue**, **serviceConnectionPoint** e **nTDSService**.</span><span class="sxs-lookup"><span data-stu-id="93503-121">Directory object examples are **user**, **computer**, **printQueue**, **serviceConnectionPoint**, and **nTDSService**.</span></span> <span data-ttu-id="93503-122">È possibile aggiungere una nuova classe in Active Directory e creare anche una nuova estensione per questa nuova classe.</span><span class="sxs-lookup"><span data-stu-id="93503-122">You can add a new class in Active Directory and create a new extension for this new class as well.</span></span>

<span data-ttu-id="93503-123">Usare le chiavi del registro di sistema per associare un nome di classe di directory ai componenti dell'estensione ADSI.</span><span class="sxs-lookup"><span data-stu-id="93503-123">You use registry keys to associate a directory class name with the ADSI extension components.</span></span> <span data-ttu-id="93503-124">La figura seguente rappresenta il layout del registro di sistema esistente, così come le nuove chiavi.</span><span class="sxs-lookup"><span data-stu-id="93503-124">The following figure represents the existing registry layout, as a well as new keys.</span></span>

-   <span data-ttu-id="93503-125">Una nuova chiave, denominata **Extensions**, contiene un elenco di chiavi, ognuna delle quali rappresenta una classe nella directory.</span><span class="sxs-lookup"><span data-stu-id="93503-125">A new key, called **Extensions**, contains a list of keys, each of which represents a class in the directory.</span></span> <span data-ttu-id="93503-126">Ogni classe, ad esempio **User**, **PrintQueue** o **computer**, gestisce un elenco di sottochiavi.</span><span class="sxs-lookup"><span data-stu-id="93503-126">Each class, for example, **user**, **printQueue**, or **computer**, maintains a list of subkeys.</span></span>
-   <span data-ttu-id="93503-127">Ogni sottochiave contiene il CLSID del componente di estensione ADSI.</span><span class="sxs-lookup"><span data-stu-id="93503-127">Each subkey contains the CLSID of the ADSI extension component.</span></span>
-   <span data-ttu-id="93503-128">Ogni sottochiave CLSID contiene una voce di stringa che consente più valori.</span><span class="sxs-lookup"><span data-stu-id="93503-128">Each CLSID subkey contains a string entry that allows multiple values.</span></span> <span data-ttu-id="93503-129">È consigliabile elencare solo le interfacce che fanno parte dell'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="93503-129">You should only list the interfaces that participate in the aggregation.</span></span>

> [!Note]  
> <span data-ttu-id="93503-130">Gli oggetti di estensione sono ancora necessari per registrare le chiavi COM standard.</span><span class="sxs-lookup"><span data-stu-id="93503-130">Extension objects are still required to register standard COM keys.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a><span data-ttu-id="93503-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="93503-131">Example</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

<span data-ttu-id="93503-132">L'elenco di interfacce da extension1 può essere diverso da quello di extension2.</span><span class="sxs-lookup"><span data-stu-id="93503-132">The list of interfaces from Extension1 can be different from that of Extension2.</span></span> <span data-ttu-id="93503-133">L'oggetto, quando attivo, supporta le interfacce di Aggregator (ADSI) e tutte le interfacce fornite dagli extension1 e extension2 dell'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="93503-133">The object, when active, supports the interfaces of the aggregator (ADSI) and all the interfaces provided by the aggregate's Extension1 and Extension2.</span></span> <span data-ttu-id="93503-134">La risoluzione delle interfacce in conflitto (la stessa interfaccia supportata sia da aggregator che da aggregazioni o da più aggregazioni) è determinata dalle priorità delle estensioni.</span><span class="sxs-lookup"><span data-stu-id="93503-134">Resolution of conflicting interfaces (the same interface supported by both the aggregator and the aggregates or by multiple aggregates) is determined by priorities of the extensions.</span></span>

<span data-ttu-id="93503-135">È anche possibile associare l'estensione CLSID a più nomi di classi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="93503-135">You can also associate your CLSID extension with multiple object class names.</span></span> <span data-ttu-id="93503-136">Ad esempio, l'estensione può estendere sia gli oggetti **utente** che quelli di **contatto** .</span><span class="sxs-lookup"><span data-stu-id="93503-136">For example, your extension can extend both the **user** and **contact** objects.</span></span>

> [!Note]  
> <span data-ttu-id="93503-137">Il comportamento dell'estensione viene aggiunto in una classe per oggetto, non in un'istanza per oggetto.</span><span class="sxs-lookup"><span data-stu-id="93503-137">Extension behavior is added on a per-object class, not on a per-object instance.</span></span>

 

<span data-ttu-id="93503-138">Come procedura consigliata, registrare le estensioni, come qualsiasi altro componente COM, con una chiamata alla funzione **DllRegisterSvr** .</span><span class="sxs-lookup"><span data-stu-id="93503-138">As a best practice, register your extensions, as you would any other COM components, with a call to the **DllRegisterSvr** function.</span></span> <span data-ttu-id="93503-139">Fornire anche una funzionalità per annullare la registrazione dell'estensione con la funzione **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="93503-139">Also provide a facility to unregister your extension with the **DllUnregisterServer** function.</span></span>

<span data-ttu-id="93503-140">Nell'esempio di codice seguente viene illustrato come registrare un'estensione.</span><span class="sxs-lookup"><span data-stu-id="93503-140">The following code example shows how to register an extension.</span></span>


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 