---
title: Sintassi degli attributi ADSI
description: A ogni attributo della directory è associata una sintassi. Ad esempio, Integer, String, numeric e così via. ADSI definisce la propria sintassi che esegue il mapping alla sintassi della directory nativa. In questa sezione vengono descritti i tipi di sintassi degli attributi in ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- attributi ADSI, sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730215"
---
# <a name="adsi-attribute-syntax"></a><span data-ttu-id="b9275-107">Sintassi degli attributi ADSI</span><span class="sxs-lookup"><span data-stu-id="b9275-107">ADSI Attribute Syntax</span></span>

<span data-ttu-id="b9275-108">A ogni attributo della directory è associata una sintassi.</span><span class="sxs-lookup"><span data-stu-id="b9275-108">Each attribute in the directory has an associated syntax.</span></span> <span data-ttu-id="b9275-109">Ad esempio, Integer, String, numeric e così via.</span><span class="sxs-lookup"><span data-stu-id="b9275-109">For example, integer, string, numeric, and so on.</span></span> <span data-ttu-id="b9275-110">ADSI definisce la propria sintassi che esegue il mapping alla sintassi della directory nativa.</span><span class="sxs-lookup"><span data-stu-id="b9275-110">ADSI defines its own syntax that maps to the native directory syntax.</span></span> <span data-ttu-id="b9275-111">In questa sezione vengono descritti i tipi di sintassi degli attributi in ADSI.</span><span class="sxs-lookup"><span data-stu-id="b9275-111">This section describes the types of attribute syntaxes in ADSI.</span></span>

## <a name="distinguished-name-string"></a><span data-ttu-id="b9275-112">Stringa del nome distinto</span><span class="sxs-lookup"><span data-stu-id="b9275-112">Distinguished Name String</span></span>


```VB
Syntax Type: ADSTYPE_DN_STRING
```



<span data-ttu-id="b9275-113">Il nome distinto è utile per collegare due oggetti.</span><span class="sxs-lookup"><span data-stu-id="b9275-113">The distinguished name is useful for linking two objects together.</span></span> <span data-ttu-id="b9275-114">Ad esempio, è possibile creare un collegamento che rende l'oggetto Alice un responsabile dell'oggetto Bob.</span><span class="sxs-lookup"><span data-stu-id="b9275-114">For example, it can create a link that makes the Alice object a manager of the Bob object.</span></span> <span data-ttu-id="b9275-115">Se l'oggetto Alice si sposta in una posizione diversa, il collegamento al gestore tra Alice e Bob viene aggiornato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b9275-115">If the Alice object moves to different place, the manager link between Alice and Bob is updated automatically.</span></span>

<span data-ttu-id="b9275-116">Il nome distinto deve contenere un oggetto nome distinto valido.</span><span class="sxs-lookup"><span data-stu-id="b9275-116">The distinguished name must contain a valid distinguished name object.</span></span> <span data-ttu-id="b9275-117">Se il nome distinto non corrisponde a un oggetto esistente valido, la maggior parte dei server rifiuta la richiesta e restituisce un errore di violazione del vincolo.</span><span class="sxs-lookup"><span data-stu-id="b9275-117">If the distinguished name does not correspond to a valid existing object, most servers reject the request and return a constraint violation error.</span></span>

<span data-ttu-id="b9275-118">Esempi:</span><span class="sxs-lookup"><span data-stu-id="b9275-118">Examples:</span></span>


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a><span data-ttu-id="b9275-119">Stringa del case esatta e maiuscole/minuscole</span><span class="sxs-lookup"><span data-stu-id="b9275-119">Case Exact String and Case Ignore String</span></span>


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



<span data-ttu-id="b9275-120">Il caso stringa esatta è una stringa con distinzione tra maiuscole e minuscole, mentre case ignora stringa è una stringa senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="b9275-120">Case Exact String is a case-sensitive string while Case Ignore String is a case-insensitive string.</span></span> <span data-ttu-id="b9275-121">Una percentuale elevata di attributi nella directory utilizza questa sintassi.</span><span class="sxs-lookup"><span data-stu-id="b9275-121">A large percentage of attributes in the directory use this syntax.</span></span>

> [!Note]  
> <span data-ttu-id="b9275-122">La directory potrebbe non essere archiviata come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="b9275-122">The directory may or may not store this as a Unicode string.</span></span> <span data-ttu-id="b9275-123">Tuttavia, ADSI accetta e restituisce stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="b9275-123">However, ADSI accepts and returns Unicode strings.</span></span>

 

<span data-ttu-id="b9275-124">Esempio:</span><span class="sxs-lookup"><span data-stu-id="b9275-124">Example:</span></span>


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a><span data-ttu-id="b9275-125">Stringa stampabile</span><span class="sxs-lookup"><span data-stu-id="b9275-125">Printable String</span></span>


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



