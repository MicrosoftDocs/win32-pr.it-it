---
description: Fornisce regole per il mapping delle classi WMI al Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Mapping di classi Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314596"
---
# <a name="mapping-active-directory-classes"></a>Mapping di classi Active Directory

Poiché Active Directory dispone di un'ampia gamma di oggetti possibili, WMI non è in grado di creare un mapping diretto uno a uno. Il provider di servizi directory utilizza invece regole per eseguire il mapping delle classi tra le due tecnologie.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Classi di mapping](#mapping-classes)
-   [Attributi di mapping](#mapping-attributes)
-   [Classi Association](#association-classes)

> [!Note]  
> Per ulteriori informazioni sul supporto e l'installazione di questo componente in un sistema operativo specifico, vedere la pagina relativa alla [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-classes"></a>Classi di mapping

Nell'elenco seguente vengono descritte le linee guida utilizzate dal provider di servizi directory per eseguire il mapping delle classi Active Directory alle classi WMI:

-   Ogni classe astratta nello schema Active Directory viene mappata a una classe astratta nello schema WMI.

    Nello schema WMI ogni classe astratta è preceduta da servizi di dominio Active Directory \_ . Ad esempio, la classe **Person** dello schema Active Directory viene mappata alla classe WMI **\_ Person DS** .

-   Ogni classe non astratta dello schema Active Directory viene mappata alle due classi seguenti nello schema WMI:

    -   La prima classe mappata è preceduta da ADS \_ . Si tratta di classi astratte, mappate in base alle regole indicate di seguito.
    -   La seconda classe mappata è una classe non astratta con il \_ prefisso del nome DS. Questa classe è derivata dalla \_ classe astratta ADS, con l'aggiunta del qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .

    Ad esempio, la classe **utente** dello schema Active Directory viene mappata a due classi. La prima classe è la classe astratta **\_ dell'utente ADS** , mappata in base alle regole indicate di seguito. La seconda classe è la classe non astratta dell' **\_ utente DS** . Viene derivato dall' **\_ utente ADS** ed è associato al qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) aggiunto.

-   Se non specificato diversamente, il nome di una classe mappata è il valore modificato della proprietà **LDAP-Display-Name** nella classe Active Directory.
-   Se la proprietà **Sub-Class-of** è presente nella classe Active Directory, la classe mappata a WMI viene derivata dalla classe specificata.

    Se la proprietà **della classe secondaria-of** non è presente, la classe mappata a WMI viene derivata dalla classe della classe **\_ \_ radice \_ LDAP DS** , come specificato nel file MOF.

    > [!Note]  
    > Questa classe dispone della proprietà della chiave **ADSIPath** , con un tipo **VT \_ BSTR**. Si tratta del percorso ADSI univoco che identifica questa istanza. Active Directory supporta solo l'ereditarietà singola, quindi funziona.

     

-   Un qualificatore **dinamico** di tipo **VT \_ bool** e Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` impostato su **true** viene creato per ogni classe. Si tratta di un qualificatore WMI standard che indica che le istanze di questa classe vengono fornite dinamicamente.
-   Se la classe non è astratta, il provider crea un qualificatore del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) di tipo **VT \_ BSTR bool** e Qualifier Flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` impostati su "DS instance provider" per ogni classe. Qualificatore WMI standard che indica il nome del provider che fornisce dinamicamente le istanze di questa classe.

Il resto delle proprietà ADSI viene mappato a qualificatori di classe e proprietà in base alle tabelle seguenti. Tutti i qualificatori vengono mappati con un valore del flag di qualificatore `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

Di seguito sono elencate le informazioni di mapping per la classe Active Directory, che mostra il qualificatore WMI e il tipo di qualificatore WMI per ogni proprietà Active Directory.

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

**Governas-ID**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Mappato dalla rappresentazione di stringa dell'OID; ad esempio, "{1 3 3 6}".

</dd> <dt>

**Classe Object**
</dt> <dd>

N/D

Non mappato.

</dd> <dt>

**Classe Object-Category**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Mappato direttamente dal valore intero. Inoltre, se il valore è abstract (2), viene creato anche il qualificatore standard di **VT \_ bool** CIM, denominato qualificatore **"abstract"** .

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Mappato dalla rappresentazione di stringa del valore OID; ad esempio, "{1 3 3 6}". Inoltre, la proprietà identificata qui viene annotata con il qualificatore CIM **indicizzato** standard impostato su **true**.

</dd> <dt>

**Solo sistema**
</dt> <dd>

**SystemOnly** (**VT \_ bool**)

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

Ogni proprietà in questo elenco è mappata a una proprietà WMI. Per ognuno di questi, viene creato il qualificatore CIM standard **Not \_ null** .

</dd> <dt>

**Sistema-può contenere**
</dt> <dd>

Ogni proprietà in questo elenco è mappata a una proprietà WMI. Inoltre, ogni proprietà viene annotata con un qualificatore di **sistema** , impostato su **true**.

</dd> <dt>

**System-must-contain**
</dt> <dd>

Ogni proprietà in questo elenco è mappata a una proprietà WMI. Per ognuno di questi, viene creato il qualificatore CIM standard **Not \_ null** . Inoltre, ogni proprietà viene annotata con un qualificatore di **sistema** , impostato su **true**.

</dd> </dl>

## <a name="mapping-attributes"></a>Attributi di mapping

Il provider di servizi directory esegue il mapping di ogni attributo di una classe Active Directory esattamente a una proprietà della classe WMI corrispondente in base alle regole di questa sezione. In generale, il provider di servizi directory denomina la proprietà WMI come versione alterata del valore **LDAP-Display-Name** dell'attributo Active Directory.

Se la proprietà Active Directory **è a valore singolo** è **false**, questa proprietà WMI viene combinata con l'operatore OR con la **matrice di \_ flag \_ CIM**. Si noti che ogni proprietà è contrassegnata con il qualificatore **\_ BSTR VT** , **ADSyntax**. Rappresenta la sintassi del Active Directory sottostante.

Nella tabella seguente viene elencato il mapping della sintassi Active Directory al tipo di dati della proprietà WMI.



| Elemento Active Directory                                      | Tipo di dati WMI                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Punto di accesso**](/windows/desktop/ADSchema/s-object-access-point)            | **\_stringa CIM**                                                         |
| [**Boolean**](/windows/desktop/ADSchema/s-boolean)                             | **\_valore booleano CIM**                                                        |
| **Stringa senza distinzione tra maiuscole e minuscole**                                   | **\_stringa CIM**                                                         |
| [**Stringa distinzione tra maiuscole e minuscole**](/windows/desktop/ADSchema/s-string-case-sensitive) | **\_stringa CIM**                                                         |
| [**Nome distinto**](/windows/desktop/ADSchema/s-object-ds-dn)             | **\_stringa CIM**                                                         |
| [**DN-binario**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Oggetto incorporato della classe **DN \_ con \_ binario** definito di seguito.<br/> |
| [**Stringa DN**](/windows/desktop/ADSchema/s-object-dn-string)                  | Oggetto incorporato della classe **DN \_ con la \_ stringa** definita di seguito.<br/> |
| [**Enumerazione**](/windows/desktop/ADSchema/s-enumeration)                     | **\_SINT32 CIM**                                                         |
| [**Enumerazione**](/windows/desktop/ADSchema/s-enumeration)                     | **\_stringa CIM**                                                         |
| [**Integer**](/windows/desktop/ADSchema/s-integer)                             | **\_SINT32 CIM**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **\_stringa CIM**                                                         |
| Descrittore di sicurezza                                           | Oggetto incorporato della classe **Uint8Array** definito di seguito.<br/>       |
| Stringa numerica                                                | **\_stringa CIM**                                                         |
| ID dell'oggetto.                                                     | **\_stringa CIM**                                                         |
| Stringa ottetto                                                  | Oggetto incorporato della classe **Uint8Array** definito di seguito.<br/>       |
| O nome                                                       | **\_stringa CIM**                                                         |
| Presentation-Address                                          | Oggetto incorporato della classe **Uint8Array** definito di seguito.<br/>       |
| Stringa del case di stampa                                             | **\_stringa CIM**                                                         |
| Collegamento replica                                                  | Oggetto incorporato della classe **Uint8Array** definito di seguito.<br/>       |
| [**Stringa (SID)**](/windows/desktop/ADSchema/s-string-sid)                      | Oggetto incorporato della classe **Uint8Array** definito di seguito.<br/>       |
| Tempo                                                          | **\_DateTime CIM**                                                       |
| Ora codificata UTC                                                | **\_DateTime CIM**                                                       |
| Stringa Unicode                                                | **\_stringa CIM**                                                         |



 

La sintassi della stringa di ottetto, che fa riferimento a una matrice di valori **Uint8** , presenta un problema quando viene eseguito il mapping a WMI, perché WMI consente le proprietà dei tipi **Uint8** e le matrici di **Uint8**, mentre Active Directory consente le proprietà di tipo stringa ottetto, nonché matrici di stringa ottetto.

Nell'esempio seguente viene illustrata la classe del provider di servizi directory utilizzata per eseguire il mapping di una matrice di proprietà di tipo stringa ottetto.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI esegue il mapping di tutte le stringhe ottetto Active Directory valori di proprietà a istanze incorporate di **Uint8Array**. Analogamente, WMI esegue il mapping di matrici di stringa ottetto a matrici di oggetti **Uint8Array** incorporati.

Nell'esempio seguente vengono illustrate le classi di cui è stato eseguito il mapping da WMI per DN-Binary e DN-String i valori delle proprietà DS.

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

Nella tabella seguente viene elencato il mapping tra il resto delle proprietà dell'interfaccia dell'attributo Active Directory e i qualificatori di proprietà WMI.



| Attributo Active Directory-nome proprietà | Qualificatore WMI       | Tipo di dati    | Informazioni sul mapping                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Sintassi degli attributi**                     | **AttributeSyntax** | **\_BSTR VT** | Mappato dalla rappresentazione di stringa dell'OID. |
| **Nome comune**                          | **CN**              | **\_BSTR VT** | Mappata dal valore stringa.                     |
| **Solo sistema**                          | **Sistema**          | **\_bool VT** | Mappato da un valore booleano.                    |



 

> [!Note]  
> WMI esegue il mapping di tutti i qualificatori di Active Directory con le `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` versioni del qualificatore.

 

## <a name="association-classes"></a>Classi Association

Il servizio directory è essenzialmente un archivio gerarchico di oggetti. Gli oggetti che possono essere visualizzati a un livello non foglia nella gerarchia sono detti "contenitori". La struttura di questa gerarchia è ulteriormente controllata dalle proprietà "poss-superiors" e "System-poss-superiors" di una classe nello schema. Insieme, specificano il set di classi le cui istanze possono essere contenute all'interno di un'istanza di una classe contenitore.

Nell'esempio seguente viene modellata un'associazione CIM come istanza della classe di associazione statica di [**dominio DS \_ \_ \_ contenuto della classe LDAP**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).

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

Il provider della classe Association supporta i metodi [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) e [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .

 

