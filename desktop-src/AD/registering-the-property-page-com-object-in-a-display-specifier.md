---
title: Registrazione dell'oggetto COM della pagina delle proprietà in un identificatore di visualizzazione
description: In questo argomento viene illustrato come registrare una DLL di estensione contenente una finestra delle proprietà di Active Directory con il registro di sistema di Windows e Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Registrazione dell'oggetto COM della pagina delle proprietà in un identificatore di visualizzazione Active Directory
- Active Directory oggetto COM della pagina delle proprietà, registrazione in un identificatore di visualizzazione
- identificatori di visualizzazione Active Directory, registrazione dell'oggetto COM della pagina delle proprietà in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5b08ac0ea6329026a6d367e71064bde917b1a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117538"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a><span data-ttu-id="94e55-106">Registrazione dell'oggetto COM della pagina delle proprietà in un identificatore di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="94e55-106">Registering the Property Page COM Object in a Display Specifier</span></span>

<span data-ttu-id="94e55-107">Quando si utilizza COM per creare una DLL di estensione della finestra delle proprietà per Active Directory Domain Services, è necessario registrare l'estensione anche con il registro di sistema di Windows e Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="94e55-107">When you use COM to create a property sheet extension DLL for Active Directory Domain Services, you must also register the extension with the Windows registry and Active Directory Domain Services.</span></span> <span data-ttu-id="94e55-108">La registrazione dell'estensione consente di Active Directory snap-in MMC amministrativi e la shell di Windows per riconoscere l'estensione.</span><span class="sxs-lookup"><span data-stu-id="94e55-108">Registering the extension enables the Active Directory administrative MMC snap-ins and the Windows shell to recognize the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="94e55-109">Registrazione nel registro di sistema di Windows</span><span class="sxs-lookup"><span data-stu-id="94e55-109">Registering in the Windows Registry</span></span>

<span data-ttu-id="94e55-110">Come tutti i server COM, un'estensione della finestra delle proprietà deve essere registrata nel registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="94e55-110">Like all COM servers, a property sheet extension must be registered in the Windows registry.</span></span> <span data-ttu-id="94e55-111">L'estensione viene registrata con la chiave seguente.</span><span class="sxs-lookup"><span data-stu-id="94e55-111">The extension is registered under the following key.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

<span data-ttu-id="94e55-112">*<clsid>* rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="94e55-112">*<clsid>* is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="94e55-113">Sotto la *<clsid>* chiave è presente una chiave **InprocServer32** che identifica l'oggetto come server in-process a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="94e55-113">Under the *<clsid>* key, there is an **InProcServer32** key that identifies the object as a 32-bit in-proc server.</span></span> <span data-ttu-id="94e55-114">Nella chiave **InprocServer32** il percorso della dll viene specificato nel valore predefinito e il modello di Threading viene specificato nel valore **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="94e55-114">Under the **InProcServer32** key, the location of the DLL is specified in the default value and the threading model is specified in the **ThreadingModel** value.</span></span> <span data-ttu-id="94e55-115">Tutte le estensioni della finestra delle proprietà devono utilizzare il modello di threading "Apartment".</span><span class="sxs-lookup"><span data-stu-id="94e55-115">All property sheet extensions must use the "Apartment" threading model.</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="94e55-116">Registrazione con Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="94e55-116">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="94e55-117">La registrazione dell'estensione della finestra delle proprietà è specifica di un'impostazione locale.</span><span class="sxs-lookup"><span data-stu-id="94e55-117">Property sheet extension registration is specific to one locale.</span></span> <span data-ttu-id="94e55-118">Se l'estensione della finestra delle proprietà si applica a tutte le impostazioni locali, deve essere registrata nell'oggetto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) della classe di oggetti in tutti i sottocontenitori delle impostazioni locali nel contenitore degli identificatori di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="94e55-118">If the property sheet extension applies to all locales, it must be registered in the object class [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) object in all of the locale subcontainers in the Display Specifiers container.</span></span> <span data-ttu-id="94e55-119">Se l'estensione della finestra delle proprietà è localizzata per determinate impostazioni locali, registrarla nell'oggetto **displaySpecifier** del sottocontenitore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="94e55-119">If the property sheet extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale subcontainer.</span></span> <span data-ttu-id="94e55-120">Per ulteriori informazioni sul contenitore e le impostazioni locali per gli identificatori di visualizzazione, vedere la pagina relativa agli [identificatori di visualizzazione](display-specifiers.md) e al [contenitore DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="94e55-120">For more information about the Display Specifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="94e55-121">Sono disponibili tre attributi dell'identificatore di visualizzazione in cui è possibile registrare un'estensione della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="94e55-121">There are three display specifier attributes that a property sheet extension can be registered under.</span></span> <span data-ttu-id="94e55-122">Si tratta di [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)e [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span><span class="sxs-lookup"><span data-stu-id="94e55-122">These are [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), and [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span></span>

