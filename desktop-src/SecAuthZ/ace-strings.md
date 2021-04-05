---
description: Vengono illustrate le stringhe utilizzate in una voce di controllo di accesso.
ms.assetid: 82c99170-784b-4724-a25b-2f2e8a2e0225
title: Stringhe ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a35bde18a1ca3ac416faa42e3b693e26305beb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756186"
---
# <a name="ace-strings"></a>Stringhe ACE

Il [linguaggio SDDL (Security Descriptor Definition Language](security-descriptor-definition-language.md) ) utilizza stringhe ACE nei componenti DACL e SACL di una stringa del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) .

Come illustrato negli esempi di [formato della stringa del descrittore di sicurezza](security-descriptor-string-format.md) , ogni voce ACE in una stringa del descrittore di sicurezza è racchiusa tra parentesi. I campi della voce ACE sono nell'ordine seguente e sono separati da punti e virgola (;).

> [!Note]  
> È disponibile un formato diverso per le [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) condizionale (ACE) rispetto ad altri tipi ACE. Per le voci ACE condizionali, vedere [Security Descriptor Definition Language per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md).

 

``` syntax
ace_type;ace_flags;rights;object_guid;inherit_object_guid;account_sid;(resource_attribute)
```

## <a name="fields"></a>Campi

<dl> <dt>

<span id="ace_type"></span><span id="ACE_TYPE"></span>**\_tipo ACE**
</dt> <dd>

Stringa che indica il valore del membro **AceType** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . La stringa di tipo ACE può essere una delle stringhe seguenti definite in SDDL. h.



| Stringa di tipo ACE | Costante in SDDL. h                      | Valore AceType                                                                                                                                                      |
|-----------------|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "A"             | \_accesso SDDL \_ consentito                   | \_ \_ tipo ACE consentito per l'accesso \_                                                                                                                                         |
| "D"             | \_accesso SDDL \_ negato                    | \_ \_ tipo ACE accesso \_ negato                                                                                                                                          |
| OA            | \_ \_ accesso agli oggetti SDDL \_ consentito           | \_ \_ \_ tipo ACE oggetto consentito \_ Access                                                                                                                                 |
| OD            | \_ \_ accesso agli oggetti SDDL \_ negato            | ACCESSO \_ negato \_ \_ tipo ACE \_ oggetto                                                                                                                                  |
| Au            | \_controllo SDDL                             | \_ \_ tipo ACE controllo \_ sistema                                                                                                                                           |
| "AL"            | \_allarme SDDL                             | \_ \_ tipo ACE allarme \_ sistema                                                                                                                                           |
| UNITÀ organizzativa            | \_controllo oggetto \_ SDDL                     | \_ \_ \_ tipo ACE oggetto controllo \_ di sistema                                                                                                                                   |
| OL            | \_allarme oggetto \_ SDDL                     | \_ \_ \_ tipo ACE oggetto allarme \_ sistema                                                                                                                                   |
| ML            | \_etichetta SDDL obbligatoria \_                  | \_ \_ \_ tipo ACE etichetta obbligatoria \_ del sistema                                                                                                                                |
| XA            | \_accesso callback \_ SDDL \_ consentito         | ACCESSO \_ consentito \_ \_ tipo ACE \_ **di callback windows vista e Windows Server 2003:** non disponibile.<br/>                                                           |
| XD            | \_accesso callback \_ SDDL \_ negato          | ACCESSO \_ negato \_ \_ tipo ACE \_ **di callback windows vista e Windows Server 2003:** non disponibile.<br/>                                                            |
| RA            | \_attributo risorsa \_ SDDL               | \_ \_ Tipo ACE attributo risorsa di sistema \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** non disponibile.<br/> |
| SP            | \_ \_ ID criterio con ambito \_ SDDL                | \_ \_ ID dei criteri con ambito di sistema \_ \_ \_ -tipo ACE **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista e Windows Server 2003:** non disponibile.<br/>  |
| Xu            | \_controllo callback \_ SDDL                   | \_ \_ Tipo ACE di callback controllo di sistema \_ \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** non disponibile.<br/>     |
| ZA            | \_ \_ accesso agli oggetti di callback SDDL \_ \_ consentito | ACCESSO \_ consentito \_ di \_ tipo ACE di CALLBACK \_ **Windows Server 2008 R2, windows 7, Windows Server 2008, windows vista e Windows Server 2003:** non disponibile.<br/>   |



 

