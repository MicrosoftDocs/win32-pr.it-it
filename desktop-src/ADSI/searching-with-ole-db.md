---
title: Ricerca con OLE DB
description: Per entrambi i client di automazione che usano ActiveX Data Objects (ADO) e tutti i client non di automazione, ADSI fornisce un provider OLE DB che supporta un subset di OLE DB di query.
ms.assetid: f4e48b60-82dd-4c39-879b-0bc8f40747d2
ms.tgt_platform: multiple
keywords:
- Ricerca con OLE DB ADSI
- query ADSI, ricerca con OLE DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969dd544600bdb88b2c01b6b932f101f0b9508d7f3f54cd5e6728fd3e4dd5f6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828371"
---
# <a name="searching-with-ole-db"></a>Ricerca con OLE DB

Per entrambi i client di automazione che usano ActiveX Data Objects (ADO) e tutti i client non di automazione, ADSI fornisce un provider OLE DB che supporta un subset di OLE DB di query. Il codice client che usa già OLE DB per le query può usare le stesse interfacce per eseguire query sui servizi directory.

Nell'implementazione OLE DB, un servizio directory viene esposto come oggetto origine dati. Gli oggetti origine dati sono factory per gli oggetti sessione e supportano [IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) per la connessione alla directory, [IDBCreateSession](/previous-versions/windows/desktop/ms724076(v=vs.85)) per creare l'oggetto sessione, [IDBProperties](/previous-versions/windows/desktop/ms719607(v=vs.85)) per fornire i dati di autenticazione allo spazio dei nomi sottostante e fornire il comando di query e [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist) per salvare i dati necessari per creare l'oggetto origine dati nel servizio directory sottostante.

**Per eseguire una query di Active Directory usando OLE DB**

1.  Recuperare [l'interfaccia IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) dal provider OLE DB database. Nel caso di Active Directory, usare l'identificatore di classe **CLSID \_ ADsDSOObject**.
2.  Compilare [una matrice DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) di dati di connessione specificando nome utente e password.
3.  Eseguire una query [sull'interfaccia IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) recuperata nel passaggio 1 per [l'interfaccia IDBProperties.](/previous-versions/windows/desktop/ms719607(v=vs.85))
4.  Chiamare il [metodo IDBProperties::SetProperties](/previous-versions/windows/desktop/ms723049(v=vs.85)) passando la matrice [DBPROP](/previous-versions/windows/desktop/ms717970(v=vs.85)) creata nel passaggio 2.
5.  Chiamare il [metodo IDBInitialize::Initialize](/previous-versions/windows/desktop/ms718026(v=vs.85)) per stabilire la connessione al provider OLE DB; che è il provider di Active Directory, in questo caso.
6.  Eseguire una query [sull'interfaccia IDBInitialize](/previous-versions/windows/desktop/ms713706(v=vs.85)) per [l'interfaccia IDBCreateSession.](/previous-versions/windows/desktop/ms724076(v=vs.85))
7.  Chiamare il [metodo IDBCreateSession::CreateSession](/previous-versions/windows/desktop/ms714942(v=vs.85)) richiedendo una nuova interfaccia di [tipo IDBCreateCommand](/previous-versions/windows/desktop/ms711625(v=vs.85)).
8.  Chiamare il [metodo IDBCreateCommand::CreateCommand](/previous-versions/windows/desktop/ms709772(v=vs.85)) per creare [un'interfaccia ICommandText.](/previous-versions/windows/desktop/ms714914(v=vs.85))
9.  Chiamare il [metodo ICommandText::SetCommandText.](/previous-versions/windows/desktop/ms709757(v=vs.85)) Passare il dialetto preferito e il testo effettivo del comando di query in tale dialetto. È **possibile \_ usare DBGUID LDAPDialect** **o \_ DBGUID DBSQL** come dialetto.
10. Chiamare [ICommand::Execute](/previous-versions/windows/desktop/ms718095(v=vs.85)); Viene [restituita un'interfaccia IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) che rappresenta l'interfaccia del set di risultati.
11. Eseguire una [query sull'interfaccia IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) per [l'interfaccia IColumnsInfo.](/previous-versions/windows/desktop/ms725401(v=vs.85))
12. Chiamare il [metodo IColumnsInfo::GetColumnInfo](/previous-versions/windows/desktop/ms722704(v=vs.85)) per recuperare i dati della colonna relativi al set di risultati.
13. Popolare una matrice di strutture [DBBINDING,](/previous-versions/windows/desktop/ms716845(v=vs.85)) descrivendo al provider OLE DB come esporre i tipi di dati per colonna al codice dell'applicazione. Questo passaggio consente di specificare quale TIPO è contenuto in una determinata colonna. Anche gli offset delle colonne, rispetto alla riga restituita, vengono impostati in questo caso colonna per colonna.
14. Eseguire una [query sull'interfaccia IRowset](/previous-versions/windows/desktop/ms720986(v=vs.85)) per [l'interfaccia IAccessor.](/previous-versions/windows/desktop/ms719672(v=vs.85))
15. Chiamare il [metodo IAccessor::CreateAccessor,](/previous-versions/windows/desktop/ms720969(v=vs.85)) che restituisce una matrice di handle della funzione di accesso. Questa matrice viene quindi usata per accedere alle righe del set di risultati.
16. Chiamare [IRowset::GetNextRows](/previous-versions/windows/desktop/ms709827(v=vs.85)) passando gli handle di riga e il numero di righe da ottenere.
17. Chiamare [IRowset::GetData](/previous-versions/windows/desktop/ms716988(v=vs.85)) passando un handle di riga, dal set restituito nel passaggio 16. Viene restituito un puntatore non elaborato alla riga.

Per altre informazioni sulla sintassi del filtro di ricerca, vedere [Sintassi del filtro di ricerca.](search-filter-syntax.md)

Per leggere i dati di riga non elaborati restituiti, usare la struttura [DBBINDING,](/previous-versions/windows/desktop/ms716845(v=vs.85)) creata nel passaggio 13, calcolare gli offset di colonna nel puntatore ai dati non elaborato restituito nel passaggio 17. Leggere la parte relativa allo stato della colonna per un risultato del recupero in tale colonna.

Per altre informazioni e un esempio di codice che illustra come eseguire ricerche in Active Directory usando il provider OLE DB ADSI, vedere Codice di esempio per l'uso di [OLE DB per la ricerca in Active Directory.](example-code-for-using-ole-db-to-search-active-directory.md)

 

 