<span data-ttu-id="b9275-126">Questa sintassi viene utilizzata per gli attributi con valori di stringa in cui maiuscole e minuscole sono considerati diversi per i confronti, ad esempio, "FABRIKAM" e "Fabrikam" non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="b9275-126">This syntax is used for attributes with string values where uppercase and lowercase are considered unequal for comparisons, for example, "FABRIKAM" and "Fabrikam" do not match.</span></span> <span data-ttu-id="b9275-127">ADSI accetta qualsiasi contenuto per una stringa stampabile; non tenta di verificare che siano effettivamente stampabili.</span><span class="sxs-lookup"><span data-stu-id="b9275-127">ADSI accepts any contents for a Printable-String; it does not attempt to verify that they are indeed printable.</span></span>

## <a name="numeric-string"></a><span data-ttu-id="b9275-128">Stringa numerica</span><span class="sxs-lookup"><span data-stu-id="b9275-128">Numeric String</span></span>


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



<span data-ttu-id="b9275-129">In questa sintassi, le stringhe corrispondono come in una stringa stampabile, ad eccezione del fatto che tutti gli spazi vengono ignorati nei confronti.</span><span class="sxs-lookup"><span data-stu-id="b9275-129">In this syntax, strings match as in Printable String, except that all space characters are ignored in comparisons.</span></span> <span data-ttu-id="b9275-130">ADSI non esegue il controllo del valore per garantire che vengano visualizzati solo numeri e spazi nei valori di questa sintassi.</span><span class="sxs-lookup"><span data-stu-id="b9275-130">ADSI does not perform value checking to ensure that only numerals and spaces appear in values of this syntax.</span></span> <span data-ttu-id="b9275-131">Active Directory accetta qualsiasi contenuto per una stringa numerica; non verifica che i caratteri siano numerici.</span><span class="sxs-lookup"><span data-stu-id="b9275-131">Active Directory accepts any content for a numeric string; it does not verify that the characters are numeric.</span></span>

## <a name="utc-time"></a><span data-ttu-id="b9275-132">Ora UTC</span><span class="sxs-lookup"><span data-stu-id="b9275-132">UTC Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="b9275-133">Questa sintassi archivia la data e l'ora in un'unica stringa.</span><span class="sxs-lookup"><span data-stu-id="b9275-133">This syntax stores the date and time in a single string.</span></span> <span data-ttu-id="b9275-134">Il formato della stringa è costituito da tre parti concatenate: (1) AAMMGG; (2) HHMM o HHMMSS (entrambi sono accettabili); e (3) "Z" per indicare che l'ora specificata è ora di Greenwich (GMT) o "+/-HHMM" per indicare che l'ora specificata è l'ora locale con il differenziale specificato da GMT.</span><span class="sxs-lookup"><span data-stu-id="b9275-134">The string format consists of three concatenated parts: (1) YYMMDD; (2) HHMM or HHMMSS (both are acceptable); and (3) "Z" to indicate that the time given is Greenwich Mean Time (GMT), or "+/-HHMM" to indicate that the time given is local time with the given differential from GMT.</span></span> <span data-ttu-id="b9275-135">Il differenziale è basato sulla formula: GMT = local + differenziale.</span><span class="sxs-lookup"><span data-stu-id="b9275-135">The differential is based on the formula: GMT=Local+differential.</span></span>

> [!Note]  
> <span data-ttu-id="b9275-136">Le prime due cifre dell'anno non vengono archiviate in questa stringa.</span><span class="sxs-lookup"><span data-stu-id="b9275-136">The first two digits of the year are not stored in this string.</span></span>

 

<span data-ttu-id="b9275-137">Alcuni esempi di valori validi sono "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503 + 0130".</span><span class="sxs-lookup"><span data-stu-id="b9275-137">Some examples of legal values are "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130".</span></span> <span data-ttu-id="b9275-138">Questa stringa viene archiviata come caratteri ASCII a byte singolo e non viene archiviato alcun numero di tabella codici.</span><span class="sxs-lookup"><span data-stu-id="b9275-138">This string is stored as single-byte ASCII characters, and no code page number is stored with it.</span></span>

<span data-ttu-id="b9275-139">Anche se l'ordinamento è supportato, viene eseguito solo come ordinamento di stringhe ASCII senza distinzione tra maiuscole e minuscole, non interpretando correttamente il significato delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="b9275-139">Although ordering is supported, it is done only as an ASCII case-insensitive string sort, not by properly interpreting the meaning of the strings.</span></span>

<span data-ttu-id="b9275-140">Qualsiasi valore stringa valido viene accettato.</span><span class="sxs-lookup"><span data-stu-id="b9275-140">Any valid string value is accepted.</span></span> <span data-ttu-id="b9275-141">Non viene effettuato alcun tentativo di verificare che la stringa contenga una stringa di ora valida.</span><span class="sxs-lookup"><span data-stu-id="b9275-141">No attempt is made to ensure that the string contains a valid time string.</span></span>