> [!Note]  
> Se **il \_ tipo ACE** è \_ \_ \_ un tipo ACE oggetto consentito \_ e nessun GUID **oggetto \_** né GUID **\_ \_ oggetto ereditano** un [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) specificato, [**ConvertStringSecurityDescriptorToSecurityDescriptor ha**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) converte **il \_ tipo ACE** per accedere al \_ \_ tipo ACE consentito \_ .

 

</dd> <dt>

<span id="ace_flags"></span><span id="ACE_FLAGS"></span>**\_flag ACE**
</dt> <dd>

Stringa che indica il valore del membro **AceFlags** della struttura dell' [**\_ intestazione ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . La stringa di flag ACE può essere una concatenazione delle stringhe seguenti definite in SDDL. h.



| Stringa flag ACE | Costante in SDDL. h       | Valore AceFlag                 |
|------------------|--------------------------|-------------------------------|
| Ci             | \_eredita il contenitore SDDL \_ | il contenitore \_ eredita \_ ACE       |
| OI             | \_oggetto SDDL \_ ereditato    | OGGETTO che \_ eredita \_ ACE          |
| NP             | SDDL \_ senza \_ propagazione      | Nessuna \_ propagazione \_ eredita \_ ACE   |
| Io             | \_solo SDDL eredita \_      | EREDITA \_ solo \_ ACE            |
| "ID"             | SDDL \_ ereditato          | Ace EREDITAta \_                |
| SA             | \_controllo SDDL \_ riuscito     | \_ \_ flag ACE di accesso riuscito \_ |
| FA             | \_errore di controllo SDDL \_     | \_ \_ flag ACE di accesso non riuscito \_     |



 

</dd> <dt>

<span id="rights"></span><span id="RIGHTS"></span>**diritti**
</dt> <dd>

Stringa che indica i [diritti di accesso](access-rights-and-access-masks.md) controllati dalla voce ACE. Questa stringa può essere una rappresentazione di stringa esadecimale dei diritti di accesso, ad esempio "0x7800003F", oppure può essere una concatenazione delle stringhe seguenti.



### <a name="generic-access-rights"></a>Diritti di accesso generici

| Stringa dei diritti di accesso | Costante in SDDL. h | Valore di accesso a destra |
|----------------------|--------------------|--------------------|
| GA                 | \_ \_ tutti i Generic SDDL | tutti GENERIci \_       |
| GR                 | \_lettura generica SDDL \_ | lettura GENERIca \_     |
| GW                 | \_scrittura generica SDDL \_ | scrittura GENERIca \_ |
| GX                 | \_esecuzione generica SDDL \_ | esecuzione GENERIca \_ |


### <a name="standard-access-rights"></a>Diritti di accesso standard

| Stringa dei diritti di accesso | Costante in SDDL. h | Valore di accesso a destra |
|----------------------|--------------------|--------------------|
| RC                 | \_controllo di lettura SDDL \_ | controllo di lettura \_      |
| SD                 | \_eliminazione standard \_ SDDL | DELETE          |
| WD                 | \_DAC scrittura \_ SDDL | Scrivi \_ DAC            |
| Wo                 | \_proprietario scrittura \_ SDDL | Scrivi \_ proprietario        |

### <a name="directory-service-object-access-rights"></a>Diritti di accesso agli oggetti del servizio directory