<span data-ttu-id="94e55-123">L'attributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifica le pagine delle proprietà amministrative da visualizzare in Active Directory snap-in amministrativi. La pagina delle proprietà viene visualizzata quando l'utente visualizza le proprietà degli oggetti della classe appropriata in uno degli snap-in di MMC di amministrazione Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94e55-123">The [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) attribute identifies administrative property pages to display in Active Directory administrative snap-ins. The property page appears when the user views properties for objects of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="94e55-124">L'attributo [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) identifica le pagine delle proprietà degli utenti finali da visualizzare nella shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="94e55-124">The [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attribute identifies end-user property pages to display in the Windows shell.</span></span> <span data-ttu-id="94e55-125">La pagina delle proprietà viene visualizzata quando l'utente visualizza le proprietà degli oggetti della classe appropriata in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="94e55-125">The property page appears when the user views the properties for objects of the appropriate class in the Windows Explorer.</span></span> <span data-ttu-id="94e55-126">A partire dai sistemi operativi Windows Server 2003, la shell di Windows non Visualizza più gli oggetti da Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="94e55-126">Beginning with the Windows Server 2003 operating systems, the Windows shell no longer displays objects from Active Directory Domain Services.</span></span>

<span data-ttu-id="94e55-127">[**AdminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) è disponibile solo nei sistemi operativi Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="94e55-127">The [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) is only available on the Windows Server 2003 operating systems.</span></span> <span data-ttu-id="94e55-128">La pagina delle proprietà viene visualizzata quando l'utente visualizza le proprietà per più di un oggetto della classe appropriata in uno degli snap-in di MMC di amministrazione Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94e55-128">The property page appears when the user views properties for more than one object of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="94e55-129">Tutti questi attributi sono multivalore.</span><span class="sxs-lookup"><span data-stu-id="94e55-129">All of these attributes are multi-valued.</span></span>

