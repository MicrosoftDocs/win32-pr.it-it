---
title: Associazione a un oggetto Active Directory
description: Il modo più comune per eseguire l'associazione a un oggetto Active Directory consiste nell'usare la funzione GetObject tra un client ADSI e un provider ADSI.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Associazione a un oggetto Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59992dbc88c00be6306dec24523ec4e030d4a516
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872946"
---
# <a name="binding-to-an-active-directory-object"></a>Associazione a un oggetto Active Directory

Il modo più comune per eseguire l'associazione a un oggetto Active Directory consiste nell'usare la funzione **GetObject** tra un client ADSI e un provider ADSI. Questo è anche il modo più semplice per illustrare il modo in cui il componente del provider riceve le richieste e i servizi. Sia la funzione API ADSI [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) che la funzione Visual Basic **GetObject** seguono gli stessi passaggi per l'associazione.

Per questo esempio, si supponga che il client ADSI sia un'applicazione Visualizzatore ADSI che ha ricevuto il ADsPath "Sample://Seattle/Redmond/Shelly" dalla relativa interfaccia utente (1). Nella figura seguente viene illustrata la sequenza di eventi numerando le frecce del flusso.

![visualizzazione dettagliata dei componenti ADSI](images/dscsex.png)

Nella figura precedente, il client avvia la richiesta di un puntatore a interfaccia nell'oggetto Active Directory rappresentato da ADsPath "Sample://Seattle/Redmond/Shelly" da servizi ADSI (2). Durante l'inizializzazione, il software dei servizi ha popolato una tabella di identificatori a livello di codice (ProgID) installati dal registro di sistema ("LDAP:", "Sample:", "WinNT:" e così via) e abbinati ai **CLSID** corrispondenti che identificano il modulo software appropriato.

Il server ADSI verifica che il ProgID, in questo caso "Sample:", esista nella ADsPath. Viene quindi creato un contesto di associazione per ottimizzare altri riferimenti a questo oggetto e viene chiamata la funzione COM standard [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) per creare un moniker COM che può essere usato per trovare e associare l'oggetto che rappresenta l'utente "Shelly".

Nella sezione seguente, i nomi file del codice sorgente del componente provider di esempio sono inclusi tra parentesi laddove appropriato.

Come in altre implementazioni di server COM, [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) esamina il ProgID e cerca il **CLSID** appropriato nel registro di sistema (3) per trovare il codice di class factory corrispondente fornito dal provider (Cprovcf. cpp) nell'implementazione del provider appropriata (4). Questo codice crea un oggetto iniziale di primo livello che implementa il metodo [**IParseDisplayName::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) (Cprov. cpp). L'implementazione del provider di **ParseDisplayName** risolve il percorso nello spazio dei nomi del provider. Viene infine chiamato ADsObject e viene richiamato il parser fornito con il componente provider (Parse. cpp) per verificare che ADsPath sia sintatticamente corretto per questo spazio dei nomi.

**GetObject**, definito in Getobj. cpp, determina se l'oggetto richiesto è un oggetto spazio dei nomi, un oggetto schema o un altro tipo di oggetto. Se uno dei primi due, viene creato tale tipo di oggetto della classe di schema e viene recuperato il puntatore di interfaccia appropriato. In caso contrario, il percorso della directory di esempio viene creato da ADsPath (ad esempio, " \\ Seattle \\ Redmond \\ Shelly", ma in un altro servizio directory potrebbe essere stato " \\ ou = Seattle \\ ou = Redmond \\ CN = Shelly") e il controllo passa a SampleDSOpenObject che apre l'oggetto nell'archivio dati di esempio e recupera anche il tipo di oggetto (in questo caso "User") (5).

Con i dati raccolti, viene creato un nuovo oggetto (6) per rappresentare l'elemento descritto da ADsPath e viene recuperato un puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) su tale oggetto. In questo caso, viene creato un oggetto Active Directory generico che supporta i metodi **IUnknown** e [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) (Cgenobj. cpp, Core. cpp). La routine CSampleDSGenObject:: AllocateGenObject legge i dati della libreria dei tipi per creare le voci di distribuzione appropriate per questi nuovi oggetti allo scopo di supportare [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

Il wrapping di questo puntatore di interfaccia in un moniker completa la funzione ResolvePathName (Cprov. cpp) e analizza il nome visualizzato.

Tutti gli oggetti COM creati durante questo processo vengono memorizzati nella cache per motivi di prestazioni e gestiti tramite il contesto di associazione. Ciò migliora le prestazioni per altre operazioni nello stesso oggetto che segue immediatamente l'associazione del moniker.

Questo oggetto Active Directory ben formato viene ora sottoposto a query per l'identificatore di interfaccia richiesto per la chiamata [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) iniziale e un puntatore a tale interfaccia viene recuperato (7) e passato attraverso il server ADSI al client (8&9). Da quel momento in poi, il client interagisce direttamente con il componente provider tramite i metodi di interfaccia finché la richiesta iniziale non viene soddisfatta (10).

Inoltre, le richieste di dati dell'oggetto dal client in genere hanno il formato di richieste per le proprietà Gets e Put, tutte ottimizzate tramite l'implementazione del provider di una cache delle proprietà (cProps. cpp). La compressione e la decompressione intelligenti dei dati, spesso incluse la copia e la liberazione di strutture e stringhe, tra i tipi di dati nativi sul sistema operativo del componente provider di esempio e il tipo di [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) di automazione supportato da ADSI avvengono prima che le proprietà vengano caricate nella cache (Smpoper. cpp).

Il componente provider di esempio è progettato in modo che le chiamate effettive al sistema operativo siano isolate logicamente dal componente provider, creando software portabile in più di un sistema operativo (RegDSAPI. cpp).

 

 