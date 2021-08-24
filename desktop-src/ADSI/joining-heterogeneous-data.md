---
title: Unione di dati eterogenei
description: Le organizzazioni tipiche archiviano i dati in più database eterogenei. I dati delle risorse umane possono essere archiviati in SQL Server, mentre i dati di gestione degli account vengono archiviati nella directory . Altri dati possono essere archiviati in formati proprietari.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409ac4e82d735f5099bb8846a59683075007c3fbdf56600bc5ae01e6863ffa2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657001"
---
# <a name="joining-heterogeneous-data"></a>Unione di dati eterogenei

Le organizzazioni tipiche archiviano i dati in più database eterogenei. I dati delle risorse umane possono essere archiviati in SQL Server, mentre i dati di gestione degli account vengono archiviati nella directory . Altri dati possono essere archiviati in formati proprietari.

Con, SQL Server 7.0, ADSI e il provider OLE DB, è possibile unire i dati da Active Directory ai dati in SQL Server e creare una vista dei dati uniti in join.

**Per aggiungere dati di Active Directory a SQL Server dati**

1.  Eseguire SQL **Query Analyzer** (Avviare programmi \| Microsoft SQL Server \| 7.0)
2.  Accedere al computer SQL Server.
3.  Eseguire la riga seguente (evidenziarla e premere CTRL+E):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    In questa riga gli argomenti per la stored procedure di sistema [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) sono i seguenti:

    -   "ADSI" è **l'argomento del server,** che sarà il nome del server collegato.
    -   "Active Directory Services" è l'argomento **srvproduct,** ovvero il nome dell'origine dati OLE DB che si sta aggiungendo come server collegato.
    -   "ADSDSOObject" è l'argomento del nome del **provider \_** e indica che si sta usando OLE DB provider.
    -   "adsdatasource" è l'argomento **\_ dell'origine** dati , ovvero il nome dell'origine dati interpretato dal provider OLE DB dati.

    È ora possibile usare il server collegato per accedere ad Active Directory da SQL Server.

4.  Nell'esempio seguente viene eseguita una query usando [l'istruzione OPENQUERY.](https://msdn.microsoft.com/library/Aa276848.aspx) Questa istruzione ha due argomenti: ADSI, ovvero il nome del server collegato appena creato, e un'istruzione di query. L'istruzione di query contiene gli elementi seguenti:

    -   [L'istruzione SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco di dati che verranno ottenuti dal servizio directory. È necessario usare il nome visualizzato LDAP per indicare i dati che si stanno cercando.
    -   [L'istruzione FROM](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni.
    -   [L'istruzione WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca. In questo esempio viene eseguita la ricerca di utenti.

    Digitare ed eseguire:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    È anche possibile usare il [dialetto ADSI LDAP](ldap-dialect.md). Esempio:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    Nell'esempio precedente la query LDAP è in quattro parti:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " è il nome distinto del server di directory in cui eseguire la ricerca.
    -   "(&(objectCategory=Person)(objectClass=user))" è il filtro di ricerca LDAP (vedere [Sintassi del filtro di ricerca).](search-filter-syntax.md)
    -   "name, adspath" sono i nomi (usando il formato del nome visualizzato LDAP) degli attributi da recuperare.
    -   "sottoalbero" indica [l'ambito](scope-of-query.md) della ricerca.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione ed esecuzione di una vista](creating-and-executing-a-view.md)
</dt> </dl>

 

 