## <a name="generalized-time"></a><span data-ttu-id="b9275-142">Ora generalizzata</span><span class="sxs-lookup"><span data-stu-id="b9275-142">Generalized Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="b9275-143">Se viene definito un nuovo attributo per archiviare i valori temporali, è consigliabile usare la sintassi GeneralizedTime.</span><span class="sxs-lookup"><span data-stu-id="b9275-143">If a new attribute to store time values is being defined, the GeneralizedTime syntax should be used.</span></span> <span data-ttu-id="b9275-144">La sintassi GeneralizedTime usa quattro caratteri per rappresentare l'anno anziché due come con UTCTime.</span><span class="sxs-lookup"><span data-stu-id="b9275-144">GeneralizedTime syntax uses four characters to represent the year instead of two as with UTCTime.</span></span>

<span data-ttu-id="b9275-145">Il formato della sintassi GeneralizedTime è "ad aaaammgghhmmss. 0Z".</span><span class="sxs-lookup"><span data-stu-id="b9275-145">The format for the GeneralizedTime syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="b9275-146">Un esempio di valore accettabile è "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="b9275-146">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="b9275-147">"Z" indica nessun differenziale temporale.</span><span class="sxs-lookup"><span data-stu-id="b9275-147">The "Z" indicates no time differential.</span></span> <span data-ttu-id="b9275-148">Active Directory archivia data/ora come ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="b9275-148">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="b9275-149">Se non viene specificato alcun intervallo di tempo, GMT è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b9275-149">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="b9275-150">Se l'ora viene specificata in un fuso orario diverso da GMT, il differenziale tra il fuso orario e il GMT viene aggiunto alla stringa anziché "Z" nel formato "ad aaaammgghhmmss. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="b9275-150">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="b9275-151">Un esempio di valore accettabile è "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="b9275-151">An example of an acceptable value is "20010928060000.0+0200".</span></span>

<span data-ttu-id="b9275-152">Il differenziale è basato sulla formula: GMT = local + differenziale.</span><span class="sxs-lookup"><span data-stu-id="b9275-152">The differential is based on the formula: GMT=Local+differential.</span></span>

## <a name="boolean"></a><span data-ttu-id="b9275-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="b9275-153">Boolean</span></span>


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



<span data-ttu-id="b9275-154">Active Directory accetta solo un valore con segno a 32 bit per questa sintassi.</span><span class="sxs-lookup"><span data-stu-id="b9275-154">Active Directory accepts only a signed 32-bit value for this syntax.</span></span> <span data-ttu-id="b9275-155">Gestisce zero come **false** e tutti i valori diversi da zero come **true**.</span><span class="sxs-lookup"><span data-stu-id="b9275-155">It handles zero as **FALSE** and all nonzero values as **TRUE**.</span></span>

## <a name="integer"></a><span data-ttu-id="b9275-156">Integer</span><span class="sxs-lookup"><span data-stu-id="b9275-156">Integer</span></span>


```VB
Syntax Type: ADSTYPE_INTEGER
```



<span data-ttu-id="b9275-157">Valore numerico con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b9275-157">A 32-bit signed numeric value.</span></span>

## <a name="large-integer"></a><span data-ttu-id="b9275-158">Integer grande</span><span class="sxs-lookup"><span data-stu-id="b9275-158">Large Integer</span></span>


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



<span data-ttu-id="b9275-159">Valore numerico con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="b9275-159">A 64-bit signed numeric value.</span></span> <span data-ttu-id="b9275-160">I numeri interi di grandi dimensioni vengono effettivamente implementati come oggetti COM nell'interfaccia [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) .</span><span class="sxs-lookup"><span data-stu-id="b9275-160">Large integers are actually implemented as COM objects on the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface.</span></span> <span data-ttu-id="b9275-161">I metodi **HighPart** e **LowPart** vengono usati per accedere alle metà di 2 32 bit del valore Integer grande.</span><span class="sxs-lookup"><span data-stu-id="b9275-161">The **HighPart** and **LowPart** methods are used to access the two 32-bit halves of the large integer value.</span></span>

<span data-ttu-id="b9275-162">Esempio:</span><span class="sxs-lookup"><span data-stu-id="b9275-162">Example:</span></span>


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a><span data-ttu-id="b9275-163">Stringa ottetto</span><span class="sxs-lookup"><span data-stu-id="b9275-163">Octet String</span></span>


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



