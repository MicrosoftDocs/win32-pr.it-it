---
title: Associazione a un oggetto di Active Directory
description: Il modo più comune per eseguire l'associazione a un oggetto Active Directory è usare la funzione GetObject tra un client ADSI e un provider ADSI.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Associazione a un oggetto Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc788ed9eb124e1da6c21848f02393d46608f00dd3a9e779788fa54429922400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429135"
---
# <a name="binding-to-an-active-directory-object"></a>Associazione a un oggetto di Active Directory

Il modo più comune per eseguire l'associazione a un oggetto Active Directory è usare la **funzione GetObject** tra un client ADSI e un provider ADSI. Questo è anche il modo più semplice per mostrare come riceve il componente provider e le richieste di servizi. Sia la funzione API ADSI [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) che la funzione **getObject** Visual Basic seguire la stessa procedura per l'associazione.

Per questo esempio, si supponga che il client ADSI sia un'applicazione del visualizzatore ADSI che ha ricevuto il "Sample://Seattle/Redmond/Shelly" ADsPath dalla relativa interfaccia utente (1). La figura seguente illustra in dettaglio la sequenza di eventi numerando le frecce del flusso.

![visualizzazione dettagliata dei componenti adsi](images/dscsex.png)

Nella figura precedente, il client avvia la richiesta di un puntatore a interfaccia sull'oggetto Active Directory rappresentato da ADsPath "Sample://Seattle/Redmond/Shelly" dai servizi ADSI (2). Durante l'inizializzazione, il software dei servizi ha popolato una tabella di identificatori programmatici del provider installati (ProgID) dal Registro di sistema ("LDAP:","Sample:", "WinNT:" e così via) e li ha associati ai **CLSID** corrispondenti che identificano il modulo software appropriato.

Il server ADSI verifica che progID, in questo caso "Sample:", esista in ADsPath. Crea quindi un contesto di associazione per ottimizzare altri riferimenti a questo oggetto e chiama la funzione COM standard [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) per creare un moniker COM che può essere usato per trovare ed eseguire l'associazione all'oggetto che rappresenta l'utente "Shelly".

Nella sezione seguente i nomi file del codice sorgente del componente del provider di esempio sono inclusi tra parentesi, se appropriato.

Come in altre implementazioni del server COM, [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) esamina ProgID e cerca il **CLSID** appropriato nel Registro di sistema (3) per trovare il codice class factory fornito dal provider corrispondente (Cprovcf.cpp) nell'implementazione del provider appropriata (4). Questo codice crea un oggetto di primo livello iniziale che implementa il metodo [**IParseDisplayName::P arseDisplayName**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) (Cprov.cpp). L'implementazione del provider **di ParseDisplayName** risolve il percorso nello spazio dei nomi del provider. Chiama infine ADsObject e richiama il parser fornito con il componente provider (Parse.cpp) per verificare che ADsPath sia sintatticamente corretto per questo spazio dei nomi.

**GetObject**, definito in Getobj.cpp, determina quindi se l'oggetto richiesto è un oggetto spazio dei nomi, un oggetto schema o un altro tipo di oggetto. Se uno dei primi due, viene creato il tipo di oggetto classe dello schema e viene recuperato il puntatore a interfaccia appropriato. In caso contrario, il percorso della directory di esempio viene creato da ADsPath (ad esempio, "Seattle Redmond Shelly", ma in un servizio directory diverso potrebbe essere " \\ \\ \\ \\ \\ OU=Seattle OU=Redmond CN=Shelly") e il controllo passa a SampleDSOpenObject che apre l'oggetto nell'archivio dati di esempio e recupera anche il tipo di oggetto (in questo \\ caso, "User") (5).

Con i dati raccolti, viene creato un nuovo oggetto (6) per rappresentare l'elemento descritto da ADsPath e viene recuperato un puntatore [**all'interfaccia IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) su tale oggetto. In questo caso, viene creato un oggetto Active Directory generico che supporta i **metodi IUnknown** e [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) (Cgenobj.cpp, Core.cpp). La routine CSampleDSGenObject::AllocateGenObject legge i dati della libreria dei tipi per creare le voci di invio appropriate per questi nuovi oggetti per supportare [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

Il wrapping di questo puntatore a interfaccia in un moniker completa la funzione ResolvePathName (Cprov.cpp) e analizza il nome visualizzato.

Tutti gli oggetti COM creati durante questo processo vengono memorizzati nella cache per motivi di prestazioni e gestiti tramite il contesto di associazione. In questo modo si migliorano le prestazioni per altre operazioni sullo stesso oggetto che seguono immediatamente l'associazione del moniker.

Questo oggetto Active Directory ben formato viene ora sottoposto a query per l'identificatore di interfaccia richiesto per la chiamata [**iniziale ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) e un puntatore a tale interfaccia viene recuperato (7) e passato di nuovo tramite il server ADSI al client (8&9). Da quel momento in poi, il client funziona direttamente con il componente provider tramite i metodi dell'interfaccia fino a quando la richiesta iniziale non viene soddisfatta (10).

Inoltre, le richieste di dati oggetto dal client in genere prendono la forma di richieste per le operazioni di gets e puts delle proprietà, tutte ottimizzate tramite l'implementazione del provider di una cache delle proprietà (Cprops.cpp). L'impacchettamento e la decompressione intelligente dei dati, spesso inclusa la copia e la libera di strutture e stringhe, tra i tipi di dati nativi nel sistema operativo del componente provider di esempio e il tipo [**AUTOMATION VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) supportato da ADSI avviene prima che le proprietà siano caricate nella cache (Smpoper.cpp).

Il componente provider di esempio è progettato in modo che le chiamate effettive al sistema operativo siano logicamente isolate dal componente provider, creando software portabile in più sistemi operativi (RegDSAPI.cpp).

 

 