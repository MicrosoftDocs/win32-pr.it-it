---
title: Associazione al catalogo globale
description: Il catalogo globale è uno spazio dei nomi che contiene i dati di directory per tutti i domini in una foresta.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Associazione al catalogo globale AD
- ANNUNCIO globale del catalogo, associazione a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046555"
---
# <a name="binding-to-the-global-catalog"></a>Associazione al catalogo globale

Il catalogo globale è uno spazio dei nomi che contiene i dati di directory per tutti i domini in una foresta. Il catalogo globale contiene una replica parziale di ogni directory di dominio. Contiene una voce per ogni oggetto nella foresta aziendale, ma non contiene tutte le proprietà di ogni oggetto. Contiene invece solo le proprietà specificate per l'inclusione nel catalogo globale.

Il catalogo globale viene archiviato in server specifici nell'intera organizzazione. Solo i controller di dominio possono fungere da server di catalogo globale. Gli amministratori indicano se un determinato controller di dominio dispone di un catalogo globale usando il Active Directory gestione siti e servizi.

Per eseguire l'associazione al catalogo globale con ADSI, usare il moniker "GC:".

Esistono due modi per eseguire l'associazione al catalogo globale per eseguire una ricerca in una foresta:

-   Eseguire l'associazione all'oggetto radice aziendale per eseguire la ricerca in tutti i domini della foresta.
-   Eseguire l'associazione a un oggetto specifico per eseguire la ricerca dell'oggetto e dei relativi elementi figlio. Se ad esempio si esegue l'associazione a un dominio con due domini sotto di esso in un albero di dominio nella foresta, è possibile eseguire ricerche in questi tre domini. Tenere presente che il nome distinto dell'oggetto a cui eseguire l'associazione è identico a quello del nome distinto utilizzato per l'associazione allo spazio dei nomi "LDAP:". Si ricordi che "LDAP:" è una replica completa di un singolo dominio e che "GC:" è una replica parziale di tutti i domini della foresta.

Come per il moniker "LDAP:", è possibile usare il binding senza server o eseguire il binding a un server di catalogo globale specifico. Se si esegue la ricerca nella foresta corrente, utilizzare un'associazione senza server. Tuttavia, se si esegue la ricerca in un'altra foresta, specificare un nome di dominio o un server di catalogo globale a cui eseguire l'associazione, come illustrato negli esempi seguenti.

Associa usando il nome di dominio:

``` syntax
GC://fabrikam.com
```

Associa utilizzando il nome del server:

``` syntax
GC://servername
```

È anche possibile eseguire l'associazione a un oggetto specifico all'interno del catalogo globale. Per eseguire l'associazione all'oggetto Sales nel dominio fabrikam, utilizzare il formato seguente.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

In alternativa, per eseguire l'associazione all'oggetto Sales nel server, utilizzare il formato seguente.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**Per eseguire una ricerca nell'intera foresta**

1.  Associare alla radice dello spazio dei nomi del catalogo globale.
2.  Enumerare il contenitore del catalogo globale. Il contenitore catalogo globale contiene un singolo oggetto che è possibile usare per eseguire ricerche nell'intera foresta.
3.  Usare l'oggetto nel contenitore per eseguire la ricerca. In C/C++ chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) sull'oggetto in modo da poter usare l'interfaccia **IDirectorySearch** per eseguire la ricerca. In Visual Basic usare l'oggetto restituito dall'enumerazione nella query ADO.

Per enumerare i server di catalogo globale in un sito, eseguire una ricerca di sottoalbero LDAP di "CN = <yoursite> , CN = Sites <DN of the configurationNamingContext> ", usando la stringa di filtro seguente.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Questo filtro usa il **bit della regola di corrispondenza LDAP \_ \_ \_ \_ e** l'operatore di regola di corrispondenza (1.2.840.113556.1.4.803) per trovare gli oggetti **NTDSDSA** con il bit di ordine inferiore impostato nella maschera di bit dell'attributo **options** . Il bit di ordine inferiore, che corrisponde a **NTDSDSA \_ opt \_ è \_** la costante GC definita in ntdsapi. h, identifica l'oggetto **NTDSDSA** di un server di catalogo globale. Per altre informazioni sulle regole di corrispondenza, vedere [sintassi del filtro di ricerca](/windows/desktop/ADSI/search-filter-syntax).

L'elemento padre dell'oggetto **NTDSDSA** è l'oggetto server e la proprietà **dNSHostName** dell'oggetto server è il nome DNS del server di catalogo globale.

Non è possibile usare \# le costanti define, ad esempio **NTDSDSA \_ opz \_ è \_** un bit della regola di corrispondenza GC e **LDAP \_ \_ \_ \_ e** direttamente in una stringa di filtro di ricerca. Tuttavia, è possibile usare queste costanti come argomenti per una funzione, ad esempio [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) , per inserire i valori costanti in una stringa di filtro.

Il catalogo globale non rappresenta l'intera struttura ad albero della foresta. Si supponga, ad esempio, che l'esempio di codice seguente enumera tutti i domini della foresta e tutti gli oggetti figlio di ogni dominio. In realtà, ciò che realmente fa è enumerare tutti i domini della foresta, ma nessuno degli oggetti di dominio enumerati contiene elementi figlio. Si tratta di una limitazione del catalogo globale.


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



Per risolvere il problema, è necessario eseguire l'associazione a ogni oggetto di dominio e quindi enumerare gli oggetti figlio di ogni dominio. La tecnica corretta è illustrata nell'esempio di codice seguente.


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



Per ulteriori informazioni ed esempi di codice che illustrano come eseguire la ricerca in un'intera foresta, vedere [il codice di esempio per la ricerca in una foresta](example-code-for-searching-a-forest.md).

 

 