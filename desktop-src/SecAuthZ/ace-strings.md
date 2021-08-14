---
description: Illustra le stringhe usate in una voce di controllo di accesso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Stringhe ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60e8f4f5d3cd94f6e871b3b4962d2d548afa003c3bd4aa37a1ae8f008ce1a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785402"
---
# <a name="ace-strings"></a>Stringhe ACE

Il linguaggio SDDL (Security [Descriptor Definition Language)](security-descriptor-definition-language.md) usa stringhe ACE nei componenti DACL e SACL di una stringa [*del descrittore di*](/windows/desktop/SecGloss/s-gly) sicurezza.

Come illustrato negli esempi [di formato di stringa](security-descriptor-string-format.md) del descrittore di sicurezza, ogni ACE in una stringa del descrittore di sicurezza è racchiusa tra parentesi. I campi della ACE sono nell'ordine seguente e sono separati da punti e virgola (;).

> [!Note]  
> Esiste un formato diverso per le voci di [*controllo di*](/windows/desktop/SecGloss/a-gly) accesso condizionale (ACE) rispetto ad altri tipi di ACE. Per le ACE condizionali, vedere [Linguaggio di definizione del descrittore di sicurezza per le ACE condizionali.](security-descriptor-definition-language-for-conditional-aces-.md)

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Campi

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**tipo \_ ace**
</dt> <dd>

Stringa che indica il valore del membro **AceType** della [**struttura ACE \_ HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) La stringa di tipo ACE può essere una delle stringhe seguenti definite in Sddl.h.



| Stringa di tipo ACE | Costante in Sddl.h                      | Valore AceType                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "A"             | ACCESSO SDDL \_ \_ CONSENTITO                   | TIPO \_ DI \_ ACE CONSENTITO PER \_ L'ACCESSO                                                                                                                                         |
| "D"             | ACCESSO SDDL \_ \_ NEGATO                    | TIPO \_ \_ ACE NEGATO DI \_ ACCESSO                                                                                                                                          |
| "OA"            | ACCESSO AGLI OGGETTI SDDL \_ \_ \_ CONSENTITO           | ACCEDERE \_ AL TIPO DI \_ \_ ACE DELL'OGGETTO \_ CONSENTITO                                                                                                                                 |
| "OD"            | ACCESSO AGLI OGGETTI SDDL \_ \_ \_ NEGATO            | TIPO \_ DI \_ \_ ACE DELL'OGGETTO \_ ACCESSO NEGATO                                                                                                                                  |
| "AU"            | CONTROLLO \_ SDDL                             | TIPO \_ DI \_ ACE DI CONTROLLO DEL \_ SISTEMA                                                                                                                                           |
| "AL"            | ALLARME \_ SDDL                             | TIPO \_ DI \_ ACE SYSTEM ALARM \_                                                                                                                                           |
| "OU"            | CONTROLLO DEGLI OGGETTI \_ \_ SDDL                     | TIPO \_ \_ \_ ACE DELL'OGGETTO DI CONTROLLO DEL \_ SISTEMA                                                                                                                                   |
| "OL"            | AVVISO \_ DELL'OGGETTO SDDL \_                     | TIPO \_ \_ \_ ACE DELL'OGGETTO ACE SYSTEM \_ ALARM                                                                                                                                   |
| "ML"            | ETICHETTA OBBLIGATORIA \_ \_ SDDL                  | SYSTEM \_ MANDATORY \_ LABEL \_ ACE TYPE Windows Server \_ **2003:** Non disponibile.                                                                                        |
| "XA"            | ACCESSO DI CALLBACK SDDL \_ \_ \_ CONSENTITO         | ACCESS \_ ALLOWED \_ CALLBACK \_ ACE TYPE Windows Server \_ **2008, Windows Vista e Windows Server 2003:** Non disponibile.                                                |
| "XD"            | ACCESSO DI CALLBACK SDDL \_ \_ \_ NEGATO          | ACCESS \_ DENIED \_ CALLBACK \_ ACE TYPE Windows Server \_ **2008, Windows Vista e Windows Server 2003:** Non disponibile.                                                 |
| "RA"            | ATTRIBUTO DELLA RISORSA \_ \_ SDDL               | SYSTEM \_ RESOURCE \_ ATTRIBUTE \_ ACE TYPE Windows Server \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile.<br/> |
| "SP"            | ID CRITERI CON AMBITO SDDL \_ \_ \_                | SYSTEM \_ SCOPED \_ POLICY ID \_ \_ ACE TYPE Windows Server \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile.<br/>  |
| "XU"            | CONTROLLO CALLBACK \_ SDDL \_                   | SYSTEM \_ AUDIT \_ CALLBACK \_ ACE TYPE Windows Server \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile.<br/>     |
| "ZA"            | ACCESSO AGLI OGGETTI DI CALLBACK SDDL \_ \_ \_ \_ CONSENTITO | ACCESS \_ ALLOWED \_ CALLBACK \_ ACE TYPE Windows Server \_ **2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile.<br/>   |
| "TL"            | ETICHETTA DI \_ ATTENDIBILITÀ PROCESSO \_ SDDL \_             | SYSTEM \_ PROCESS TRUST LABEL \_ \_ \_ ACE TYPE \_ **Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile. |
| "FL"            | FILTRO DI \_ ACCESSO SDDL \_                    | SYSTEM \_ ACCESS \_ FILTER \_ ACE TYPE \_ **Windows Server 2016, Windows 10 versione 1607, Windows 10 versione 1511, Windows 10 versione 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile. |
 

