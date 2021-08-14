---
title: Panoramica del codice
description: La figura seguente è una rappresentazione concettuale dei blocchi di codice necessari per implementare il componente provider di esempio ADSI.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Panoramica del codice ad Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc23f4a3a51c33f24748347a2941bc09dbda8bc3bd99d133f99d0377eb0bda90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017727"
---
# <a name="code-overview"></a>Panoramica del codice

La figura seguente è una rappresentazione concettuale dei blocchi di codice necessari per implementare il componente provider di esempio ADSI. Ogni sezione è descritta nella figura seguente. I programmatori COM esperti potrebbero trovare questa soluzione come una panoramica appropriata del componente provider di esempio. Per altre informazioni, vedere [Dettagli codice.](code-details.md)

![implementazione del provider di esempio](images/dssmco.png)

Gli elementi numerati seguenti corrispondono agli elementi del blocco nella figura.

1.  Caricamento della DLL (Libmain.cpp, Guid.cpp). Punto di ingresso per la DLL. Definizioni di oggetti statici della class factory per i due oggetti provider: Guid.cpp contiene le definizioni CLSID per le implementazioni dei vari oggetti componente del provider Example.
2.  Oggetto provider class factory codice di creazione (Cprovcf.cpp, Cprov.cpp, Stdfact.cpp). L'oggetto provider è l'oggetto che supporta [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) durante le operazioni di associazione del moniker, come descritto in Ricerca e associazione nel componente provider di esempio.
3.  Associazione a un oggetto (Getobj.cpp). Questo codice chiama il parser per verificare che il valore ADsPath specificato sia sintatticamente corretto e quindi esegue il mapping necessario da ADsPath al percorso del servizio directory nativo per l'elemento creato come oggetto Active Directory. Cerca nella definizione dello schema questo tipo di oggetto e inserisce le proprietà obbligatorie. Dopo aver creato l'oggetto Active Directory, viene recuperato un puntatore di interfaccia [**a IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per il chiamante.
4.  Parser per lo spazio dei nomi del provider (Parse.cpp). Si tratta del codice richiamato dall'elemento 3. Il parser verifica che la stringa ADsPath passata sia sintatticamente corretta per il proprio spazio dei nomi.
5.  Class factory, creazione ed enumerazione per l'oggetto spazio dei nomi (Cnamcf.cpp, Cnamesp.cpp, Cenumns.cpp). L'oggetto spazio dei nomi è un oggetto contenitore che può essere enumerato per trovare tutti gli oggetti nodo radice per questo spazio dei nomi.
6.  Class factory e codice di creazione per un oggetto Active Directory generico e codice di class factory, creazione ed enumerazione per un oggetto contenitore ADs generico (Cgenobj.cpp, Cenumobj.cpp, Common.cpp, Core.cpp). Questo codice viene eseguito quando viene creato un oggetto Active Directory.
7.  Filtro ed enumerazione di VARIANTs (Cenumvar.cpp, Object.cpp). Quando una raccolta di elementi VARIANT di un singolo tipo viene gestita in all'interno di ADSI, viene usato questo codice.
8.  Globals (Globals.cpp). Le parole chiave dello spazio dei nomi, le strutture di mapping della sintassi dai formati di dati nativi al tipo VARIANT di Automazione ADs sono tutte definite qui.
9.  Marshalling/unmarshaling dei dati (Pack.cpp, Property.cpp, Smpoper.cpp). La conversione da formati di dati nativi al set supportato di tipi VARIANT di Automazione si verifica quando le proprietà di un oggetto vengono caricate nella cache delle proprietà. È necessario eseguire altre operazioni di gestione speciali per i dati quando le strutture con puntatori vengono copiate, eliminate o spostate in memoria.
10. Cache delle proprietà (Cprops.cpp). Caching proprietà è una funzionalità dell'ambiente ADSI. I [**metodi IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo), [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)e [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) agiscono sulla cache delle proprietà.
11. Gestione della memoria (Memory.cpp). L'uso di un set di funzioni di memoria per allocare e liberare memoria consente al componente provider di esempio di tenere traccia dell'uso della memoria e arrestare le perdite di memoria.
12. Gestione e oggetti dello schema (Cschobj.cpp, Cprpobj.cpp, Cclsobj.cpp, Cenumsch.cpp). Sono incluse routine per creare, gestire ed enumerare gli oggetti dello schema. Sono inclusi gli oggetti classe dello schema, gli oggetti proprietà e gli oggetti di sintassi, oltre a essere in grado di enumerare l'oggetto contenitore della classe dello schema.
13. Chiamate specifiche del sistema operativo (RegDSAPI.cpp). Sono incluse tutte le chiamate che fanno riferimento al sistema operativo nativo. Tra le altre funzioni, includono funzioni di apertura, chiusura, lettura e modifica di oggetti, nonché quelle che accedono ai dati dello schema e della proprietà. Il componente provider di esempio simula una gerarchia di directory usando il Registro di sistema. Solo i nomi di funzione devono essere di particolare interesse per un writer di provider.
14. [**Implementazione di IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr.cpp). Questo codice accede ai dati della libreria dei tipi per consentire ai metodi di interfaccia di essere richiamati in modo compatibile con Automazione.

 

 