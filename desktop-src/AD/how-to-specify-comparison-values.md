---
title: Come specificare i valori di confronto
description: Ogni tipo di attributo presenta una sintassi che determina il tipo di valori di confronto che è possibile specificare in un filtro di ricerca per tale attributo.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Come specificare i valori di confronto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f9355bc4853fa6dc62645e1c241d8e26f731f9
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724490"
---
# <a name="how-to-specify-comparison-values"></a>Come specificare i valori di confronto

Ogni tipo di attributo presenta una sintassi che determina il tipo di valori di confronto che è possibile specificare in un filtro di ricerca per tale attributo.

Nelle sezioni seguenti vengono descritti i requisiti per ogni sintassi di attributo. Per ulteriori informazioni sulle sintassi degli attributi, vedere [sintassi per gli attributi in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean
</dt> <dd>

Il valore specificato in un filtro deve essere un valore stringa "TRUE" o "FALSE". Negli esempi seguenti viene illustrato come specificare una stringa di confronto booleana.

Nell'esempio seguente vengono cercati gli oggetti con **showInAdvancedViewOnly** impostato su **true**:


```C++
(showInAdvancedViewOnly=TRUE)
```



Nell'esempio seguente vengono cercati gli oggetti il cui **showInAdvancedViewOnly** è impostato su **false**:


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer ed enumerazione
</dt> <dd>

Il valore specificato in un filtro deve essere un numero intero decimale. I valori esadecimali devono essere convertiti in decimali. Una stringa di confronto dei valori assume il formato seguente:


```C++
<attribute name>:<value>
```



" <attribute name> " è l' **ldapDisplayName** dell'attributo e "<value>"è il valore da usare per il confronto.

Nell'esempio di codice seguente viene illustrato un filtro che consente di cercare oggetti con un valore **GroupType** uguale al tipo di **\_ gruppo Ads \_ \_ \_** (8) flag e il flag 0x80000000 ( **Ads \_ Group \_ \_ Security \_ Enabled** ). I due flag combinati uguale a 0x80000008, che è stato convertito in Decimal è 2147483656.


```C++
(groupType=2147483656)
```



Gli operatori della regola di corrispondenza LDAP possono essere usati anche per eseguire confronti bit per bit. Per altre informazioni sulle regole di corrispondenza, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax). Nell'esempio di codice riportato di seguito viene illustrato un filtro che consente di cercare gli oggetti con un **GroupType** con il set di bit **\_ \_ \_ Security \_ Enabled** (0x80000000 = 2147483648) del gruppo ads.


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString
</dt> <dd>

Il valore specificato in un filtro è costituito dai dati da trovare. I dati devono essere rappresentati come una stringa di byte con codifica a due caratteri, in cui ogni byte è preceduto da una barra rovesciata ( \) . Ad esempio, il valore 0x05 verrà visualizzato nella stringa come " \\ 05".

La funzione [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) può essere utilizzata per creare una rappresentazione di stringa codificata di dati binari. La funzione **ADsEncodeBinaryData** non codifica i valori di byte che rappresentano caratteri alfanumerici. Verrà invece inserito il carattere nella stringa senza codificarlo. In questo modo si ottiene la stringa che contiene una combinazione di caratteri codificati e non codificati. Se, ad esempio, i dati binari sono 0x05 \| 0x1A \| 0x1B \| 0x43 \| 0x32, la stringa codificata conterrà " \\ 05 \\ 1a \\ 1BC2". Questa operazione non ha alcun effetto sul filtro e i filtri di ricerca funzioneranno correttamente con questi tipi di stringhe.

I caratteri jolly sono accettati.

Nell'esempio di codice seguente viene illustrato un filtro che contiene una stringa codificata per **schemaIDGUID** con il valore GUID "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>SID
</dt> <dd>

Il valore specificato in un filtro è la rappresentazione di stringa di byte codificata del SID. Per ulteriori informazioni sulle stringhe di byte codificate, vedere la sezione precedente in questo argomento che illustra la sintassi di OctetString.

Nell'esempio di codice seguente viene illustrato un filtro che contiene una stringa codificata per **objectSID** con il valore della stringa SID "S-1-5-21-1935655697-308236825-1417001333":


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>DN
</dt> <dd>

È necessario specificare l'intero nome distinto, per cui trovare una corrispondenza.

I caratteri jolly non sono accettati.

Tenere presente che l'attributo **objectCategory** consente inoltre di specificare il **ldapDisplayName** della classe impostata sull'attributo.

Nell'esempio seguente viene illustrato un filtro che specifica un **membro** che contiene "CN = TESTUSER, DC = Fabrikam, DC = com":


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

