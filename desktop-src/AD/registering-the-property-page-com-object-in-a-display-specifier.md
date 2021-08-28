---
title: Registrazione dell'oggetto COM della pagina delle proprietà in un identificatore di visualizzazione
description: Questo argomento illustra come registrare una DLL di estensione che contiene una finestra delle proprietà di Active Directory con il registro Windows e Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Registrazione dell'oggetto COM della pagina delle proprietà in un identificatore di visualizzazione Active Directory
- oggetto COM della pagina delle proprietà Active Directory, registrazione in un identificatore di visualizzazione
- identificatori di visualizzazione Active Directory, registrazione dell'oggetto COM della pagina delle proprietà in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6685e406cb1bfdc16f73dd2fddd94a195fe74a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881239"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>Registrazione dell'oggetto COM della pagina delle proprietà in un identificatore di visualizzazione

Quando si usa COM per creare una DLL di estensione della finestra delle proprietà per Active Directory Domain Services, è necessario registrare anche l'estensione con il registro Windows e Active Directory Domain Services. La registrazione dell'estensione consente agli snap-in mmc amministrativi di Active Directory e Windows shell di riconoscere l'estensione.

## <a name="registering-in-the-windows-registry"></a>Registrazione nel Registro Windows dati

Come tutti i server COM, un'estensione della finestra delle proprietà deve essere registrata nel registro Windows sistema. L'estensione viene registrata nella chiave seguente.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; clsid &gt;* è la rappresentazione di stringa del CLSID come prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) Sotto la *&lt; chiave &gt; clsid* è presente una chiave **InProcServer32** che identifica l'oggetto come server in-process a 32 bit. Nella chiave **InProcServer32** il percorso della DLL viene specificato nel valore predefinito e il modello di threading viene specificato nel **valore ThreadingModel.** Tutte le estensioni della finestra delle proprietà devono usare il modello di threading "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrazione con Active Directory Domain Services

La registrazione dell'estensione della finestra delle proprietà è specifica di un'impostazione locale. Se l'estensione della finestra delle proprietà si applica a tutte le impostazioni locali, deve essere registrata nell'oggetto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) della classe di oggetti in tutti i sottocontenitori delle impostazioni locali nel contenitore Identificatori di visualizzazione. Se l'estensione della finestra delle proprietà è localizzata per determinate impostazioni locali, registrarla nell'oggetto **displaySpecifier** nel sottocontenitore delle impostazioni locali. Per altre informazioni sul contenitore Identificatori di visualizzazione e sulle impostazioni locali, vedere [Identificatori di visualizzazione](display-specifiers.md) e [Contenitore DisplaySpecifiers](displayspecifiers-container.md).

Esistono tre attributi dell'identificatore di visualizzazione in cui è possibile registrare un'estensione della finestra delle proprietà. Si tratta [**di adminPropertyPages,**](/windows/desktop/ADSchema/a-adminpropertypages) [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)e [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).