| Stringa dei diritti di accesso | Costante in SDDL. h | Valore di accesso a destra |
|----------------------|--------------------|--------------------|
| RP                 | \_proprietà di lettura SDDL \_ | ADS \_ Rights \_ DS \_ Read \_ prop |
| WP                 | \_Proprietà scrittura \_ SDDL | ADS \_ Rights \_ Write DS- \_ \_ prop |
| CC                 | SDDL \_ Crea \_ figlio | ADS \_ Rights \_ DS \_ creazione \_ figlio |
| DC                 | \_eliminazione \_ elemento figlio SDDL | ADS \_ Rights \_ DS \_ Delete \_ figlio |
| LC                 | \_elenco \_ elementi figlio SDDL | elenco degli annunci \_ giusti \_ ACTRL \_ DS \_ |
| SW                 | \_scrittura automatica \_ SDDL    | \_autonomi \_ DS \_ giusti |
| LO                  | \_oggetto elenco \_ SDDL | \_ \_ \_ oggetto elenco DS destro \_ ADS |
| DT                 | \_Elimina \_ albero SDDL | \_albero di \_ \_ eliminazione DS destro Ads \_ |
| CR                  | \_ \_ accesso al controllo SDDL | \_ \_ \_ accesso al controllo DS Rights Ads \_ |

### <a name="file-access-rights"></a>Diritti di accesso ai file

| Stringa dei diritti di accesso | Costante in SDDL. h | Valore di accesso a destra |
|----------------------|--------------------|--------------------|
| FA                 | \_ \_ tutti i file SDDL    | \_accesso a tutti i file \_   |
| FR                 | \_lettura file \_ SDDL   | \_lettura file generica \_ |
| FW                 | \_scrittura file \_ SDDL  | \_scrittura generica file \_ |
| FX                 | \_esecuzione file \_ SDDL | \_esecuzione generica file \_ |


### <a name="registry-key-access-rights"></a>Diritti di accesso alla chiave del registro di sistema

| Stringa dei diritti di accesso | Costante in SDDL. h | Valore di accesso a destra |
|----------------------|--------------------|--------------------|
| Ka                 | \_chiave SDDL \_ All     | CHIAVE \_ tutti gli \_ accessi   |
| KR                 | \_lettura chiave \_ SDDL    | \_lettura chiave          |
| KW                 | \_scrittura chiave \_ SDDL   | \_scrittura chiave         |
| Kx                 | \_esecuzione della chiave SDDL \_ | esecuzione della chiave \_       |

### <a name="mandatory-label-rights"></a>Diritti etichetta obbligatoria

| Stringa dei diritti di accesso | Costante in SDDL. h | Valore di accesso a destra |
|----------------------|--------------------|--------------------|
| Nr                 | SDDL \_ Nessuna \_ lettura \_ | \_etichetta obbligatoria \_ sistema \_ senza \_ lettura \_ |
| NW                 | SDDL \_ senza \_ scrittura \_ | \_etichetta obbligatoria \_ sistema \_ senza \_ scrittura \_ |
| NX                 | SDDL \_ Nessuna \_ esecuzione \_ | \_etichetta obbligatoria del sistema \_ \_ Nessuna \_ esecuzione \_ |
</dd> <dt>

<span id="object_guid"></span><span id="OBJECT_GUID"></span>**\_GUID oggetto**
</dt> <dd>

Rappresentazione in forma di stringa di un GUID che indica il valore del membro **ObjectType** di una struttura Ace specifica dell'oggetto, ad esempio [**Access \_ allowed \_ Object \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace). La stringa GUID usa il formato restituito dalla funzione [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

Nella tabella seguente sono elencati alcuni GUID oggetto usati comunemente.



| Diritti e GUID                         | Autorizzazione      |
|-----------------------------------------|-----------------|
| CR; ab721a53-1e2f-11D0-9819-00aa0040529b | Cambia password |
| CR; 00299570-246d-11D0-A768-00aa006e0529 | Reimposta password  |



 

