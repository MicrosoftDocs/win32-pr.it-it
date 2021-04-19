---
title: Unione di dati eterogenei
description: Le organizzazioni tipiche archiviano i dati in più database eterogenei. I dati delle risorse umane possono essere archiviati in SQL Server, mentre i dati di gestione degli account vengono archiviati nella directory. Altri dati possono essere archiviati in formati proprietari.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314614"
---
# <a name="joining-heterogeneous-data"></a>Unione di dati eterogenei

Le organizzazioni tipiche archiviano i dati in più database eterogenei. I dati delle risorse umane possono essere archiviati in SQL Server, mentre i dati di gestione degli account vengono archiviati nella directory. Altri dati possono essere archiviati in formati proprietari.

Con, SQL Server 7,0, ADSI e il provider di OLE DB, è possibile unire i dati da Active Directory ai dati in SQL Server e creare una vista dei dati aggiunti.

**Per aggiungere Active Directory dati con SQL Server dati**

1.  Eseguire **SQL Query Analyzer** (avvia \| programmi \| Microsoft SQL Server 7,0)
2.  Accedere al computer SQL Server.
3.  Eseguire la riga seguente (evidenziando e premendo CTRL + E):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    In questa riga, gli argomenti per la stored procedure di sistema [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) sono i seguenti:

    -   "ADSI" è l'argomento del **Server** , che sarà il nome del server collegato.
    -   "Active Directory Services" è l'argomento **srvproduct** , ovvero il nome dell'origine dati OLE DB che si sta aggiungendo come server collegato.
    -   "ADSDSOObject" è l'argomento del **\_ nome del provider** e indica che si sta usando il provider di OLE DB.
    -   "adsdatasource" è l' **\_ argomento dell'origine dati**, ovvero il nome dell'origine dati interpretato dal provider OLE DB.

    È ora possibile usare il server collegato per accedere a Active Directory da SQL Server.

4.  Nell'esempio successivo viene eseguita una query utilizzando l'istruzione [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) . Questa istruzione ha due argomenti: ADSI, ovvero il nome del server collegato appena creato e un'istruzione di query. L'istruzione di query contiene gli elementi seguenti:

    -   L'istruzione [Select](https://msdn.microsoft.com/library/Aa259187.aspx) contiene l'elenco dei dati che verranno ottenuti dal servizio directory. È necessario usare il nome visualizzato LDAP per indicare i dati che si stanno cercando.
    -   L'istruzione [from](https://msdn.microsoft.com/library/Aa258869.aspx) contiene il nome del server di directory collegato da cui verranno ottenute queste informazioni.
    -   L'istruzione [where](https://msdn.microsoft.com/library/Aa260674.aspx) fornisce le condizioni di ricerca. In questo esempio è in corso la ricerca di utenti.

    Digitare ed eseguire:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    È anche possibile usare il [dialetto ADSI LDAP](ldap-dialect.md). Ad esempio:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    Nell'esempio precedente la query LDAP è costituita da quattro parti:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " è il nome distinto del server di directory in cui eseguire la ricerca.
    -   "(& (objectCategory = person) (objectClass = user))" è il filtro di ricerca LDAP (vedere la [sintassi del filtro di ricerca](search-filter-syntax.md)).
    -   "Name, ADsPath" sono i nomi (usando il formato del nome visualizzato LDAP) degli attributi da recuperare.
    -   "sottoalbero" indica l' [ambito](scope-of-query.md) della ricerca.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione ed esecuzione di una visualizzazione](creating-and-executing-a-view.md)
</dt> </dl>

 

 




