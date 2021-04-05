---
title: Ricerca con OLE DB
description: Per entrambi i client di automazione che utilizzano ActiveX Data Objects (ADO) e tutti i client non di automazione, ADSI fornisce un provider OLE DB che supporta un subset di OLE DB interfacce di query.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Ricerca con OLE DB ADSI
- query ADSI, ricerca con OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b6b0c056a63174233271b9b059ebffa9d4d841
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730322"
---
# <a name="searching-with-ole-db"></a>Ricerca con OLE DB

Per entrambi i client di automazione che utilizzano ActiveX Data Objects (ADO) e tutti i client non di automazione, ADSI fornisce un provider OLE DB che supporta un subset di OLE DB interfacce di query. Il codice client che usa già OLE DB interfacce per le query può usare le stesse interfacce per eseguire query nei servizi directory.

Nell'implementazione OLE DB un servizio directory viene esposto come oggetto origine dati. Gli oggetti origine dati sono Factory per gli oggetti sessione e supportano [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) per la connessione alla directory, [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) per creare l'oggetto sessione, [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) per fornire i dati di autenticazione allo spazio dei nomi sottostante e fornire il comando di query e [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) per salvare i dati necessari per creare l'oggetto origine dati nel servizio directory sottostante.

**Per eseguire una query Active Directory utilizzando OLE DB**

1.  Recuperare l'interfaccia [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) dal provider OLE DB. Nel caso di Active Directory, usare l'identificatore di classe **CLSID \_ ADSDSOObject**.
2.  Compila una matrice [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) di dati di connessione specificando il nome utente e la password.
3.  Eseguire una query sull'interfaccia [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) recuperata nel passaggio 1 per l'interfaccia [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) .
4.  Chiamare il metodo [IDBProperties:: seproperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) passando la matrice [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) creata nel passaggio 2.
5.  Chiamare il metodo [IDBInitialize:: Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) per stabilire la connessione al provider OLE DB; si tratta del provider Active Directory, in questo caso.
6.  Eseguire una query sull'interfaccia [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) per l'interfaccia [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) .
7.  Chiamare il metodo [IDBCreateSession:: CreateSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) richiedendo una nuova interfaccia di tipo [IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85)).
8.  Chiamare il metodo [IDBCreateCommand:: CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) per creare un'interfaccia [ICommandText](/previous-versions/windows/desktop/ms714914(v=vs.85)) .
9.  Chiamare il metodo [ICommandText::](/previous-versions/windows/desktop/ms709757(v=vs.85)) SetValue. Passare il dialetto preferito e il testo effettivo del comando di query nel dialetto. Come dialetto è possibile utilizzare **DBGUID \_ LDAPDialect** o **DBGUID \_ dbsql** .
10. Chiamare [ICommand:: Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); viene restituita un'interfaccia [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) che rappresenta l'interfaccia del set di risultati.
11. Eseguire una query sull'interfaccia [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) per l'interfaccia [IColumnsInfo](/previous-versions/windows/desktop/ms725401(v=vs.85)) .
12. Chiamare il metodo [IColumnsInfo:: GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) per recuperare i dati della colonna relativi al set di risultati.
13. Popolare una matrice di strutture [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) , che descrive al provider OLE DB come esporre i tipi di dati per ogni colonna al codice dell'applicazione. Questo passaggio consente di specificare il tipo contenuto in una determinata colonna. Inoltre, gli offset delle colonne, relativi alla riga restituita, vengono impostati qui per colonna per colonna.
14. Eseguire una query sull'interfaccia [IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) per l'interfaccia [IAccessor](/previous-versions/windows/desktop/ms719672(v=vs.85)) .
15. Chiamare il metodo [IAccessor:: CreateAccessor](/previous-versions/windows/desktop/ms720969(v=vs.85)) , che restituisce una matrice di handle della funzione di accesso. Questa matrice viene quindi utilizzata per accedere alle righe del set di risultati.
16. Chiamare [IRowset:: GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) passando gli handle di riga e il numero di righe da ottenere.
17. Chiamare [IRowset:: GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) passando un handle di riga, dal set restituito nel passaggio 16. Viene restituito un puntatore non elaborato alla riga.

Per ulteriori informazioni sulla sintassi del filtro di ricerca, vedere la [sintassi del filtro di ricerca](search-filter-syntax.md).

Per leggere i dati di riga non elaborati restituiti, utilizzare la struttura [DBBINDING](/previous-versions/windows/desktop/ms716845(v=vs.85)) creata nel passaggio 13, calcolare gli offset di colonna nel puntatore ai dati non elaborati restituito nel passaggio 17. Leggere la parte relativa allo stato della colonna per ottenere un risultato di recupero in tale colonna.

Per ulteriori informazioni e un esempio di codice in cui viene illustrato come eseguire la ricerca Active Directory utilizzando il provider ADSI OLE DB, vedere il [codice di esempio per l'utilizzo di OLE DB per la ricerca Active Directory](example-code-for-using-ole-db-to-search-active-directory.md).

 

 