</dd> <dt>

<span id="inherit_object_guid"></span><span id="INHERIT_OBJECT_GUID"></span>**eredita \_ \_ GUID oggetto**
</dt> <dd>

Rappresentazione in forma di stringa di un GUID che indica il valore del membro **InheritedObjectType** di una struttura Ace specifica dell'oggetto. La stringa GUID usa il formato [**UuidToString**](/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring) .

</dd> <dt>

<span id="account_sid"></span><span id="ACCOUNT_SID"></span>**SID dell'account \_**
</dt> <dd>

[Stringa SID](sid-strings.md) che identifica il [trustee](trustees.md) della voce ACE.

</dd> <dt>

<span id="resource_attribute"></span><span id="RESOURCE_ATTRIBUTE"></span>**\_attributo Resource**
</dt> <dd>

\[FACOLTATIVO \] l'attributo della risorsa \_ è solo per le voci ACE della risorsa ed è facoltativo. Stringa che indica il tipo di dati. Il tipo di dati ACE dell'attributo di risorsa può essere uno dei tipi di dati seguenti definiti in SDDL. h.

Il \# segno "" è sinonimo di "0" negli attributi delle risorse. Ad esempio, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) equivale a e interpretato come D:ai (XA; OICI; fa;;; WD; (OctetStringType = = \# 01020300)).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista e Windows server 2003:** Gli attributi della risorsa non sono disponibili.



| Stringa tipo di dati Ace attributo risorsa | Costante in SDDL. h | Tipo di dati        |
|-----------------------------------------|--------------------|------------------|
| TI                                    | SDDL \_ int          | Intero con segno   |
| TU                                    | SDDL \_ uint         | Intero senza segno |
| TS                                    | \_WSTRING SDDL      | Stringa estesa      |
| TD                                    | \_SID SDDL          | SID              |
| TX                                    | \_BLOB SDDL         | Stringa ottetto     |
| TB                                    | \_valore booleano SDDL      | Boolean          |



 

</dd> </dl>

Nell'esempio seguente viene illustrata una stringa ACE per una voce ACE consentita per l'accesso. Non si tratta di una voce ACE specifica dell'oggetto, quindi non contiene alcuna informazione **nel \_ GUID oggetto** e eredita i campi **\_ \_ GUID oggetto** . Anche il campo dei **\_ flag ACE** è vuoto, a indicare che non è stato impostato nessuno dei flag ACE.


```C++
(A;;RPWPCCDCLCSWRCWDWOGA;;;S-1-1-0)
```



La stringa ACE illustrata sopra descrive le informazioni ACE seguenti.


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



Nell'esempio seguente viene illustrato un file classificato con attestazioni di risorse per Windows e Structured Query Language (SQL) con segretezza impostata su un livello aziendale elevato.


```C++
(RA;CI;;;;S-1-1-0; ("Project",TS,0,"Windows","SQL")) 
(RA;CI;;;;S-1-1-0; ("Secrecy",TU,0,3))
```



La stringa ACE illustrata sopra descrive le informazioni ACE seguenti.


```C++
AceType:       0x12 (SYSTEM_RESOURCE_ATTRIBUTE_ACE_TYPE)
AceFlags:      0x1  (SDDL_CONTAINER_INHERIT)
Access Mask:   0x0
Ace Sid      : (S-1-1-0)
Resource Attributes: Project has the strings Windows and SQL, Secrecy has the unsigned int value of 3
```



Per altre informazioni, vedere [formato stringa del descrittore di sicurezza](security-descriptor-string-format.md) e [stringhe SID](sid-strings.md). Per le voci ACE condizionali, vedere [Security Descriptor Definition Language per le ACE condizionali](security-descriptor-definition-language-for-conditional-aces-.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\[MS-DTYP \] : Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