Il valore specificato in un filtro deve essere un numero intero decimale. Converte i valori esadecimali in decimali.

Nell'esempio di codice seguente viene illustrato un filtro che specifica un **creationTime** impostato su un [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) di "1999-12-31 23:59:59 (UTC/GMT)":


```C++
(creationTime=125911583990000000)
```



Le funzioni seguenti creano un filtro di corrispondenza esatta (=) per un attributo Integer di grandi dimensioni e verificano l'attributo nello schema e la relativa sintassi:


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

Gli attributi con queste sintassi devono rispettare set di caratteri specifici. Per ulteriori informazioni, vedere [sintassi per gli attributi in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

Attualmente, Active Directory Domain Services non applicano i set di caratteri.

Il valore specificato in un filtro è una stringa. Il confronto fa distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime
</dt> <dd>

Il valore specificato in un filtro è una stringa che rappresenta la data nel formato seguente:


```C++
YYYYMMDDHHMMSS.0Z
```



"0Z" indica nessun differenziale temporale. Tenere presente che il server di Active Directory archivia data/ora come ora di Greenwich (GMT). Se non viene specificato un valore differenziale per l'ora, il valore predefinito è GMT.

Se il fuso orario locale non è GMT, usare un valore differenziale per specificare il fuso orario locale e applicare il differenziale a GMT. Il differenziale si basa su: GMT = local + differenziale.

Per specificare un valore differenziale, usare:


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



Nell'esempio seguente viene illustrato un filtro che specifica un **DataCreazione** tempo impostato su 3/23/99 8:52:58 PM GMT:


```C++
(whenCreated=19990323205258.0Z)
```



Nell'esempio riportato di seguito viene illustrato un filtro che specifica un'ora di **DataCreazione** impostata su 3/23/99 8:52:58 PM Nuova Zelanda standard time (differenziale è + 12 ore):


```C++
(whenCreated=19990323205258.0+1200)
```



Nell'esempio di codice riportato di seguito viene illustrato come calcolare il differenziale del fuso orario. La funzione restituisce il differenziale tra il fuso orario locale corrente e il GMT. Il valore restituito è una stringa nel formato seguente:


```C++
[+/-]HHMM
```



Ad esempio, l'ora solare Pacifico è-0800.


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



Z indica nessun differenziale temporale. Tenere presente che il server di Active Directory archivia data e ora come ora GMT. Se non si specifica un intervallo di tempo, il valore predefinito è GMT.

Il valore dei secondi ("SS") è facoltativo.

Se GMT non è il fuso orario locale, applicare un valore differenziale locale per specificare il fuso orario locale. Il differenziale è: GMT = local + differenziale.

Per specificare un valore differenziale, usare il formato seguente:


```C++
YYMMDDHHMMSS[+/-]HHMM
```



Nell'esempio seguente viene illustrato un filtro che specifica un **myTimeAttrib** tempo impostato su 3/23/99 8:52:58 PM GMT:


```C++
(myTimeAttrib=990323205258Z)
```



Nell'esempio seguente viene illustrato un filtro che specifica un'ora di **myTimeAttrib** impostata su 3/23/99 8:52:58 pm senza secondi specificati:


```C++
(myTimeAttrib=9903232052Z)
```



Nell'esempio seguente viene illustrato un filtro che specifica un'ora di **myTimeAttrib** impostata su 3/23/99 8:52:58 PM Nuova Zelanda standard time (differenziale è 12 ore). Equivale a 3/23/99 8:52:58 AM GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString
</dt> <dd>

Il valore specificato in un filtro è una stringa. DirectoryString può contenere caratteri Unicode. Il confronto viene eseguito senza distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

È necessario specificare l'intero OID da confrontare.

I caratteri jolly non sono accettati.

L'attributo **objectCategory** consente di specificare il **ldapDisplayName** della classe impostata per l'attributo.

Nell'esempio seguente viene illustrato un filtro che specifica **governsID** per la classe volume:


```C++
(governsID=1.2.840.113556.1.5.36)
```



Due filtri equivalenti che specificano l'attributo **systemMustContain** che contiene **UNCName**, che presenta un OID di 1.2.840.113556.1.4.137:


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Altre sintassi
</dt> <dd>

Le seguenti sintassi vengono valutate in un filtro simile a una stringa di ottetto:

-   ObjectSecurityDescriptor
-   AccessPointDN
-   PresentationAddresses
-   ReplicaLink
-   DNWithString
-   DNWithOctetString
-   ORName

</dd> </dl>

 

 