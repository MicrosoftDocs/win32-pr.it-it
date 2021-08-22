---
description: Fornisce regole per il mapping di classi WMI ad Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapping delle classi di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38e91d52b59a206a0b64465d0f9710f6d515c9487853824477b7f4f6a126aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992901"
---
# <a name="mapping-active-directory-classes"></a>Mapping delle classi di Active Directory

Poiché Active Directory dispone di un'ampia gamma di oggetti possibili, WMI non può creare un mapping diretto uno-a-uno. Il provider di servizi directory usa invece le regole per eseguire il mapping delle classi tra le due tecnologie.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Classi di mapping](#mapping-classes)
-   [Attributi di mapping](#mapping-attributes)
-   [Classi di associazione](#association-classes)

> [!Note]  
> Per altre informazioni sul supporto e sull'installazione di questo componente in un sistema operativo specifico, vedere Disponibilità del sistema [operativo dei componenti WMI.](operating-system-availability-of-wmi-components.md)

 

## <a name="mapping-classes"></a>Classi di mapping

Nell'elenco seguente vengono descritte le linee guida utilizzate dal provider di servizi directory per eseguire il mapping delle classi di Active Directory alle classi WMI:

-   Ogni classe astratta nello schema di Active Directory esegue il mapping a una classe astratta nello schema WMI.

    Nello schema WMI ogni classe astratta è preceduta dal prefisso DS \_ . Ad esempio, la **classe person** dello schema di Active Directory esegue il mapping alla classe WMI **person \_ DS.**

-   Ogni classe non astratta dallo schema di Active Directory esegue il mapping alle due classi seguenti nello schema WMI:

    -   La prima classe mappata è preceduta dal prefisso ADS \_ . Si tratta di classi astratte, mappate in base alle regole riportate di seguito.
    -   La seconda classe mappata è una classe non astratta con il prefisso del \_ nome DS. Questa classe è derivata dalla classe astratta \_ ADS, con l'aggiunta del [**qualificatore Provider.**](/windows/desktop/api/Provider/nl-provider-provider)

    Ad esempio, la **classe utente** dello schema di Active Directory esegue il mapping a due classi. La prima classe è la classe **astratta \_ dell'utente ADS,** mappata in base alle regole riportate di seguito. La seconda classe è la **classe DS \_ user** nonabstract. Deriva dall'utente **ADS \_ e** ha il qualificatore [**provider**](/windows/desktop/api/Provider/nl-provider-provider) aggiunto.

-   Se non specificato diversamente, il nome di una classe mappata è il valore danneggiato della proprietà **LDAP-Display-Name** nella classe Active Directory.
-   Se la **proprietà Sub-Class-Of** è presente nella classe Active Directory, la classe mappata a WMI viene derivata dalla classe specificata.

    Se la **proprietà Sub-Class-Of** non è presente, la classe mappata a WMI viene derivata dalla classe radice **\_ LDAP \_ \_ DS,** come specificato nel file MOF.

    > [!Note]  
    > Questa classe ha la **proprietà chiave ADSIPath,** con un **tipo VT \_ BSTR.** Si tratta del percorso ADSI univoco che identifica questa istanza. Active Directory supporta solo l'ereditarietà singola, quindi funziona.

     

-   Per **ogni classe** viene creato un qualificatore dinamico di tipo **VT \_ BOOL** e flavor impostato su `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` **TRUE.** Si tratta di un qualificatore WMI standard che indica che le istanze di questa classe vengono fornite in modo dinamico.
-   Se la classe non è astratta, il provider crea un qualificatore provider di tipo **VT \_ BSTR BOOL** e il qualificatore flavor impostato su [](/windows/desktop/api/Provider/nl-provider-provider) `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` "DS Instance Provider" per ogni classe. Si tratta di un qualificatore WMI standard che indica il nome del provider che fornisce dinamicamente istanze di questa classe.

Il resto delle proprietà ADSI viene mappato ai qualificatori di classe e alle proprietà in base alle tabelle seguenti. Tutti i qualificatori vengono mappati con un valore del flag di qualificatore pari a `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

Di seguito sono elencate le informazioni di mapping per la classe Active Directory, che mostrano il qualificatore WMI e il tipo di qualificatore WMI per ogni proprietà di Active Directory.

<dl> <dt>

**Nome comune**
</dt> <dd>

**CN** (**VT \_ BSTR**)

Mappato direttamente dal valore stringa.

</dd> <dt>

**Default-Object-Category**
</dt> <dd>

**DefaultObjectCategory** (**VT \_ BSTR**)

Mappato direttamente dal valore stringa.

</dd> <dt>

**Descrittore di sicurezza predefinito**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**)

Mappato direttamente dal valore stringa.

</dd> <dt>

**Governs-Id**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Mappato dalla rappresentazione di stringa dell'OID; ad esempio "{ 1 3 3 6 }".

</dd> <dt>

**Classe object**
</dt> <dd>

N/A

Non mappato.

</dd> <dt>

**Object-Class-Category**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Mappato direttamente dal valore intero. Inoltre, se il valore è Abstract(2), viene creato anche il qualificatore **CIM \_ BOOL standard,** denominato qualificatore **"Abstract".**

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Mappato dalla rappresentazione di stringa del valore OID. ad esempio "{ 1 3 3 6 }". Inoltre, la proprietà identificata qui viene annotata con il qualificatore **CIM** indicizzato standard impostato su **TRUE.**

</dd> <dt>

**Solo sistema**
</dt> <dd>

**SystemOnly** (**VT \_ BOOL**)

Mappato direttamente dal valore booleano.

</dd> </dl>

 

Di seguito sono elencate le proprietà della classe Active Directory mappate alle proprietà della classe WMI.

<dl> <dt>

**Può contenere**
</dt> <dd>

Ogni proprietà in questo elenco è mappata a una proprietà WMI.

</dd> <dt>

**Deve contenere**
</dt> <dd>

Ogni proprietà in questo elenco è mappata a una proprietà WMI. Per ognuno **\_ di questi viene** creato il qualificatore CIM non Null standard.

</dd> <dt>

**System-May-Contain**
</dt> <dd>

Ogni proprietà in questo elenco è mappata a una proprietà WMI. Inoltre, ogni proprietà viene annotata con un **qualificatore di** sistema, impostato su **TRUE.**

</dd> <dt>

**System-Must-Contain**
</dt> <dd>

Ogni proprietà in questo elenco è mappata a una proprietà WMI. Per ognuno **\_ di questi viene** creato il qualificatore CIM non Null standard. Inoltre, ogni proprietà viene annotata con un **qualificatore di** sistema, impostato su **TRUE.**

</dd> </dl>

## <a name="mapping-attributes"></a>Attributi di mapping

Il provider di servizi directory esegue il mapping di ogni attributo di una classe Active Directory a una proprietà della classe WMI corrispondente in base alle regole di questa sezione. In generale, il provider di servizi directory denota la proprietà WMI come versione modificata del **valore LDAP-Display-Name** dell'attributo Di Active Directory.

Se la proprietà di Active Directory **Is-Single-Valued** è **FALSE,** questa proprietà WMI viene combinata con l'operatore OR con **CIM \_ FLAG \_ ARRAY**. Si noti che ogni proprietà è contrassegnata con il qualificatore **\_ BSTR VT,** **ADSyntax.** Rappresenta la sintassi di Active Directory sottostante.

Nella tabella seguente viene elencato il mapping della sintassi di Active Directory al tipo di dati della proprietà WMI.



| Elemento Active Directory                                      | Tipo di dati WMI                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Punto di accesso**](/windows/desktop/ADSchema/s-object-access-point)            | **STRINGA \_ CIM**                                                         |
| [**Boolean**](/windows/desktop/ADSchema/s-boolean)                             | **CIM \_ BOOLEAN**                                                        |
| **Stringa senza distinzione tra maiuscole e minuscole**                                   | **STRINGA \_ CIM**                                                         |
| [**Stringa con distinzione tra maiuscole e minuscole**](/windows/desktop/ADSchema/s-string-case-sensitive) | **STRINGA \_ CIM**                                                         |
| [**Nome distinto**](/windows/desktop/ADSchema/s-object-ds-dn)             | **STRINGA \_ CIM**                                                         |
| [**DN-Binary**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Oggetto incorporato della classe **DN \_ con \_ binario** definito di seguito.<br/> |
| [**Stringa DN**](/windows/desktop/ADSchema/s-object-dn-string)                  | Oggetto incorporato della classe **DN \_ con la \_ stringa** definita di seguito.<br/> |
| [**Enumerazione**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM \_ SINT32**                                                         |
| [**Enumerazione**](/windows/desktop/ADSchema/s-enumeration)                     | **STRINGA \_ CIM**                                                         |
| [**Intero**](/windows/desktop/ADSchema/s-integer)                             | **CIM \_ SINT32**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **STRINGA \_ CIM**                                                         |
| Descrittore di sicurezza                                           | Oggetto incorporato della classe **Uint8Array definito** di seguito.<br/>       |
| Stringa numerica                                                | **STRINGA \_ CIM**                                                         |
| ID dell'oggetto.                                                     | **STRINGA \_ CIM**                                                         |
| Octet String                                                  | Oggetto incorporato della classe **Uint8Array definito** di seguito.<br/>       |
| OR Name                                                       | **STRINGA \_ CIM**                                                         |
| Presentation-Address                                          | Oggetto incorporato della classe **Uint8Array definito** di seguito.<br/>       |
| Stampa stringa maiuscole/minuscole                                             | **STRINGA \_ CIM**                                                         |
| Collegamento di replica                                                  | Oggetto incorporato della classe **Uint8Array definito** di seguito.<br/>       |
| [**String(Sid)**](/windows/desktop/ADSchema/s-string-sid)                      | Oggetto incorporato della classe **Uint8Array definito** di seguito.<br/>       |
| Ora                                                          | **CIM \_ DATETIME**                                                       |
| Ora UTC codificata                                                | **CIM \_ DATETIME**                                                       |
| Stringa Unicode                                                | **STRINGA \_ CIM**                                                         |



 

La sintassi Octet String, che fa riferimento a una matrice di valori **uint8,** presenta un problema quando viene eseguito il mapping a WMI perché WMI consente proprietà di tipo **uint8** e matrici di **uint8,** mentre Active Directory consente proprietà di tipo Octet String e matrici di Octet String.

Nell'esempio seguente viene illustrata la classe Del provider di servizi directory usata per eseguire il mapping di una matrice di proprietà di tipo Octet String.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI esegue il mapping di tutti i valori delle proprietà di Active Directory Octet String alle istanze incorporate di **Uint8Array.** Analogamente, WMI esegue il mapping delle matrici di Octet String alle matrici di **oggetti Uint8Array** incorporati.

Nell'esempio seguente vengono illustrate le classi mappate da WMI DN-Binary e DN-String proprietà DS.

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

La tabella seguente elenca il modo in cui WMI esegue il mapping delle altre proprietà dell'interfaccia dell'attributo di Active Directory ai qualificatori di proprietà WMI.



| Nome proprietà-attributo di Active Directory | Qualificatore WMI       | Tipo di dati    | Informazioni sul mapping                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Sintassi degli attributi**                     | **AttributeSyntax** | **VT \_ BSTR** | Mappato dalla rappresentazione di stringa dell'OID. |
| **Nome comune**                          | **Cn**              | **VT \_ BSTR** | Mappato dal valore stringa.                     |
| **Solo sistema**                          | **Sistema**          | **VT \_ BOOL** | Mappato dal valore booleano.                    |



 

> [!Note]  
> WMI esegue il mapping di tutti i qualificatori di Active Directory con `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` i tipi di qualificatori.

 

## <a name="association-classes"></a>Classi di associazione

Il servizio directory è essenzialmente un archivio gerarchico di oggetti. Gli oggetti che possono essere visualizzati a un livello non figlio nella gerarchia sono denominati "contenitori". La struttura di questa gerarchia è ulteriormente controllata dalle proprietà "Poss-Superiors" e "System-Poss-Superiors" di una classe nello schema. Queste, insieme, specificano il set di classi le cui istanze possono essere contenute all'interno di un'istanza di una classe contenitore.

Nell'esempio seguente viene modellata un'associazione CIM come istanze della classe di associazione [**statica DS \_ LDAP Class \_ \_ Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

Il provider della classe di associazione supporta [**i metodi GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) [**e CreateClassEnumAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)

 

