---
title: Come specificare i valori di confronto
description: Ogni tipo di attributo ha una sintassi che determina il tipo di valori di confronto che è possibile specificare in un filtro di ricerca per tale attributo.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Come specificare i valori di confronto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edba238961cdc18b088b6b5bd5b06ff4be383add
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386751"
---
# <a name="how-to-specify-comparison-values"></a><span data-ttu-id="fef94-104">Come specificare i valori di confronto</span><span class="sxs-lookup"><span data-stu-id="fef94-104">How to Specify Comparison Values</span></span>

<span data-ttu-id="fef94-105">Ogni tipo di attributo ha una sintassi che determina il tipo di valori di confronto che è possibile specificare in un filtro di ricerca per tale attributo.</span><span class="sxs-lookup"><span data-stu-id="fef94-105">Each attribute type has a syntax that determines the type of comparison values that you can specify in a search filter for that attribute.</span></span>

<span data-ttu-id="fef94-106">Nelle sezioni seguenti vengono descritti i requisiti per la sintassi di ogni attributo.</span><span class="sxs-lookup"><span data-stu-id="fef94-106">The following sections describe requirements for each attribute syntax.</span></span> <span data-ttu-id="fef94-107">Per altre informazioni sulle sintassi degli attributi, vedere [Sintassi per gli attributi in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="fef94-107">For more information about attribute syntaxes, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<dl> <dt>

<span data-ttu-id="fef94-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span><span class="sxs-lookup"><span data-stu-id="fef94-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span></span>
</dt> <dd>

<span data-ttu-id="fef94-109">Il valore specificato in un filtro deve essere un valore stringa "TRUE" o "FALSE".</span><span class="sxs-lookup"><span data-stu-id="fef94-109">The value specified in a filter must be a string value that is either "TRUE" or "FALSE".</span></span> <span data-ttu-id="fef94-110">Negli esempi seguenti viene illustrato come specificare una stringa di confronto booleana.</span><span class="sxs-lookup"><span data-stu-id="fef94-110">The following examples show how to specify a Boolean comparison string.</span></span>

<span data-ttu-id="fef94-111">L'esempio seguente cerca gli oggetti con **showInAdvancedViewOnly** impostato su **TRUE:**</span><span class="sxs-lookup"><span data-stu-id="fef94-111">The following example will search for objects that have a **showInAdvancedViewOnly** set to **TRUE**:</span></span>


```C++
(showInAdvancedViewOnly=TRUE)
```



<span data-ttu-id="fef94-112">L'esempio seguente cerca gli oggetti con **showInAdvancedViewOnly** impostato su **FALSE:**</span><span class="sxs-lookup"><span data-stu-id="fef94-112">The following example will search for objects that have a **showInAdvancedViewOnly** set to **FALSE**:</span></span>


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span data-ttu-id="fef94-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer ed enumerazione</span><span class="sxs-lookup"><span data-stu-id="fef94-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer and Enumeration</span></span>
</dt> <dd>

<span data-ttu-id="fef94-114">Il valore specificato in un filtro deve essere un numero intero decimale.</span><span class="sxs-lookup"><span data-stu-id="fef94-114">The value specified in a filter must be a decimal Integer.</span></span> <span data-ttu-id="fef94-115">I valori esadecimali devono essere convertiti in decimali.</span><span class="sxs-lookup"><span data-stu-id="fef94-115">Hexadecimal values must be converted to decimal.</span></span> <span data-ttu-id="fef94-116">Una stringa di confronto dei valori ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="fef94-116">A value comparison string takes the following form:</span></span>


```C++
<attribute name>:<value>
```



<span data-ttu-id="fef94-117">" <attribute name> " è il valore **lDAPDisplayName** dell'attributo e "</span><span class="sxs-lookup"><span data-stu-id="fef94-117">"<attribute name>" is the **lDAPDisplayName** of the attribute and "</span></span><value><span data-ttu-id="fef94-118">" è il valore da usare per il confronto.</span><span class="sxs-lookup"><span data-stu-id="fef94-118">" is the value to use for comparison.</span></span>

<span data-ttu-id="fef94-119">Nell'esempio di codice seguente viene illustrato un filtro che consente di cercare oggetti con un valore **groupType** uguale al flag **ADS \_ GROUP TYPE UNIVERSAL \_ \_ \_ GROUP** (8) e al flag **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000).</span><span class="sxs-lookup"><span data-stu-id="fef94-119">The following code example shows a filter that will search for objects that have a **groupType** value that is equal to the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** (8) flag and the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000) flag.</span></span> <span data-ttu-id="fef94-120">I due flag combinati sono uguali 0x80000008, che viene convertito in decimal è 2147483656.</span><span class="sxs-lookup"><span data-stu-id="fef94-120">The two flags combined equal 0x80000008, which converted to decimal is 2147483656.</span></span>


```C++
(groupType=2147483656)
```



<span data-ttu-id="fef94-121">Gli operatori delle regole di corrispondenza LDAP possono essere usati anche per eseguire confronti bit per bit.</span><span class="sxs-lookup"><span data-stu-id="fef94-121">The LDAP matching rule operators can also be used to perform bitwise comparisons.</span></span> <span data-ttu-id="fef94-122">Per altre informazioni sulle regole di corrispondenza, vedere [Sintassi dei filtri di ricerca.](/windows/desktop/ADSI/search-filter-syntax)</span><span class="sxs-lookup"><span data-stu-id="fef94-122">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span> <span data-ttu-id="fef94-123">Nell'esempio di codice seguente viene illustrato un filtro che consente di cercare oggetti con **groupType** con il set di bit **ADS \_ GROUP TYPE \_ SECURITY \_ \_ ENABLED** (0x80000000 = 2147483648).</span><span class="sxs-lookup"><span data-stu-id="fef94-123">The following code example shows a filter that will search for objects that have a **groupType** with the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) bit set.</span></span>


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span data-ttu-id="fef94-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span><span class="sxs-lookup"><span data-stu-id="fef94-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span></span>
</dt> <dd>

<span data-ttu-id="fef94-125">Il valore specificato in un filtro è il numero di dati da trovare.</span><span class="sxs-lookup"><span data-stu-id="fef94-125">The value specified in a filter is the data to be found.</span></span> <span data-ttu-id="fef94-126">I dati devono essere rappresentati come una stringa di byte con codifica a due caratteri in cui ogni byte è preceduto da una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="fef94-126">The data must be represented as a two character encoded byte string where each byte is preceded by a backslash (\\).</span></span> <span data-ttu-id="fef94-127">Ad esempio, il valore 0x05 verrà visualizzato nella stringa come " \\ 05".</span><span class="sxs-lookup"><span data-stu-id="fef94-127">For example, the value 0x05 will appear in the string as "\\05".</span></span>

<span data-ttu-id="fef94-128">La [**funzione ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) può essere usata per creare una rappresentazione di stringa codificata dei dati binari.</span><span class="sxs-lookup"><span data-stu-id="fef94-128">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function can be used to create an encoded string representation of binary data.</span></span> <span data-ttu-id="fef94-129">La **funzione ADsEncodeBinaryData** non codifica i valori byte che rappresentano caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="fef94-129">The **ADsEncodeBinaryData** function does not encode byte values that represent alpha-numeric characters.</span></span> <span data-ttu-id="fef94-130">Il carattere verrà invece inserito nella stringa senza codificarlo.</span><span class="sxs-lookup"><span data-stu-id="fef94-130">It will, instead, place the character into the string without encoding it.</span></span> <span data-ttu-id="fef94-131">Il risultato è la stringa contenente una combinazione di caratteri codificati e non codificati.</span><span class="sxs-lookup"><span data-stu-id="fef94-131">This results in the string containing a mixture of encoded and unencoded characters.</span></span> <span data-ttu-id="fef94-132">Ad esempio, se i dati binari sono 0x05 0x1A 0x1B 0x43 0x32, la stringa codificata conterrà \| \| " \| \| \\ 05 \\ 1A \\ 1BC2".</span><span class="sxs-lookup"><span data-stu-id="fef94-132">For example, if the binary data is 0x05\|0x1A\|0x1B\|0x43\|0x32, the encoded string will contain "\\05\\1A\\1BC2".</span></span> <span data-ttu-id="fef94-133">Questa operazione non ha alcun effetto sul filtro e i filtri di ricerca funzioneranno correttamente con questi tipi di stringhe.</span><span class="sxs-lookup"><span data-stu-id="fef94-133">This has no effect on the filter and the search filters will work correctly with these types of strings.</span></span>

<span data-ttu-id="fef94-134">I caratteri jolly vengono accettati.</span><span class="sxs-lookup"><span data-stu-id="fef94-134">Wildcards are accepted.</span></span>

<span data-ttu-id="fef94-135">L'esempio di codice seguente mostra un filtro che contiene una stringa codificata per **schemaIDGUID** con valore GUID "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span><span class="sxs-lookup"><span data-stu-id="fef94-135">The following code example shows a filter that contains encoded string for **schemaIDGUID** with GUID value of "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span></span>


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span data-ttu-id="fef94-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span><span class="sxs-lookup"><span data-stu-id="fef94-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span></span>
</dt> <dd>

<span data-ttu-id="fef94-137">Il valore specificato in un filtro è la rappresentazione della stringa di byte codificata del SID.</span><span class="sxs-lookup"><span data-stu-id="fef94-137">The value specified in a filter is the encoded byte string representation of the SID.</span></span> <span data-ttu-id="fef94-138">Per altre informazioni sulle stringhe di byte codificate, vedere la sezione precedente di questo argomento che illustra la sintassi OctetString.</span><span class="sxs-lookup"><span data-stu-id="fef94-138">For more information about encoded byte strings, see the previous section in this topic which discusses OctetString syntax.</span></span>

<span data-ttu-id="fef94-139">L'esempio di codice seguente mostra un filtro che contiene una stringa codificata per **objectSid** con valore stringa SID "S-1-5-21-1935655697-308236825-1417001333":</span><span class="sxs-lookup"><span data-stu-id="fef94-139">The following code example shows a filter that contains an encoded string for **objectSid** with SID string value of "S-1-5-21-1935655697-308236825-1417001333":</span></span>


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span data-ttu-id="fef94-140"><span id="DN"></span><span id="dn"></span>Dn</span><span class="sxs-lookup"><span data-stu-id="fef94-140"><span id="DN"></span><span id="dn"></span>DN</span></span>
</dt> <dd>

<span data-ttu-id="fef94-141">È necessario specificare l'intero nome distinto da associare.</span><span class="sxs-lookup"><span data-stu-id="fef94-141">The entire distinguished name, to be matched, must be supplied.</span></span>

<span data-ttu-id="fef94-142">I caratteri jolly non sono accettati.</span><span class="sxs-lookup"><span data-stu-id="fef94-142">Wildcards are not accepted.</span></span>

<span data-ttu-id="fef94-143">Tenere presente che **l'attributo objectCategory** consente anche di specificare **lDAPDisplayName** della classe impostata sull'attributo.</span><span class="sxs-lookup"><span data-stu-id="fef94-143">Be aware that the **objectCategory** attribute also enables you to specify the **lDAPDisplayName** of the class set on the attribute.</span></span>

<span data-ttu-id="fef94-144">L'esempio seguente illustra un filtro che specifica un **membro** che contiene "CN=TestUser,DC=Fabrikam,DC=COM":</span><span class="sxs-lookup"><span data-stu-id="fef94-144">The following example shows a filter that specifies a **member** that contains "CN=TestUser,DC=Fabrikam,DC=COM":</span></span>


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span data-ttu-id="fef94-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span><span class="sxs-lookup"><span data-stu-id="fef94-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span></span>
</dt> <dd>

<span data-ttu-id="fef94-146">Il valore specificato in un filtro deve essere un numero intero decimale.</span><span class="sxs-lookup"><span data-stu-id="fef94-146">The value specified in a filter must be a decimal integer.</span></span> <span data-ttu-id="fef94-147">Converte i valori esadecimali in decimali.</span><span class="sxs-lookup"><span data-stu-id="fef94-147">Convert hexadecimal values to decimal.</span></span>

<span data-ttu-id="fef94-148">L'esempio di codice seguente illustra un filtro che specifica un **valore creationTime** impostato su [**UN VALORE FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) "1999-12-31 23:59:59 (UTC/GMT)":</span><span class="sxs-lookup"><span data-stu-id="fef94-148">The following code example shows a filter that specifies a **creationTime** set to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) of "1999-12-31 23:59:59 (UTC/GMT)":</span></span>


```C++
(creationTime=125911583990000000)
```



<span data-ttu-id="fef94-149">Le funzioni seguenti creano un filtro di corrispondenza esatta (=) per un attributo integer di grandi dimensioni e verificano l'attributo nello schema e la relativa sintassi:</span><span class="sxs-lookup"><span data-stu-id="fef94-149">The following functions create an exact match (=) filter for a large integer attribute and verify the attribute in the schema and its syntax:</span></span>


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

<span data-ttu-id="fef94-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span><span class="sxs-lookup"><span data-stu-id="fef94-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span></span>
</dt> <dd>

<span data-ttu-id="fef94-151">Gli attributi con queste sintassi devono essere conformi a set di caratteri specifici.</span><span class="sxs-lookup"><span data-stu-id="fef94-151">Attributes with these syntaxes should adhere to specific character sets.</span></span> <span data-ttu-id="fef94-152">Per altre informazioni, vedere [Sintassi per gli attributi in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="fef94-152">For more information, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="fef94-153">Attualmente, Active Directory Domain Services non applicano tali set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fef94-153">Currently, Active Directory Domain Services do not enforce those character sets.</span></span>

<span data-ttu-id="fef94-154">Il valore specificato in un filtro è una stringa.</span><span class="sxs-lookup"><span data-stu-id="fef94-154">The value specified in a filter is a string.</span></span> <span data-ttu-id="fef94-155">Il confronto fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fef94-155">The comparison is case-sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="fef94-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span><span class="sxs-lookup"><span data-stu-id="fef94-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span></span>
</dt> <dd>

<span data-ttu-id="fef94-157">Il valore specificato in un filtro è una stringa che rappresenta la data nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="fef94-157">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYYYMMDDHHMMSS.0Z
```



<span data-ttu-id="fef94-158">"0Z" indica che l'ora non è differenziale.</span><span class="sxs-lookup"><span data-stu-id="fef94-158">"0Z" indicates no time differential.</span></span> <span data-ttu-id="fef94-159">Tenere presente che il server Active Directory archivia data/ora come ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="fef94-159">Be aware that the Active Directory server stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="fef94-160">Se non viene specificato un valore differenziale dell'ora, il valore predefinito è GMT.</span><span class="sxs-lookup"><span data-stu-id="fef94-160">If a time differential is not specified, the default is GMT.</span></span>

<span data-ttu-id="fef94-161">Se il fuso orario locale non è GMT, usare un valore differenziale per specificare il fuso orario locale e applicarlo a GMT.</span><span class="sxs-lookup"><span data-stu-id="fef94-161">If the local time zone is not GMT, use a differential value to specify your local time zone and apply the differential to GMT.</span></span> <span data-ttu-id="fef94-162">Il differenziale è basato su: GMT=Local+differential.</span><span class="sxs-lookup"><span data-stu-id="fef94-162">The differential is based on: GMT=Local+differential.</span></span>

<span data-ttu-id="fef94-163">Per specificare un differenziale, usare:</span><span class="sxs-lookup"><span data-stu-id="fef94-163">To specify a differential, use:</span></span>


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



<span data-ttu-id="fef94-164">L'esempio seguente mostra un filtro che specifica **quandoCreated** time impostato su 3/23/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="fef94-164">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(whenCreated=19990323205258.0Z)
```



<span data-ttu-id="fef94-165">L'esempio seguente mostra un filtro che specifica **quandoCreated** time impostato su 3/23/99 8:52:58 PM New Australia Standard Time (differenziale è +12 ore):</span><span class="sxs-lookup"><span data-stu-id="fef94-165">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is +12 hours):</span></span>


```C++
(whenCreated=19990323205258.0+1200)
```



<span data-ttu-id="fef94-166">Nell'esempio di codice seguente viene illustrato come calcolare il fuso orario differenziale.</span><span class="sxs-lookup"><span data-stu-id="fef94-166">The following code example shows how to calculate time zone differential.</span></span> <span data-ttu-id="fef94-167">La funzione restituisce il differenziale tra il fuso orario locale corrente e GMT.</span><span class="sxs-lookup"><span data-stu-id="fef94-167">The function returns the differential between the current local time zone and GMT.</span></span> <span data-ttu-id="fef94-168">Il valore restituito è una stringa nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="fef94-168">The value returned is a string in the following format:</span></span>


```C++
[+/-]HHMM
```



<span data-ttu-id="fef94-169">Ad esempio, l'ora solare Pacifico è -0800.</span><span class="sxs-lookup"><span data-stu-id="fef94-169">For example, Pacific Standard Time is -0800.</span></span>


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

<span data-ttu-id="fef94-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span><span class="sxs-lookup"><span data-stu-id="fef94-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span></span>
</dt> <dd>

<span data-ttu-id="fef94-171">Il valore specificato in un filtro è una stringa che rappresenta la data nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="fef94-171">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYMMDDHHMMSSZ
```



<span data-ttu-id="fef94-172">Z indica che non sono presenti differenze di tempo.</span><span class="sxs-lookup"><span data-stu-id="fef94-172">Z indicates no time differential.</span></span> <span data-ttu-id="fef94-173">Tenere presente che il server Active Directory archivia data e ora come ora GMT.</span><span class="sxs-lookup"><span data-stu-id="fef94-173">Be aware that the Active Directory server stores date and time as GMT time.</span></span> <span data-ttu-id="fef94-174">Se non viene specificato un valore differenziale dell'ora, l'impostazione predefinita è GMT.</span><span class="sxs-lookup"><span data-stu-id="fef94-174">If a time differential is not specified, GMT is the default.</span></span>

<span data-ttu-id="fef94-175">Il valore dei secondi ("SS") è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fef94-175">The seconds value ("SS") is optional.</span></span>

<span data-ttu-id="fef94-176">Se GMT non è il fuso orario locale, applicare un valore differenziale locale per specificare il fuso orario locale.</span><span class="sxs-lookup"><span data-stu-id="fef94-176">If GMT is not the local time zone, apply a local differential value to specify your local time zone.</span></span> <span data-ttu-id="fef94-177">Il differenziale è: GMT=Local+differential.</span><span class="sxs-lookup"><span data-stu-id="fef94-177">The differential is: GMT=Local+differential.</span></span>

<span data-ttu-id="fef94-178">Per specificare un differenziale, usare il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="fef94-178">To specify a differential, use the following form:</span></span>


```C++
YYMMDDHHMMSS[+/-]HHMM
```



<span data-ttu-id="fef94-179">L'esempio seguente illustra un filtro che specifica un'ora **myTimeAttrib** impostata su 23/3/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="fef94-179">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(myTimeAttrib=990323205258Z)
```



<span data-ttu-id="fef94-180">L'esempio seguente illustra un filtro che specifica un'ora **myTimeAttrib** impostata su 23/3/99 8:52:58 PM senza i secondi specificati:</span><span class="sxs-lookup"><span data-stu-id="fef94-180">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM without seconds specified:</span></span>


```C++
(myTimeAttrib=9903232052Z)
```



<span data-ttu-id="fef94-181">Nell'esempio seguente viene illustrato un filtro che specifica un'ora **myTimeAttrib** impostata su 23/3/99 8:52:58 PM Ora solare Nuova Zelanda (il differenziale è di 12 ore).</span><span class="sxs-lookup"><span data-stu-id="fef94-181">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is 12 hours).</span></span> <span data-ttu-id="fef94-182">Equivale a 23/3/99 8:52:58 GMT.</span><span class="sxs-lookup"><span data-stu-id="fef94-182">This is equivalent to 3/23/99 8:52:58 AM GMT.</span></span>


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span data-ttu-id="fef94-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span><span class="sxs-lookup"><span data-stu-id="fef94-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span></span>
</dt> <dd>

<span data-ttu-id="fef94-184">Il valore specificato in un filtro è una stringa.</span><span class="sxs-lookup"><span data-stu-id="fef94-184">The value specified in a filter is a string.</span></span> <span data-ttu-id="fef94-185">DirectoryString può contenere caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="fef94-185">DirectoryString can contain Unicode characters.</span></span> <span data-ttu-id="fef94-186">Il confronto viene eseguito senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="fef94-186">The comparison is case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="fef94-187"><span id="OID"></span><span id="oid"></span>Oid</span><span class="sxs-lookup"><span data-stu-id="fef94-187"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="fef94-188">È necessario specificare l'intero OID di cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="fef94-188">The entire OID to be matched must be supplied.</span></span>

<span data-ttu-id="fef94-189">I caratteri jolly non sono accettati.</span><span class="sxs-lookup"><span data-stu-id="fef94-189">Wildcards are not accepted.</span></span>

<span data-ttu-id="fef94-190">**L'attributo objectCategory** consente di specificare **lDAPDisplayName** della classe impostata per l'attributo.</span><span class="sxs-lookup"><span data-stu-id="fef94-190">The **objectCategory** attribute enables you to specify the **lDAPDisplayName** of the class set for the attribute.</span></span>

<span data-ttu-id="fef94-191">L'esempio seguente mostra un filtro che specifica **governsID per** la classe volume:</span><span class="sxs-lookup"><span data-stu-id="fef94-191">The following example shows a filter that specifies **governsID** for volume class:</span></span>


```C++
(governsID=1.2.840.113556.1.5.36)
```



<span data-ttu-id="fef94-192">Due filtri equivalenti che specificano **l'attributo systemMustContain** contenente **uNCName**, che ha un OID di 1.2.840.113556.1.4.137:</span><span class="sxs-lookup"><span data-stu-id="fef94-192">Two equivalent filters that specifies **systemMustContain** attribute containing **uNCName**, which has an OID of 1.2.840.113556.1.4.137:</span></span>


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span data-ttu-id="fef94-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Altre sintassi</span><span class="sxs-lookup"><span data-stu-id="fef94-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Other Syntaxes</span></span>
</dt> <dd>

<span data-ttu-id="fef94-194">Le sintassi seguenti vengono valutate in un filtro simile a una stringa ottetto:</span><span class="sxs-lookup"><span data-stu-id="fef94-194">The following syntaxes are evaluated in a filter similar to an octet string:</span></span>

-   <span data-ttu-id="fef94-195">ObjectSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="fef94-195">ObjectSecurityDescriptor</span></span>
-   <span data-ttu-id="fef94-196">AccessPointDN</span><span class="sxs-lookup"><span data-stu-id="fef94-196">AccessPointDN</span></span>
-   <span data-ttu-id="fef94-197">PresentationAddresses</span><span class="sxs-lookup"><span data-stu-id="fef94-197">PresentationAddresses</span></span>
-   <span data-ttu-id="fef94-198">ReplicaLink</span><span class="sxs-lookup"><span data-stu-id="fef94-198">ReplicaLink</span></span>
-   <span data-ttu-id="fef94-199">DNWithString</span><span class="sxs-lookup"><span data-stu-id="fef94-199">DNWithString</span></span>
-   <span data-ttu-id="fef94-200">DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="fef94-200">DNWithOctetString</span></span>
-   <span data-ttu-id="fef94-201">ORName</span><span class="sxs-lookup"><span data-stu-id="fef94-201">ORName</span></span>

</dd> </dl>

 

 