[**L'attributo adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifica le pagine delle proprietà amministrative da visualizzare negli snap-in amministrativi di Active Directory. La pagina delle proprietà viene visualizzata quando l'utente visualizza le proprietà per gli oggetti della classe appropriata in uno degli snap-in MMC amministrativi di Active Directory.

[**L'attributo shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) identifica le pagine delle proprietà dell'utente finale da visualizzare nella Windows shell. La pagina delle proprietà viene visualizzata quando l'utente visualizza le proprietà per gli oggetti della classe appropriata nel Windows Explorer. A partire dai sistemi operativi Windows Server 2003, la shell Windows non visualizza più gli oggetti Active Directory Domain Services.

[**AdminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) è disponibile solo nei sistemi operativi Windows Server 2003. La pagina delle proprietà viene visualizzata quando l'utente visualizza le proprietà di più oggetti della classe appropriata in uno degli snap-in MMC amministrativi di Active Directory.

Tutti questi attributi sono multivalore.

I valori per gli [**attributi adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) [**e shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) richiedono il formato seguente.


```C++
<order number>,<clsid>,<optional data>
```



I valori per [**l'attributo adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) richiedono il formato seguente.


```C++
<order number>,<clsid>
```



Il " &lt; numero di ordine " è un numero senza segno che rappresenta la posizione della pagina nel &gt; foglio. Quando viene visualizzata una finestra delle proprietà, i valori vengono ordinati usando un confronto del " numero di ordine" &lt; di ogni &gt; valore. Se più valori hanno lo stesso " numero di ordine ", gli oggetti COM della pagina delle proprietà vengono caricati nell'ordine in cui vengono letti &lt; &gt; dal server Active Directory. Se possibile, è consigliabile usare un " numero di ordine " non esistente, cio' non usato da &lt; altri valori nella proprietà &gt; . Non è stata specificata alcuna posizione iniziale e sono consentiti spazi nella sequenza " &lt; numero di &gt; ordine ".

" &lt; clsid " è la rappresentazione di stringa &gt; del CLSID come prodotto dalla [**funzione StringFromCLSID.**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)

" &lt; dati &gt; facoltativi " è un valore stringa che non è obbligatorio. Questo valore può essere recuperato dall'oggetto COM della pagina delle proprietà usando il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passato al relativo [**metodo IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) L'oggetto COM della pagina delle proprietà ottiene questi dati chiamando [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) con il formato degli Appunti [**CFSTR \_ DSPROPERTYPAGEINFO.**](cfstr-dspropertypageinfo.md) Fornisce un **HGLOBAL** che contiene una struttura [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) La struttura **DSPROPERTYPAGEINFO** contiene una stringa Unicode che contiene i " &lt; dati &gt; facoltativi ". I " &lt; dati &gt; facoltativi " non sono consentiti con l'attributo [**adminMultiselectPropertyPages.**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) Nell'esempio di codice C/C++ seguente viene illustrato come recuperare i " &lt; dati facoltativi &gt; ".


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



Un'estensione della finestra delle proprietà può implementare più di una pagina delle proprietà. un possibile uso dei " &lt; dati &gt; facoltativi " è assegnare un nome alle pagine da visualizzare. In questo modo è possibile scegliere di implementare più oggetti COM, uno per ogni pagina o un singolo oggetto COM per gestire più pagine.

L'esempio di codice seguente è un valore di esempio che può essere usato per gli attributi [**adminPropertyPages,**](/windows/desktop/ADSchema/a-adminpropertypages) [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)o [**adminMultiselectPropertyPages.**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages)


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> Per la Windows shell, i dati dell'identificatore di visualizzazione vengono recuperati all'accesso utente e memorizzati nella cache per la sessione utente. Per gli snap-in amministrativi, i dati dell'identificatore di visualizzazione vengono recuperati al caricamento dello snap-in e vengono memorizzati nella cache per la durata del processo. Per la Windows shell, ciò indica che le modifiche apportate agli identificatori di visualizzazione vengono applicate dopo che un utente si disconnette e quindi accede di nuovo. Per gli snap-in amministrativi, le modifiche vengono applicate quando viene caricato lo snap-in o il file della console.

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>Aggiunta di un valore agli attributi di estensione della finestra delle proprietà

La procedura seguente descrive come registrare un'estensione della finestra delle proprietà in uno degli attributi di estensione della finestra delle proprietà.

**Registrazione di un'estensione della finestra delle proprietà in uno degli attributi di estensione della finestra delle proprietà**

1.  Assicurarsi che l'estensione non esista già nei valori dell'attributo.
2.  Aggiungere il nuovo valore alla fine dell'elenco di ordinamento della pagina delle proprietà. Viene impostata la parte " order number " del valore dell'attributo &lt; sul valore successivo dopo il numero di ordine esistente più &gt; alto.
3.  Il [**metodo IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) viene usato per aggiungere il nuovo valore all'attributo. Il *parametro lnControlCode* deve essere impostato su **ADS PROPERTY \_ \_ APPEND** in modo che il nuovo valore sia aggiunto ai valori esistenti e non sovrascriva quindi i valori esistenti. Il [**metodo IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) deve essere chiamato successivamente per eseguire il commit della modifica nella directory.

Tenere presente che la stessa estensione della finestra delle proprietà può essere registrata per più di una classe di oggetti.

Il [**metodo IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) viene usato per aggiungere il nuovo valore all'attributo. Il *parametro lnControlCode* deve essere impostato su **ADS PROPERTY \_ \_ APPEND,** in modo che il nuovo valore sia aggiunto ai valori esistenti e non sovrascriva quindi i valori esistenti. Il [**metodo IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) deve essere chiamato dopo per eseguire il commit della modifica nella directory.

Nell'esempio di codice seguente viene aggiunta un'estensione della finestra delle proprietà alla classe group nelle impostazioni locali predefinite del computer. Tenere presente che la funzione **AddPropertyPageToDisplaySpecifier** verifica il CLSID dell'estensione della finestra delle proprietà nei valori esistenti, ottiene il numero di ordine più alto e aggiunge il valore per la pagina delle proprietà usando [**IADs::P utEx**](/windows/desktop/api/iads/nf-iads-iads-putex) con il codice di controllo **ADS \_ PROPERTY \_ APPEND.**


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



 

 
