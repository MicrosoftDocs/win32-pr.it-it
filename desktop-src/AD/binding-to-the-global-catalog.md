---
title: Associazione al catalogo globale
description: Il catalogo globale è uno spazio dei nomi che contiene i dati della directory per tutti i domini in una foresta.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Associazione ad ACTIVE Directory del catalogo globale
- catalogo globale AD, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d094a0c07a40fa063b726d0ba1c5a15977873d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881643"
---
# <a name="binding-to-the-global-catalog"></a>Associazione al catalogo globale

Il catalogo globale è uno spazio dei nomi che contiene i dati della directory per tutti i domini in una foresta. Il catalogo globale contiene una replica parziale di ogni directory di dominio. Contiene una voce per ogni oggetto nella foresta aziendale, ma non contiene tutte le proprietà di ogni oggetto. Contiene invece solo le proprietà specificate per l'inclusione nel catalogo globale.

Il catalogo globale viene archiviato in server specifici in tutta l'organizzazione. Solo i controller di dominio possono fungere da server di catalogo globale. Gli amministratori indicano se un determinato controller di dominio contiene un catalogo globale tramite Active Directory Sites and Services Manager.

Per eseguire l'associazione al catalogo globale con ADSI, usare il moniker "GC:".

Esistono due modi per eseguire l'associazione al catalogo globale per eseguire una ricerca in una foresta:

-   Eseguire il binding all'oggetto radice dell'organizzazione per eseguire la ricerca in tutti i domini nella foresta.
-   Eseguire l'associazione a un oggetto specifico per cercare l'oggetto e i relativi elementi figlio. Ad esempio, se si esegue l'associazione a un dominio che ha due domini sottostanti in un albero di dominio nella foresta, è possibile eseguire ricerche in questi tre domini. Tenere presente che il nome distinto per l'oggetto a cui eseguire l'associazione corrisponde esattamente al nome distinto usato per l'associazione allo spazio dei nomi "LDAP:". Tenere presente che "LDAP:" è una replica completa di un singolo dominio e che "GC:" è una replica parziale di tutti i domini nella foresta.

Come per il moniker "LDAP:", è possibile usare l'associazione serverless o l'associazione a un server di catalogo globale specifico. Se si esegue una ricerca nella foresta corrente, usare l'associazione serverless. Tuttavia, se si esegue una ricerca in un'altra foresta, specificare un nome di dominio o un server di catalogo globale a cui eseguire l'associazione, come illustrato negli esempi seguenti.

Eseguire il binding usando il nome di dominio:

``` syntax
GC://fabrikam.com
```

Eseguire il binding usando il nome del server:

``` syntax
GC://servername
```

È anche possibile eseguire l'associazione a un oggetto specifico all'interno del catalogo globale. Per eseguire l'associazione all'oggetto sales nel dominio fabrikam, usare il formato seguente.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

In caso contrario, per eseguire l'associazione all'oggetto sales nel server, usare il formato seguente.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**Per eseguire ricerche nell'intera foresta**

1.  Eseguire l'associazione alla radice dello spazio dei nomi del catalogo globale.
2.  Enumerare il contenitore del catalogo globale. Il contenitore catalogo globale contiene un singolo oggetto che è possibile usare per eseguire ricerche nell'intera foresta.
3.  Usare l'oggetto nel contenitore per eseguire la ricerca. In C/C++ chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) sull'oggetto in modo che sia possibile usare l'interfaccia **IDirectorySearch** per eseguire la ricerca. In Visual Basic usare l'oggetto restituito dall'enumerazione nella query ADO.

Per enumerare i server di catalogo globale in un sito, eseguire una ricerca nel sottoalbero LDAP di "cn= &lt; yoursite &gt; ,cn=sites, ", usando la <DN of the configurationNamingContext> stringa di filtro seguente.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Questo filtro usa l'operatore della regola di corrispondenza **LDAP MATCHING RULE BIT \_ \_ \_ \_ AND** (1.2.840.113556.1.4.803) per trovare gli oggetti **nTDSDSA** con il bit di ordine più basso impostato nella maschera di bit dell'attributo **options.** Il bit meno importante, che corrisponde alla costante **GC NTDSDSA \_ OPT \_ \_ IS** definita in Ntdsapi.h, identifica l'oggetto **nTDSDSA** di un server di catalogo globale. Per altre informazioni sulle regole di corrispondenza, vedere [Sintassi del filtro di ricerca.](/windows/desktop/ADSI/search-filter-syntax)

L'elemento padre **dell'oggetto nTDSDSA** è l'oggetto server e la proprietà **dNSHostName** dell'oggetto server è il nome DNS del server di catalogo globale.

Non è possibile usare \# costanti define come **NTDSDSA \_ OPT IS \_ \_ GC** e **LDAP MATCHING RULE BIT \_ \_ \_ \_ AND** direttamente in una stringa di filtro di ricerca. È tuttavia possibile usare queste costanti come argomenti per una funzione, ad esempio [**swprintf \_ s,**](/windows/win32/api/winuser/nf-winuser-wsprintfa) per inserire i valori costanti in una stringa di filtro.

Il catalogo globale non rappresenta l'intera struttura ad albero della foresta. Ad esempio, si potrebbe prevedere che l'esempio di codice seguente enumera tutti i domini nella foresta e tutti gli oggetti figlio di ogni dominio. In realtà, ciò che effettivamente fa è enumerare tutti i domini nella foresta, ma nessuno degli oggetti dominio enumerati contiene elementi figlio. Si tratta di una limitazione del catalogo globale.


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



Per risolvere questo problema, è necessario eseguire l'associazione a ogni oggetto di dominio e quindi enumerare gli oggetti figlio di ogni dominio. La tecnica appropriata è illustrata nell'esempio di codice seguente.


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



Per altre informazioni ed esempi di codice che illustrano come eseguire ricerche in un'intera foresta, vedere [Codice di esempio per la ricerca di una foresta.](example-code-for-searching-a-forest.md)

 

 