> [!Note]  
> Se il tipo **\_ ace** è ACCESS ALLOWED OBJECT ACE TYPE e non è specificato alcun GUID oggetto né guid \_ \_ \_ \_ oggetto, [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converte **\_** **\_ \_** [](/windows/win32/api/guiddef/ns-guiddef-guid) **\_** il tipo ace in ACCESS ALLOWED \_ \_ ACE \_ TYPE.

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**flag \_ ace**
</dt> <dd>

Stringa che indica il valore del membro **AceFlags** della [**struttura ACE \_ HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) La stringa flag ACE può essere una concatenazione delle stringhe seguenti definite in Sddl.h.



| Stringa flag ACE | Costante in Sddl.h       | Valore AceFlag                 |
|------------------|--------------------------|-------------------------------|
| "CI"             | EREDITARIETÀ DEL \_ CONTENITORE \_ SDDL | ACE \_ EREDITA \_ CONTENITORE       |
| "OI"             | EREDITARIETÀ \_ DELL'OGGETTO \_ SDDL    | OBJECT \_ INHERIT \_ ACE          |
| "NP"             | SDDL \_ NO \_ PROPAGATE      | NO \_ PROPAGATE \_ INHERIT \_ ACE   |
| "IO"             | SOLO \_ EREDITARIETÀ \_ SDDL      | INHERIT \_ ONLY \_ ACE (EREDITA SOLO ACE)            |
| "ID"             | SDDL \_ EREDITATO          | ACE \_ EREDITATO                |
| "SA"             | CONTROLLO SDDL \_ \_ RIUSCITO     | \_FLAG \_ ACE DI \_ ACCESSO RIUSCITO |
| "FA"             | ERRORE DI CONTROLLO \_ \_ SDDL     | \_FLAG \_ ACE DI ACCESSO NON \_ RIUSCITO     |
| "TP"             | FILTRO PROTETTO CON \_ \_ ATTENDIBILITÀ \_ SDDL | TRUST \_ PROTECTED \_ FILTER \_ ACE FLAG \_ **Windows Server 2016, Windows 10 versione 1607, Windows 10 versione 1511, Windows 10 versione 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile. |
| "CR"             | SDDL \_ CRITICAL           | CRITICAL \_ ACE \_ FLAG Windows Server **versione 1803, Windows 10 versione 1803, Windows Server versione 1709, Windows 10 versione 1709, Windows 10 versione 1703, Windows Server 2016, Windows 10 versione 1607, Windows 10 versione 1511, Windows 10 versione 1507, Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Non disponibile. |
 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**Diritti**
</dt> <dd>

Stringa che indica i diritti [di accesso controllati](access-rights-and-access-masks.md) dalla ACE. Questa stringa può essere una rappresentazione di stringa esadecimale dei diritti di accesso, ad esempio "0x7800003F", oppure può essere una concatenazione delle stringhe seguenti.



### <a name="generic-access-rights"></a>Diritti di accesso generici

| Stringa dei diritti di accesso | Costante in Sddl.h | Valore diritto di accesso |
|----------------------|--------------------|--------------------|
| "GA"                 | TUTTI GENERICI SDDL \_ \_ | GENERIC \_ ALL       |
| "GR"                 | LETTURA GENERICA \_ \_ SDDL | LETTURA \_ GENERICA     |
| "GW"                 | SCRITTURA GENERICA \_ \_ SDDL | SCRITTURA \_ GENERICA |
| "GX"                 | ESECUZIONE GENERICA \_ SDDL \_ | ESECUZIONE \_ GENERICA |


### <a name="standard-access-rights"></a>Diritti di accesso standard

| Stringa dei diritti di accesso | Costante in Sddl.h | Valore diritto di accesso |
|----------------------|--------------------|--------------------|
| "RC"                 | CONTROLLO DI \_ LETTURA SDDL \_ | CONTROLLO \_ LETTURA      |
| "SD"                 | ELIMINAZIONE STANDARD \_ SDDL \_ | DELETE          |
| "WD"                 | Applicazione livello dati SDDL \_ WRITE \_ | APPLICAZIONE \_ LIVELLO DATI WRITE            |
| "WO"                 | PROPRIETARIO SCRITTURA \_ SDDL \_ | WRITE \_ OWNER        |

### <a name="directory-service-object-access-rights"></a>Diritti di accesso agli oggetti del servizio directory

| Stringa dei diritti di accesso | Costante in Sddl.h | Valore diritto di accesso |
|----------------------|--------------------|--------------------|
| "RP"                 | PROPRIETÀ READ DI \_ \_ SDDL | ACTIVE DIRECTORY \_ RIGHT \_ DS \_ READ \_ PROP |
| "WP"                 | PROPRIETÀ \_ WRITE \_ SDDL | ACTIVE DIRECTORY \_ RIGHT \_ DS \_ WRITE \_ PROP |
| "CC"                 | SDDL \_ CREATE \_ CHILD | ADS \_ RIGHT \_ DS \_ CREATE \_ CHILD |
| "DC"                 | SDDL \_ DELETE \_ CHILD | ADS \_ RIGHT \_ DS \_ DELETE \_ CHILD |
| "LC"                 | ELEMENTI FIGLIO \_ DELL'ELENCO SDDL \_ | ELENCO ADS \_ RIGHT \_ ACTRL \_ DS \_ |
| "SW"                 | SDDL \_ SELF \_ WRITE    | ADS \_ RIGHT \_ DS \_ SELF |
| "LO"                  | OGGETTO ELENCO \_ \_ SDDL | OGGETTO ELENCO DI \_ ACTIVE DIRECTORY \_ \_ RIGHT DS \_ |
| "DT"                 | ALBERO DI ELIMINAZIONE \_ \_ SDDL | ADS \_ RIGHT \_ DS \_ DELETE \_ TREE |
| "CR"                  | ACCESSO DI CONTROLLO \_ SDDL \_ | ADS \_ RIGHT \_ DS \_ CONTROL \_ ACCESS |

### <a name="file-access-rights"></a>Diritti di accesso ai file

| Stringa dei diritti di accesso | Costante in Sddl.h | Valore diritto di accesso |
|----------------------|--------------------|--------------------|
| "FA"                 | SDDL \_ FILE \_ ALL    | ACCESSO \_ A TUTTI I \_ FILE   |
| "FR"                 | LETTURA FILE \_ SDDL \_   | LETTURA \_ GENERICA \_ FILE |
| "FW"                 | SCRITTURA FILE \_ SDDL \_  | SCRITTURA \_ GENERICA \_ DI FILE |
| "FX"                 | ESECUZIONE DI FILE SDDL \_ \_ | ESECUZIONE \_ GENERICA \_ DI FILE |


### <a name="registry-key-access-rights"></a>Diritti di accesso alle chiavi del Registro di sistema

| Stringa dei diritti di accesso | Costante in Sddl.h | Valore diritto di accesso |
|----------------------|--------------------|--------------------|
| "KA"                 | CHIAVE SDDL \_ \_ ALL     | CHIAVE \_ ALL \_ ACCESS   |
| "KR"                 | SDDL \_ KEY \_ READ    | LETTURA \_ DELLA CHIAVE          |
| "KW"                 | SDDL \_ KEY \_ WRITE   | KEY \_ WRITE         |
| "KX"                 | ESECUZIONE DELLA CHIAVE SDDL \_ \_ | KEY \_ EXECUTE       |

### <a name="mandatory-label-rights"></a>Diritti di etichetta obbligatori

| Stringa dei diritti di accesso | Costante in Sddl.h | Valore del diritto di accesso |
|----------------------|--------------------|--------------------|
| "NR"                 | SDDL \_ NO \_ READ \_ UP | SYSTEM \_ MANDATORY LABEL NO READ UP Windows Server \_ \_ \_ \_ **2008, Windows Vista and Windows Server 2003:** Non disponibile. |
| "NW"                 | SDDL \_ NO \_ WRITE \_ UP | SYSTEM \_ MANDATORY LABEL NO WRITE UP Windows Server \_ \_ \_ \_ **2008, Windows Vista and Windows Server 2003:** Non disponibile. |
| "NX"                 | SDDL \_ NO \_ EXECUTE \_ UP | SYSTEM \_ MANDATORY LABEL NO EXECUTE UP Windows Server \_ \_ \_ \_ **2008, Windows Vista and Windows Server 2003:** Non disponibile. |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**GUID \_ oggetto**
</dt> <dd>

Rappresentazione di stringa di un GUID che indica il valore del membro **ObjectType** di una struttura ACE specifica dell'oggetto, ad esempio [**ACCESS ALLOWED OBJECT \_ \_ \_ ACE.**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) La stringa GUID usa il formato restituito [**dalla funzione UuidToString.**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring)

Nella tabella seguente sono elencati alcuni GUID di oggetti di uso comune.



| Diritti e GUID                         | Autorizzazione      |
|-----------------------------------------|-----------------|
| CR;ab721a53-1e2f-11d0-9819-00aa0040529b | Cambia password |
| CR;00299570-246d-11d0-a768-00aa006e0529 | Reimposta password  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**inherit \_ object \_ guid**
</dt> <dd>

Rappresentazione di stringa di un GUID che indica il valore del membro **InheritedObjectType** di una struttura ACE specifica dell'oggetto. La stringa GUID usa il [**formato UuidToString.**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring)

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**account \_ sid**
</dt> <dd>

[Stringa SID](sid-strings.md) che identifica il [trustee](trustees.md) della ACE.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**attributo \_ della risorsa**
</dt> <dd>

\[\]FACOLTATIVO \_ L'attributo della risorsa è solo per le voci ACE della risorsa ed è facoltativo. Stringa che indica il tipo di dati. Il tipo di dati ace dell'attributo della risorsa può essere uno dei tipi di dati seguenti definiti in Sddl.h.

Il segno \# " " è sinonimo di "0" negli attributi della risorsa. Ad esempio, D:AI(XA;OICI;FA;;; WD;(OctetStringType== 1 2 3 )) è equivalente e interpretato \# \# come \# \# \# D:AI(XA;OICI;FA;;; WD;(OctetStringType== \# 01020300)).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** Gli attributi della risorsa non sono disponibili.



| Stringa del tipo di dati ace dell'attributo risorsa | Costante in Sddl.h | Tipo di dati        |
|-----------------------------------------|--------------------|------------------|
| "TI"                                    | SDDL \_ INT          | Intero con segno   |
| "TU"                                    | SDDL \_ UINT         | Intero senza segno |
| "TS"                                    | SDDL \_ WSTRING      | Stringa wide      |
| "TD"                                    | SDDL \_ SID          | SID              |
| "TX"                                    | SDDL \_ BLOB         | Stringa ottetto     |
| "TB"                                    | VALORE BOOLEANO \_ SDDL      | Boolean          |



 

</dd> </dl>

Nell'esempio seguente viene illustrata una stringa ACE per una ACE consentita per l'accesso. Non si tratta di una ACE specifica dell'oggetto, quindi non contiene informazioni nel **\_ GUID** dell'oggetto ed **eredita i campi GUID \_ \_ dell'oggetto.** Anche **il campo flag \_ ace** è vuoto, a indicare che nessuno dei flag ACE è impostato.


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



La stringa ACE illustrata in precedenza descrive le informazioni ACE seguenti.


```C++
AceType:       0x00 (ACCESS_ALLOWED_ACE_TYPE)
AceFlags:      0x00
Access Mask:   0x100e003f
                    READ_CONTROL
                    WRITE_DAC
                    WRITE_OWNER
                    GENERIC_ALL
                    Other access rights(0x0000003f)
Ace Sid      : (S-1-1-0)
```



L'esempio seguente mostra un file classificato con attestazioni di risorse per Windows e Structured Query Language (SQL) con la proprietà Secrecy impostata su High Business Impact.


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



La stringa ACE illustrata in precedenza descrive le informazioni ACE seguenti.


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



Per altre informazioni, vedere [Security Descriptor String Format](security-descriptor-string-format.md) and [SID Strings](sid-strings.md). Per le ACE condizionali, vedere [Linguaggio di definizione del descrittore di sicurezza per ACE condizionali.](security-descriptor-definition-language-for-conditional-aces-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\[MS-DTYP: \] Linguaggio di descrizione del descrittore di sicurezza](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

