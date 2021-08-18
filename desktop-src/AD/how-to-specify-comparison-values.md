---
title: Come specificare i valori di confronto
description: Ogni tipo di attributo ha una sintassi che determina il tipo di valori di confronto che è possibile specificare in un filtro di ricerca per tale attributo.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Come specificare i valori di confronto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5babc7d9781895c9671594214e4e036a85ef951cdb4b97ba34d708d160dd8fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188122"
---
# <a name="how-to-specify-comparison-values"></a>Come specificare i valori di confronto

Ogni tipo di attributo ha una sintassi che determina il tipo di valori di confronto che è possibile specificare in un filtro di ricerca per tale attributo.

Nelle sezioni seguenti vengono descritti i requisiti per la sintassi di ogni attributo. Per altre informazioni sulle sintassi degli attributi, vedere [Sintassi per gli attributi in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean
</dt> <dd>

Il valore specificato in un filtro deve essere un valore stringa "TRUE" o "FALSE". Negli esempi seguenti viene illustrato come specificare una stringa di confronto booleana.

L'esempio seguente cerca gli oggetti con **showInAdvancedViewOnly** impostato su **TRUE:**


```C++
(showInAdvancedViewOnly=TRUE)
```



L'esempio seguente cerca gli oggetti con **showInAdvancedViewOnly** impostato su **FALSE:**


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer ed enumerazione
</dt> <dd>

Il valore specificato in un filtro deve essere un numero intero decimale. I valori esadecimali devono essere convertiti in decimali. Una stringa di confronto dei valori ha il formato seguente:


```C++
<attribute name>:<value>
```



" <attribute name> " è il valore **lDAPDisplayName** dell'attributo e "<value>" è il valore da usare per il confronto.

Nell'esempio di codice seguente viene illustrato un filtro che consente di cercare oggetti con un valore **groupType** uguale al flag **ADS \_ GROUP TYPE UNIVERSAL \_ \_ \_ GROUP** (8) e al flag **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000). I due flag combinati sono uguali 0x80000008, che viene convertito in decimal è 2147483656.


```C++
(groupType=2147483656)
```



Gli operatori delle regole di corrispondenza LDAP possono essere usati anche per eseguire confronti bit per bit. Per altre informazioni sulle regole di corrispondenza, vedere [Sintassi del filtro di ricerca.](/windows/desktop/ADSI/search-filter-syntax) Nell'esempio di codice seguente viene illustrato un filtro che consente di cercare oggetti per i cui valori **groupType** è impostato il bit **ADS \_ GROUP TYPE \_ SECURITY \_ \_ ENABLED** (0x80000000 = 2147483648).


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString
</dt> <dd>

Il valore specificato in un filtro è il numero di dati da trovare. I dati devono essere rappresentati come una stringa di byte con codifica a due caratteri in cui ogni byte è preceduto da una barra rovesciata ( \\ ). Ad esempio, il valore 0x05 verrà visualizzato nella stringa come " \\ 05".

La [**funzione ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) può essere usata per creare una rappresentazione di stringa codificata dei dati binari. La **funzione ADsEncodeBinaryData** non codifica i valori byte che rappresentano caratteri alfanumerici. Il carattere verrà invece inserito nella stringa senza codificarlo. Di seguito viene restituita la stringa contenente una combinazione di caratteri codificati e non codificati. Ad esempio, se i dati binari sono 0x05 0x1A 0x1B 0x43 0x32, la stringa codificata conterrà \| \| " \| \| \\ 05 \\ 1A \\ 1BC2". Questa operazione non ha alcun effetto sul filtro e i filtri di ricerca funzioneranno correttamente con questi tipi di stringhe.

I caratteri jolly vengono accettati.

L'esempio di codice seguente mostra un filtro che contiene una stringa codificata per **schemaIDGUID** con valore GUID "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid
</dt> <dd>

Il valore specificato in un filtro è la rappresentazione della stringa di byte codificata del SID. Per altre informazioni sulle stringhe di byte codificate, vedere la sezione precedente di questo argomento che illustra la sintassi OctetString.

L'esempio di codice seguente mostra un filtro che contiene una stringa codificata per **objectSid** con valore stringa SID "S-1-5-21-1935655697-308236825-1417001333":


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>Dn
</dt> <dd>

È necessario specificare l'intero nome distinto per cui trovare una corrispondenza.

I caratteri jolly non sono accettati.

Tenere presente che **l'attributo objectCategory** consente anche di specificare **lDAPDisplayName** della classe impostata sull'attributo.

L'esempio seguente illustra un filtro che specifica un **membro** che contiene "CN=TestUser,DC=Fabrikam,DC=COM":


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

Il valore specificato in un filtro deve essere un numero intero decimale. Converte i valori esadecimali in decimali.

L'esempio di codice seguente illustra un filtro che specifica un **valore creationTime** impostato su [**UN VALORE FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) "1999-12-31 23:59:59 (UTC/GMT)":


```C++
(creationTime=125911583990000000)
```



Le funzioni seguenti creano un filtro di corrispondenza esatta (=) per un attributo integer di grandi dimensioni e verificano l'attributo nello schema e la relativa sintassi:


```C++
//***************************************************************************
//
//  CheckAttribute()
//
//***************************************************************************

HRESULT CheckAttribute(LPOLESTR szAttribute, LPOLESTR szSyntax)
{
    HRESULT hr = E_FAIL;
    BSTR bstr;
    IADsProperty *pObject = NULL;
    LPWSTR szPrefix = L"LDAP://schema/";
    LPWSTR szPath;
     
    if((!szAttribute) || (!szSyntax))
    {
        return E_POINTER;
    }

    // Allocate a buffer large enough to hold the ADsPath of the attribute.
    szPath = new WCHAR[lstrlenW(szPrefix) + lstrlenW(szAttribute) + 1];
    if(NULL == szPath)
    {
        return E_OUTOFMEMORY;
    }
     
    // Create the ADsPath of the attribute.
    wcscpy_s(szPath, szPrefix);
    wcscat_s(szPath, szAttribute);

    hr = ADsOpenObject( szPath,
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsProperty,
                        (void**)&pObject);
    if(SUCCEEDED(hr)) 
    {
        hr = pObject->get_Syntax(&bstr);
        if (SUCCEEDED(hr)) 
        {
            if (0==lstrcmpiW(bstr, szSyntax)) 
            {
                hr = S_OK;
            }
            else
            {
                hr = S_FALSE;
            }
        }

        SysFreeString(bstr);
    }
    
    if(pObject)
    {
        pObject->Release();
    }

    delete szPath;
    
    return hr;
}

//***************************************************************************
//
//  CreateExactMatchFilterLargeInteger()
//
//***************************************************************************

HRESULT CreateExactMatchFilterLargeInteger( LPOLESTR szAttribute, 
                                            INT64 liValue, 
                                            LPOLESTR *pszFilter)
{
    HRESULT hr = E_FAIL;
     
    if ((!szAttribute) || (!pszFilter))
    {
        return E_POINTER;
    }
     
    // Verify that the attribute exists and has 
    // Integer8 (Large Integer) syntax.
     
    hr = CheckAttribute(szAttribute, L"Integer8");
    if (S_OK == hr) 
    {
        LPWSTR szFormat = L"%s=%I64d";
        LPWSTR szTempFilter = new WCHAR[lstrlenW(szFormat) + lstrlenW(szAttribute) + 20 + 1];

        if(NULL == szTempFilter)
        {
            return E_OUTOFMEMORY;
        }
        
        swprintf_s(szTempFilter, L"%s=%I64d", szAttribute, liValue);
     
        // Allocate buffer for the filter string.
        // Caller must free the buffer using CoTaskMemFree.
        *pszFilter = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (lstrlenW(szTempFilter) + 1));
        if (*pszFilter) 
        {
            wcscpy_s(*pszFilter, szTempFilter);
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        delete szTempFilter;
    }

    return hr;
}
```



</dd> <dt>

<span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString
</dt> <dd>

Gli attributi con queste sintassi devono essere conformi a set di caratteri specifici. Per altre informazioni, vedere [Sintassi per gli attributi in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

Attualmente, Active Directory Domain Services non applicano tali set di caratteri.

Il valore specificato in un filtro è una stringa. Il confronto fa distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime
</dt> <dd>

Il valore specificato in un filtro è una stringa che rappresenta la data nel formato seguente:


```C++
YYYYMMDDHHMMSS.0Z
```



"0Z" indica che l'ora non è differenziale. Tenere presente che il server Active Directory archivia data/ora come ora di Greenwich (GMT). Se non viene specificato un valore differenziale dell'ora, il valore predefinito è GMT.

Se il fuso orario locale non è GMT, usare un valore differenziale per specificare il fuso orario locale e applicarlo a GMT. Il differenziale è basato su: GMT=Local+differential.

Per specificare un differenziale, usare:


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



L'esempio seguente mostra un filtro che specifica un'ora **whenCreated** impostata su 23/3/99 8:52:58 PM GMT:


```C++
(whenCreated=19990323205258.0Z)
```



L'esempio seguente mostra un filtro che specifica **quandoCreated** time impostato su 3/23/99 8:52:58 PM New Zealand Standard Time (differenziale è +12 ore):


```C++
(whenCreated=19990323205258.0+1200)
```



Nell'esempio di codice seguente viene illustrato come calcolare il fuso orario differenziale. La funzione restituisce il differenziale tra il fuso orario locale corrente e GMT. Il valore restituito è una stringa nel formato seguente:


```C++
[+/-]HHMM
```



Ad esempio, l'ora solare Pacifico è -0800.


```C++
//***************************************************************************
//
//  GetLocalTimeZoneDifferential()
//
//***************************************************************************

HRESULT GetLocalTimeZoneDifferential(LPOLESTR *pszDifferential)
{
    if(NULL == pszDifferential)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    DWORD dwReturn;
    TIME_ZONE_INFORMATION timezoneinfo;
    LONG lTimeDifferential;
    LONG lHours;
    LONG lMinutes;
    
    dwReturn  = GetTimeZoneInformation(&timezoneinfo);

    switch (dwReturn)
    {
    case TIME_ZONE_ID_STANDARD:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.StandardBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;

        hr = S_OK;
        break;

    case TIME_ZONE_ID_DAYLIGHT:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.DaylightBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        // Apply the additive inverse.
        // Bias is based on GMT=Local+Bias.
        // A differential, based on GMT=Local-Bias, is required.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;
        
        hr = S_OK;
        break;

    case TIME_ZONE_ID_INVALID:
    default:
        hr = E_FAIL;
        break;
    }
     
    if (SUCCEEDED(hr))
    {
        // The caller must free the memory using CoTaskMemFree.
        *pszDifferential = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (3 + 2 + 1));
        if (*pszDifferential)
        {
            swprintf_s(*pszDifferential, L"%+03d%02d", lHours, lMinutes);
            
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
     
    return hr;
}
```



</dd> <dt>

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime
</dt> <dd>

Il valore specificato in un filtro è una stringa che rappresenta la data nel formato seguente:


```C++
YYMMDDHHMMSSZ
```



Z indica che non sono presenti differenze di tempo. Tenere presente che il server Active Directory archivia data e ora come ora GMT. Se non viene specificato un valore differenziale dell'ora, l'impostazione predefinita è GMT.

Il valore dei secondi ("SS") è facoltativo.

Se GMT non è il fuso orario locale, applicare un valore differenziale locale per specificare il fuso orario locale. Il differenziale è: GMT=Local+differential.

Per specificare un differenziale, usare il formato seguente:


```C++
YYMMDDHHMMSS[+/-]HHMM
```



L'esempio seguente illustra un filtro che specifica un'ora **myTimeAttrib** impostata su 23/3/99 8:52:58 PM GMT:


```C++
(myTimeAttrib=990323205258Z)
```



L'esempio seguente mostra un filtro che specifica un'ora **myTimeAttrib** impostata su 23/3/99 8:52:58 PM senza i secondi specificati:


```C++
(myTimeAttrib=9903232052Z)
```



Nell'esempio seguente viene illustrato un filtro che specifica un'ora **myTimeAttrib** impostata su 23/3/99 8:52:58 PM Ora solare Nuova Zelanda (il differenziale è di 12 ore). Equivale a 23/3/99 8:52:58 GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString
</dt> <dd>

Il valore specificato in un filtro è una stringa. DirectoryString può contenere caratteri Unicode. Il confronto viene eseguito senza distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>Oid
</dt> <dd>

È necessario specificare l'intero OID di cui trovare una corrispondenza.

I caratteri jolly non sono accettati.

**L'attributo objectCategory** consente di specificare **lDAPDisplayName** della classe impostata per l'attributo.

L'esempio seguente illustra un filtro che specifica **governsID per** la classe volume:


```C++
(governsID=1.2.840.113556.1.5.36)
```



Due filtri equivalenti che specificano **l'attributo systemMustContain** contenente **uNCName**, che ha un OID di 1.2.840.113556.1.4.137:


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Altre sintassi
</dt> <dd>

Le sintassi seguenti vengono valutate in un filtro simile a una stringa ottetto:

-   ObjectSecurityDescriptor
-   AccessPointDN
-   PresentationAddresses
-   ReplicaLink
-   DNWithString
-   DNWithOctetString
-   ORName

</dd> </dl>

 

 