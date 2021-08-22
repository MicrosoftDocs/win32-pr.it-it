---
title: Sintassi degli attributi ADSI
description: A ogni attributo nella directory è associata una sintassi. Ad esempio, integer, stringa, numerico e così via. ADSI definisce la propria sintassi che esegue il mapping alla sintassi della directory nativa. Questa sezione descrive i tipi di sintassi degli attributi in ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- attributi ADSI , sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 310a678c48051909e4a3e7555b9d8ff0a508c339cfcd41ed6c66286529cadde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023929"
---
# <a name="adsi-attribute-syntax"></a>Sintassi degli attributi ADSI

A ogni attributo nella directory è associata una sintassi. Ad esempio, integer, stringa, numerico e così via. ADSI definisce la propria sintassi che esegue il mapping alla sintassi della directory nativa. Questa sezione descrive i tipi di sintassi degli attributi in ADSI.

## <a name="distinguished-name-string"></a>Stringa del nome distinto


```VB
Syntax Type: ADSTYPE_DN_STRING
```



Il nome distinto è utile per collegare due oggetti. Ad esempio, può creare un collegamento che rende l'oggetto Alice un gestore dell'oggetto Bob. Se l'oggetto Alice viene spostato in una posizione diversa, il collegamento di gestione tra Alice e Bob viene aggiornato automaticamente.

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



## <a name="case-exact-string-and-case-ignore-string"></a>Stringa esatta di maiuscole/minuscole e stringa di ignorare maiuscole/minuscole


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



Stringa esatta di maiuscole/minuscole è una stringa con distinzione tra maiuscole e minuscole, mentre Stringa di ignorare maiuscole/minuscole è una stringa senza distinzione tra maiuscole e minuscole. Una percentuale elevata di attributi nella directory usa questa sintassi.

> [!Note]  
> La directory può o meno archiviare questa stringa come stringa Unicode. TUTTAVIA, ADSI accetta e restituisce stringhe Unicode.

 

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



Questa sintassi viene usata per gli attributi con valori stringa in cui maiuscole e minuscole sono considerate non uguali per i confronti, ad esempio "FABRIKAM" e "Fabrikam" non corrispondono. ADSI accetta qualsiasi contenuto per printable-string; non tenta di verificare che siano effettivamente stampabili.

## <a name="numeric-string"></a>Stringa numerica


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



In questa sintassi, le stringhe corrispondono come in Stringa stampabile, ad eccezione del fatto che tutti gli spazi vengono ignorati nei confronti. ADSI non esegue il controllo dei valori per garantire che nei valori di questa sintassi vengano visualizzati solo numeri e spazi. Active Directory accetta qualsiasi contenuto per una stringa numerica. non verifica che i caratteri siano numerici.

## <a name="utc-time"></a>Ora UTC


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Questa sintassi archivia la data e l'ora in una singola stringa. Il formato della stringa è costituito da tre parti concatenate: (1) YYMMDD; (2) HHMM o HHMMSS (entrambi sono accettabili); e (3) "Z" per indicare che l'ora specificata è l'ora di Greenwich Mean Time (GMT) o "+/-HHMM" per indicare che l'ora specificata è l'ora locale con il differenziale specificato rispetto a GMT. Il differenziale si basa sulla formula GMT=Local+differenziale.

> [!Note]  
> Le prime due cifre dell'anno non vengono archiviate in questa stringa.

 

Alcuni esempi di valori validi sono "9101311455Z", "910131145503Z", "91013144555-0500", "910131145503+0130". Questa stringa viene archiviata come caratteri ASCII a byte singolo e non viene archiviato alcun numero di tabella codici.

Sebbene l'ordinamento sia supportato, viene eseguito solo come ordinamento di stringhe ASCII senza distinzione tra maiuscole e minuscole, non interpretando correttamente il significato delle stringhe.

Qualsiasi valore stringa valido viene accettato. Non viene effettuato alcun tentativo di assicurarsi che la stringa contenga una stringa di ora valida.

## <a name="generalized-time"></a>Ora generalizzata


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Se viene definito un nuovo attributo per archiviare i valori di ora, è necessario usare la sintassi GeneralizedTime. La sintassi GeneralizedTime usa quattro caratteri per rappresentare l'anno anziché due come con UTCTime.

Il formato della sintassi GeneralizedTime è "AAAAMMGGHHMMSS.0Z". Un esempio di valore accettabile è "20010928060000.0Z". La "Z" non indica differenze di tempo. Active Directory archivia data/ora come ora di Greenwich (GMT). Se non viene specificato alcun differenziale di ora, GMT è l'impostazione predefinita.

Se l'ora viene specificata in un fuso orario diverso da GMT, il differenziale tra il fuso orario e GMT viene aggiunto alla stringa anziché "Z" nel formato "YYYYMMDDHHMMSS.0 \[ +/- \] HHMM". Un esempio di valore accettabile è "20010928060000.0+0200".

Il differenziale si basa sulla formula GMT=Local+differenziale.

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory accetta solo un valore a 32 bit firmato per questa sintassi. Gestisce zero come **FALSE** e tutti i valori diversi da zero come **TRUE.**

## <a name="integer"></a>Intero


```VB
Syntax Type: ADSTYPE_INTEGER
```



Valore numerico con segno a 32 bit.

## <a name="large-integer"></a>Numero intero grande


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



Valore numerico con segno a 64 bit. I numeri interi di grandi dimensioni vengono effettivamente implementati come oggetti COM [**nell'interfaccia IADsLargeInteger.**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) I **metodi HighPart** **e LowPart** vengono usati per accedere alle due metà a 32 bit del valore integer di grandi dimensioni.

Esempio:


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>Stringa dell'ottetto


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



Una stringa dell'ottetto viene restituita come matrice di byte variant. È costituito da un numero di dimensioni (numero di ottetti) seguito da una serie di ottetti. Un ottetto è un byte a 8 bit, quindi una serie di ottetti è una stringa di dati binari.

## <a name="object-class"></a>Classe Object


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



Classe di oggetti è un identificatore di oggetto univoco per una determinata classe dello schema. La classe di ogni istanza di oggetto è identificata **dall'attributo objectClass.** Dopo la creazione, non è mai possibile modificare una classe di oggetti. **objectClass** è un attributo con più valori. Elenca la classe specifica dell'oggetto e le classi di tutte le classi strutturali o astratte da cui è stata derivata la classe specifica. Ciò include Top, la classe da cui tutte le altre classi sono infine derivate. Active Directory non elenca le classi ausiliarie **nell'attributo objectClass.**

## <a name="security-descriptor"></a>Descrittore di sicurezza


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



I diritti di accesso definiscono le capacità di un'entità di sicurezza quando tenta di eseguire un'operazione su un oggetto di Active Directory. Un descrittore di sicurezza descrive le informazioni di controllo di accesso associate a un oggetto .

Il descrittore di sicurezza viene archiviato come proprietà di un oggetto directory nella **proprietà nTSecurityDescriptor.** Quando un utente autenticato tenta di accedere a un oggetto directory, il server di directory determina l'accesso concesso o negato all'utente in base al descrittore di sicurezza dell'oggetto.

[**L'enumerazione \_ ADS SD \_ CONTROL \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) specifica i flag di controllo per un descrittore di sicurezza.

Nell'esempio di codice seguente viene illustrato come ottenere un descrittore di sicurezza.


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

 

 