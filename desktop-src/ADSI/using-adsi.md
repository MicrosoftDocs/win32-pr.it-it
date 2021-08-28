---
title: Uso delle interfacce del servizio Active Directory
description: Active Directory Service Interfaces (ADSI) consente alle applicazioni client dei servizi directory di usare un set di interfacce per comunicare con qualsiasi spazio dei nomi che fornisce un'implementazione ADSI.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Uso di ACTIVE Directory Service Interfaces ADSI
- ADSI ADSI , uso
- Interfacce del servizio Active Directory ADSI , uso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15495f9fa21f436570381ea8f0b2a7c7fff5f4efed645a5f3465a3b5d2929776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648851"
---
# <a name="using-active-directory-service-interfaces"></a>Uso delle interfacce del servizio Active Directory

Active Directory Service Interfaces (ADSI) consente alle applicazioni client dei servizi directory di usare un set di interfacce per comunicare con qualsiasi spazio dei nomi che fornisce un'implementazione ADSI. I client ADSI usano le interfacce del servizio Active Directory ben definite al posto delle chiamate API specifiche della rete per ottenere un accesso più semplice ai servizi per uno spazio dei nomi.

Le interfacce del servizio Active Directory sono conformi Component Object Model (COM) e supportano le funzionalità COM standard.

ADSI fornisce interfacce conformi ad Automazione per controller associati a nomi come Java, microsoft Visual Basic development system e Visual Basic Scripting Edition (VBScript). ADSI può anche fornire un'interfaccia in grado di ottimizzare le prestazioni per le interfacce non conformi ad Automazione, da usare con ambienti di linguaggio come C e C++.

ADSI fornisce anche le interfacce non di [**automazione, IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)per supportare la gestione degli oggetti directory e le query.

ADSI fornisce anche il proprio provider OLE DB, in modo che qualsiasi client che già usa OLE DB, inclusi quelli che usano ActiveX Data Objects, possa eseguire query direttamente sui servizi directory.

Le applicazioni Web che Active Server pages possono anche programmare l'accesso ai servizi directory tramite ADSI.

I client ADSI possono individuare a livello di codice tutti i provider ADSI in un sito e usare le stesse interfacce per comunicare con ogni spazio dei nomi. Con l'installazione di provider aggiuntivi, i client ADSI possono comunicare, senza ricompilare, anche con i nuovi spazi dei nomi.

Questa guida per programmatori descrive il funzionamento di ADSI e fornisce informazioni per l'esecuzione di attività specifiche in ADSI. Vengono trattati i seguenti argomenti:

-   [Associazione a un oggetto ADSI](binding-to-an-adsi-object.md)
-   [Creazione ed eliminazione di oggetti](creating-and-deleting-objects.md)
-   [Accesso e modifica dei dati con ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Uso dello schema ADSI](using-the-adsi-schema.md)
-   [Raccolte e gruppi](collections-and-groups.md)
-   [Enumerazione di oggetti ADSI](enumerating-adsi-objects.md)
-   [Ricerca in Active Directory](searching-active-directory.md)
-   [Modello di sicurezza ADSI](adsi-security-model.md)
-   [Estensioni ADSI](adsi-extensions.md)
-   [Uso di ADSI con Exchange](using-adsi-with-exchange.md)
-   [Interfacce dell'utilità ADSI](adsi-utility-interfaces.md)
-   [Programmazione di ADSI con Java/COM](programming-adsi-with-javacom.md)

 

 