<span data-ttu-id="b9275-164">Una stringa di ottetto viene restituita come matrice di byte Variant.</span><span class="sxs-lookup"><span data-stu-id="b9275-164">An octet string is returned as a variant array of bytes.</span></span> <span data-ttu-id="b9275-165">È costituito da un conteggio delle dimensioni (numero di ottetti) seguito da una serie di ottetti.</span><span class="sxs-lookup"><span data-stu-id="b9275-165">This consists of a size count (number of octets) followed by a series of octets.</span></span> <span data-ttu-id="b9275-166">Un ottetto è un byte a 8 bit, quindi una serie di ottetti è una stringa di dati binari.</span><span class="sxs-lookup"><span data-stu-id="b9275-166">An octet is an 8-bit byte, so a series of octets is a string of binary data.</span></span>

## <a name="object-class"></a><span data-ttu-id="b9275-167">Classe Object</span><span class="sxs-lookup"><span data-stu-id="b9275-167">Object Class</span></span>


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



<span data-ttu-id="b9275-168">Object Class è un identificatore di oggetto univoco per una determinata classe di schema.</span><span class="sxs-lookup"><span data-stu-id="b9275-168">Object Class is a unique object identifier for a given schema class.</span></span> <span data-ttu-id="b9275-169">La classe di ogni istanza di oggetto è identificata dall'attributo **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="b9275-169">The class of each object instance is identified by the **objectClass** attribute.</span></span> <span data-ttu-id="b9275-170">Al momento della creazione, non è possibile modificare mai una classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="b9275-170">When created, you can never change an object class.</span></span> <span data-ttu-id="b9275-171">**objectClass** è un attributo a più valori.</span><span class="sxs-lookup"><span data-stu-id="b9275-171">**objectClass** is a multiple valued attribute.</span></span> <span data-ttu-id="b9275-172">Viene elencata la classe specifica dell'oggetto e le classi di tutte le classi strutturali o astratte da cui è stata derivata la classe specifica.</span><span class="sxs-lookup"><span data-stu-id="b9275-172">It lists the specific class of the object, and the classes of all structural or abstract classes from which the specific class was derived.</span></span> <span data-ttu-id="b9275-173">Sono incluse le classi Top, da cui derivano tutte le altre classi.</span><span class="sxs-lookup"><span data-stu-id="b9275-173">This includes Top, the class from which all other classes are ultimately derived.</span></span> <span data-ttu-id="b9275-174">Active Directory non elenca le classi ausiliarie nell'attributo **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="b9275-174">Active Directory does not list auxiliary classes in the **objectClass** attribute.</span></span>

## <a name="security-descriptor"></a><span data-ttu-id="b9275-175">Descrittore di sicurezza</span><span class="sxs-lookup"><span data-stu-id="b9275-175">Security Descriptor</span></span>


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



<span data-ttu-id="b9275-176">I diritti di accesso definiscono le capacità di un'entità di sicurezza quando tenta di eseguire un'operazione su un oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b9275-176">Access rights define what abilities a security principal has when it attempts to perform an operation on an Active Directory object.</span></span> <span data-ttu-id="b9275-177">Un descrittore di sicurezza descrive le informazioni di controllo di accesso associate a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b9275-177">A security descriptor describes the access control information associated with an object.</span></span>

<span data-ttu-id="b9275-178">Il descrittore di sicurezza viene archiviato come proprietà di un oggetto directory nella proprietà **ntSecurityDescriptor** .</span><span class="sxs-lookup"><span data-stu-id="b9275-178">The security descriptor is stored as a property of a directory object in the **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="b9275-179">Quando un utente autenticato tenta di accedere a un oggetto directory, il server di directory determina l'accesso concesso o negato all'utente in base al descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b9275-179">When an authenticated user attempts to access a directory object, the directory server determines the access granted or denied to the user based on the object security descriptor.</span></span>

<span data-ttu-id="b9275-180">L'enumerazione di enumerazione del [**\_ \_ controllo \_ SD di ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) specifica i flag di controllo per un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b9275-180">The [**ADS\_SD\_CONTROL\_ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) enumeration specifies control flags for a security descriptor.</span></span>

<span data-ttu-id="b9275-181">Nell'esempio di codice riportato di seguito viene illustrato come ottenere un descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b9275-181">The following code example shows how to obtain a security descriptor.</span></span>


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a><span data-ttu-id="b9275-182">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9275-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9275-183">Sintassi per gli attributi di Active Directory</span><span class="sxs-lookup"><span data-stu-id="b9275-183">Syntaxes for Active Directory Attributes</span></span>](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[<span data-ttu-id="b9275-184">Scelta di una sintassi</span><span class="sxs-lookup"><span data-stu-id="b9275-184">Choosing a Syntax</span></span>](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[<span data-ttu-id="b9275-185">Come specificare i valori di confronto</span><span class="sxs-lookup"><span data-stu-id="b9275-185">How to Specify Comparison Values</span></span>](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 