<span data-ttu-id="94e55-130">I valori per gli attributi [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) e [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) richiedono il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="94e55-130">The values for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) and [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attributes require the following format.</span></span>


```C++
<order number>,<clsid>,<optional data>
```



<span data-ttu-id="94e55-131">I valori per l'attributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) richiedono il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="94e55-131">The values for the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute require the following format.</span></span>


```C++
<order number>,<clsid>
```



<span data-ttu-id="94e55-132">Il " &lt; numero &gt; di ordine" è un numero senza segno che rappresenta la posizione della pagina nel foglio.</span><span class="sxs-lookup"><span data-stu-id="94e55-132">The "&lt;order number&gt;" is an unsigned number that represents the page position in the sheet.</span></span> <span data-ttu-id="94e55-133">Quando viene visualizzata una finestra delle proprietà, i valori vengono ordinati usando un confronto tra il " &lt; numero di ordine" di ogni valore &gt; .</span><span class="sxs-lookup"><span data-stu-id="94e55-133">When a property sheet is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="94e55-134">Se più di un valore ha lo stesso " &lt; numero &gt; di ordine", gli oggetti COM della pagina delle proprietà vengono caricati nell'ordine in cui vengono letti dal server Active Directory.</span><span class="sxs-lookup"><span data-stu-id="94e55-134">If more than one value has the same "&lt;order number&gt;", those property page COM objects are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="94e55-135">Se possibile, è necessario usare un "numero di ordine" non esistente, &lt; &gt; ovvero uno non usato da altri valori nella proprietà.</span><span class="sxs-lookup"><span data-stu-id="94e55-135">If possible, you should use a non-existing "&lt;order number&gt;"; that is, one not used by other values in the property.</span></span> <span data-ttu-id="94e55-136">Non esiste una posizione di inizio prescritta e sono consentiti gap nella &lt; sequenza "Order Number &gt; ".</span><span class="sxs-lookup"><span data-stu-id="94e55-136">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="94e55-137">" &lt; CLSID &gt; " è la rappresentazione di stringa del CLSID come prodotto dalla funzione [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="94e55-137">The "&lt;clsid&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="94e55-138">" &lt; Dati facoltativi &gt; " è un valore stringa non obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="94e55-138">The "&lt;optional data&gt;" is a string value that is not required.</span></span> <span data-ttu-id="94e55-139">Questo valore può essere recuperato dall'oggetto COM della pagina delle proprietà usando il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passato al metodo [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="94e55-139">This value can be retrieved by the property page COM object using the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to its [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method.</span></span> <span data-ttu-id="94e55-140">L'oggetto COM della pagina delle proprietà ottiene questi dati chiamando [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) con il formato degli Appunti [**\_ DSPROPERTYPAGEINFO di CFSTR**](cfstr-dspropertypageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="94e55-140">The property page COM object obtains this data by calling [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) with the [**CFSTR\_DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) clipboard format.</span></span> <span data-ttu-id="94e55-141">Fornisce un **HGLOBAL** che contiene una struttura [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) la struttura **DSPROPERTYPAGEINFO** contiene una stringa Unicode che contiene i &lt; dati facoltativi &gt; .</span><span class="sxs-lookup"><span data-stu-id="94e55-141">This provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure The **DSPROPERTYPAGEINFO** structure contains a Unicode string that contains the "&lt;optional data&gt;".</span></span> <span data-ttu-id="94e55-142">" &lt; Dati facoltativi &gt; " non consentito con l'attributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .</span><span class="sxs-lookup"><span data-stu-id="94e55-142">The "&lt;optional data&gt;" is not allowed with the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute.</span></span> <span data-ttu-id="94e55-143">Nell'esempio di codice C/C++ riportato di seguito viene illustrato come recuperare i &lt; dati facoltativi &gt; .</span><span class="sxs-lookup"><span data-stu-id="94e55-143">The following C/C++ code example shows how to retrieve the "&lt;optional data&gt;".</span></span>


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



<span data-ttu-id="94e55-144">Un'estensione della finestra delle proprietà può implementare più di una pagina delle proprietà. un possibile utilizzo di " &lt; dati facoltativi &gt; " consiste nel denominare le pagine da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="94e55-144">A property sheet extension can implement more than one property page; one possible use of the "&lt;optional data&gt;" is to name the pages to display.</span></span> <span data-ttu-id="94e55-145">In questo modo si offre la flessibilità di scegliere di implementare più oggetti COM, uno per ogni pagina o un singolo oggetto COM per gestire più pagine.</span><span class="sxs-lookup"><span data-stu-id="94e55-145">This provides the flexibility of choosing to implement multiple COM objects, one for each page, or a single COM object to handle multiple pages.</span></span>

<span data-ttu-id="94e55-146">L'esempio di codice seguente è un valore di esempio che può essere usato per gli attributi [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)o [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .</span><span class="sxs-lookup"><span data-stu-id="94e55-146">The following code example is an example value that can be used for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), or [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attributes.</span></span>


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> <span data-ttu-id="94e55-147">Per la shell di Windows, i dati degli identificatori di visualizzazione vengono recuperati all'accesso dell'utente e memorizzati nella cache per la sessione utente.</span><span class="sxs-lookup"><span data-stu-id="94e55-147">For the Windows shell, display specifier data is retrieved at user logon, and cached for the user session.</span></span> <span data-ttu-id="94e55-148">Per gli snap-in amministrativi, i dati dell'identificatore di visualizzazione vengono recuperati quando lo snap-in viene caricato e viene memorizzato nella cache per la durata del processo.</span><span class="sxs-lookup"><span data-stu-id="94e55-148">For administrative snap-ins, the display specifier data is retrieved when the snap-in is loaded, and is cached for the lifetime of the process.</span></span> <span data-ttu-id="94e55-149">Per la shell di Windows, ciò indica che le modifiche apportate agli identificatori di visualizzazione diventano effettive dopo che un utente si disconnette e quindi si riconnette.</span><span class="sxs-lookup"><span data-stu-id="94e55-149">For the Windows shell, this indicates that changes to display specifiers take effect after a user logs off and then logs on again.</span></span> <span data-ttu-id="94e55-150">Per gli snap-in amministrativi, le modifiche diventano effettive quando viene caricato lo snap-in o il file della console.</span><span class="sxs-lookup"><span data-stu-id="94e55-150">For the administrative snap-ins, changes take effect when the snap-in or console file is loaded.</span></span>

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a><span data-ttu-id="94e55-151">Aggiunta di un valore agli attributi di estensione della finestra delle proprietà</span><span class="sxs-lookup"><span data-stu-id="94e55-151">Adding a Value to the Property Sheet Extension Attributes</span></span>

<span data-ttu-id="94e55-152">Nella procedura riportata di seguito viene descritto come registrare un'estensione della finestra delle proprietà in uno degli attributi di estensione della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="94e55-152">The following procedure describes how to register a property sheet extension under one of the property sheet extension attributes.</span></span>

<span data-ttu-id="94e55-153">**Registrazione di un'estensione della finestra delle proprietà in uno degli attributi di estensione della finestra delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="94e55-153">**Registering a property sheet extension under one of the property sheet extension attributes**</span></span>

1.  <span data-ttu-id="94e55-154">Verificare che l'estensione non esista già nei valori dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="94e55-154">Ensure that the extension does not already exist in the attribute values.</span></span>
2.  <span data-ttu-id="94e55-155">Aggiungere il nuovo valore alla fine dell'elenco di ordini delle pagine delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="94e55-155">Add the new value at the end of the property page ordering list.</span></span> <span data-ttu-id="94e55-156">Imposta la &lt; parte "Order Number &gt; " del valore dell'attributo sul valore successivo dopo il numero di ordine esistente più elevato.</span><span class="sxs-lookup"><span data-stu-id="94e55-156">That is set the "&lt;order number&gt;" portion of the attribute value to the next value after the highest existing order number.</span></span>
3.  <span data-ttu-id="94e55-157">Il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) viene usato per aggiungere il nuovo valore all'attributo.</span><span class="sxs-lookup"><span data-stu-id="94e55-157">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="94e55-158">Il parametro *lnControlCode* deve essere impostato sulla **\_ Proprietà Ads \_ Append** , in modo che il nuovo valore venga aggiunto ai valori esistenti e non sovrascriva quindi i valori esistenti.</span><span class="sxs-lookup"><span data-stu-id="94e55-158">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND** so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="94e55-159">Per eseguire il commit della modifica nella directory, è necessario chiamare il metodo [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) in seguito.</span><span class="sxs-lookup"><span data-stu-id="94e55-159">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called afterward to commit the change to the directory.</span></span>

<span data-ttu-id="94e55-160">Tenere presente che la stessa estensione della finestra delle proprietà può essere registrata per più di una classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="94e55-160">Be aware that the same property sheet extension can be registered for more than one object class.</span></span>

<span data-ttu-id="94e55-161">Il metodo [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) viene usato per aggiungere il nuovo valore all'attributo.</span><span class="sxs-lookup"><span data-stu-id="94e55-161">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="94e55-162">Il parametro *lnControlCode* deve essere impostato sulla **\_ Proprietà Ads \_ Append**, in modo che il nuovo valore venga aggiunto ai valori esistenti e non sovrascriva quindi i valori esistenti.</span><span class="sxs-lookup"><span data-stu-id="94e55-162">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND**, so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="94e55-163">Per eseguire il commit della modifica nella directory, è necessario chiamare il metodo [**IADs:: seinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="94e55-163">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called after to commit the change to the directory.</span></span>

<span data-ttu-id="94e55-164">Nell'esempio di codice seguente viene aggiunta un'estensione della finestra delle proprietà alla classe gruppo nelle impostazioni locali predefinite del computer.</span><span class="sxs-lookup"><span data-stu-id="94e55-164">The following code example adds a property sheet extension to the group class in the computer's default locale.</span></span> <span data-ttu-id="94e55-165">Tenere presente che la funzione **AddPropertyPageToDisplaySpecifier** verifica il CLSID dell'estensione della finestra delle proprietà nei valori esistenti, ottiene il numero di ordine più elevato e aggiunge il valore per la pagina delle proprietà utilizzando [**IADs::P UTEX**](/windows/desktop/api/iads/nf-iads-iads-putex) con la **\_ Proprietà Ads \_ Accoda** il codice di controllo.</span><span class="sxs-lookup"><span data-stu-id="94e55-165">Be aware that the **AddPropertyPageToDisplaySpecifier** function verifies the property sheet extension CLSID in the existing values, gets the highest order number, and adds the value for the property page using [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) with the **ADS\_PROPERTY\_APPEND** control code.</span></span>


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 