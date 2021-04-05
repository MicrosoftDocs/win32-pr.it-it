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
# <a name="adsi-attribute-syntax"></a>Sintassi degli attributi ADSI

A ogni attributo della directory è associata una sintassi. Ad esempio, Integer, String, numeric e così via. ADSI definisce la propria sintassi che esegue il mapping alla sintassi della directory nativa. In questa sezione vengono descritti i tipi di sintassi degli attributi in ADSI.

## <a name="distinguished-name-string"></a>Stringa del nome distinto


```VB
Syntax Type: ADSTYPE_DN_STRING
```



Il nome distinto è utile per collegare due oggetti. Ad esempio, è possibile creare un collegamento che rende l'oggetto Alice un responsabile dell'oggetto Bob. Se l'oggetto Alice si sposta in una posizione diversa, il collegamento al gestore tra Alice e Bob viene aggiornato automaticamente.

Il nome distinto deve contenere un oggetto nome distinto valido. Se il nome distinto non corrisponde a un oggetto esistente valido, la maggior parte dei server rifiuta la richiesta e restituisce un errore di violazione del vincolo.

Esempi:


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a>Stringa del case esatta e maiuscole/minuscole


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



Il caso stringa esatta è una stringa con distinzione tra maiuscole e minuscole, mentre case ignora stringa è una stringa senza distinzione tra maiuscole e minuscole Una percentuale elevata di attributi nella directory utilizza questa sintassi.

> [!Note]  
> La directory potrebbe non essere archiviata come stringa Unicode. Tuttavia, ADSI accetta e restituisce stringhe Unicode.

 

Esempio:


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a>Stringa stampabile


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



Questa sintassi viene utilizzata per gli attributi con valori di stringa in cui maiuscole e minuscole sono considerati diversi per i confronti, ad esempio, "FABRIKAM" e "Fabrikam" non corrispondono. ADSI accetta qualsiasi contenuto per una stringa stampabile; non tenta di verificare che siano effettivamente stampabili.

## <a name="numeric-string"></a>Stringa numerica


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



In questa sintassi, le stringhe corrispondono come in una stringa stampabile, ad eccezione del fatto che tutti gli spazi vengono ignorati nei confronti. ADSI non esegue il controllo del valore per garantire che vengano visualizzati solo numeri e spazi nei valori di questa sintassi. Active Directory accetta qualsiasi contenuto per una stringa numerica; non verifica che i caratteri siano numerici.

## <a name="utc-time"></a>Ora UTC


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Questa sintassi archivia la data e l'ora in un'unica stringa. Il formato della stringa è costituito da tre parti concatenate: (1) AAMMGG; (2) HHMM o HHMMSS (entrambi sono accettabili); e (3) "Z" per indicare che l'ora specificata è ora di Greenwich (GMT) o "+/-HHMM" per indicare che l'ora specificata è l'ora locale con il differenziale specificato da GMT. Il differenziale è basato sulla formula: GMT = local + differenziale.

> [!Note]  
> Le prime due cifre dell'anno non vengono archiviate in questa stringa.

 

Alcuni esempi di valori validi sono "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503 + 0130". Questa stringa viene archiviata come caratteri ASCII a byte singolo e non viene archiviato alcun numero di tabella codici.

Anche se l'ordinamento è supportato, viene eseguito solo come ordinamento di stringhe ASCII senza distinzione tra maiuscole e minuscole, non interpretando correttamente il significato delle stringhe.

Qualsiasi valore stringa valido viene accettato. Non viene effettuato alcun tentativo di verificare che la stringa contenga una stringa di ora valida.

## <a name="generalized-time"></a>Ora generalizzata


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Se viene definito un nuovo attributo per archiviare i valori temporali, è consigliabile usare la sintassi GeneralizedTime. La sintassi GeneralizedTime usa quattro caratteri per rappresentare l'anno anziché due come con UTCTime.

Il formato della sintassi GeneralizedTime è "ad aaaammgghhmmss. 0Z". Un esempio di valore accettabile è "20010928060000.0 Z". "Z" indica nessun differenziale temporale. Active Directory archivia data/ora come ora di Greenwich (GMT). Se non viene specificato alcun intervallo di tempo, GMT è il valore predefinito.

Se l'ora viene specificata in un fuso orario diverso da GMT, il differenziale tra il fuso orario e il GMT viene aggiunto alla stringa anziché "Z" nel formato "ad aaaammgghhmmss. 0 \[ +/- \] hhmm". Un esempio di valore accettabile è "20010928060000.0 + 0200".

Il differenziale è basato sulla formula: GMT = local + differenziale.

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory accetta solo un valore con segno a 32 bit per questa sintassi. Gestisce zero come **false** e tutti i valori diversi da zero come **true**.

## <a name="integer"></a>Integer


```VB
Syntax Type: ADSTYPE_INTEGER
```



Valore numerico con segno a 32 bit.

## <a name="large-integer"></a>Integer grande


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



Valore numerico con segno a 64 bit. I numeri interi di grandi dimensioni vengono effettivamente implementati come oggetti COM nell'interfaccia [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) . I metodi **HighPart** e **LowPart** vengono usati per accedere alle metà di 2 32 bit del valore Integer grande.

Esempio:


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>Stringa ottetto


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



Una stringa di ottetto viene restituita come matrice di byte Variant. È costituito da un conteggio delle dimensioni (numero di ottetti) seguito da una serie di ottetti. Un ottetto è un byte a 8 bit, quindi una serie di ottetti è una stringa di dati binari.

## <a name="object-class"></a>Classe Object


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



Object Class è un identificatore di oggetto univoco per una determinata classe di schema. La classe di ogni istanza di oggetto è identificata dall'attributo **objectClass** . Al momento della creazione, non è possibile modificare mai una classe di oggetti. **objectClass** è un attributo a più valori. Viene elencata la classe specifica dell'oggetto e le classi di tutte le classi strutturali o astratte da cui è stata derivata la classe specifica. Sono incluse le classi Top, da cui derivano tutte le altre classi. Active Directory non elenca le classi ausiliarie nell'attributo **objectClass** .

## <a name="security-descriptor"></a>Descrittore di sicurezza


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



I diritti di accesso definiscono le capacità di un'entità di sicurezza quando tenta di eseguire un'operazione su un oggetto Active Directory. Un descrittore di sicurezza descrive le informazioni di controllo di accesso associate a un oggetto.

Il descrittore di sicurezza viene archiviato come proprietà di un oggetto directory nella proprietà **ntSecurityDescriptor** . Quando un utente autenticato tenta di accedere a un oggetto directory, il server di directory determina l'accesso concesso o negato all'utente in base al descrittore di sicurezza dell'oggetto.

L'enumerazione di enumerazione del [**\_ \_ controllo \_ SD di ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) specifica i flag di controllo per un descrittore di sicurezza.

Nell'esempio di codice riportato di seguito viene illustrato come ottenere un descrittore di sicurezza.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi per gli attributi di Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[Scelta di una sintassi](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[Come specificare i valori di confronto](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 