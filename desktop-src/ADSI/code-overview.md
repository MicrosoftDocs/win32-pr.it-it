---
title: Panoramica del codice
description: La figura seguente è una rappresentazione concettuale dei blocchi di codice necessari per implementare il componente del provider di esempio ADSI.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Panoramica del codice AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99a4974ac97488fc051ea80dbde7a8a83fa329e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047364"
---
# <a name="code-overview"></a>Panoramica del codice

La figura seguente è una rappresentazione concettuale dei blocchi di codice necessari per implementare il componente del provider di esempio ADSI. Ogni sezione è descritta nella figura seguente. I programmatori COM esperti possono trovare questa è una panoramica appropriata del componente provider di esempio. Per ulteriori informazioni, vedere [Dettagli del codice](code-details.md).

![implementazione del provider di esempio](images/dssmco.png)

Gli elementi numerati seguenti corrispondono agli elementi Block nella figura.

1.  Caricamento della DLL (LibMain. cpp, Guid. cpp). Il punto di ingresso per la DLL. Definizioni di oggetti statici di class factory per i due oggetti provider: GUID. cpp contiene le definizioni CLSID per le implementazioni dei vari oggetti componente del provider di esempio.
2.  Oggetto provider class factory e codice di creazione (Cprovcf. cpp, Cprov. cpp, STDFact. cpp). L'oggetto provider è l'oggetto che supporta [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) durante le operazioni di associazione del moniker come descritto in ricerca e associazione nel componente provider di esempio.
3.  Associazione a un oggetto (Getobj. cpp). Questo codice chiama il parser per verificare che il ADsPath specificato sia sintatticamente corretto, quindi esegue tutti i mapping necessari da ADsPath al percorso del servizio directory nativo per l'elemento creato come oggetto Active Directory. Cerca la definizione dello schema per questo tipo di oggetto e compila le proprietà obbligatorie. Dopo la creazione dell'oggetto Active Directory, viene recuperato un puntatore di interfaccia a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per il chiamante.
4.  Parser per lo spazio dei nomi del provider (Parse. cpp). Si tratta del codice richiamato dall'elemento 3. Il parser verifica che la stringa ADsPath passata sia sintatticamente corretta per il proprio spazio dei nomi.
5.  Class factory, creazione ed enumerazione per l'oggetto spazio dei nomi (Cnamcf. cpp, Cnamesp. cpp, Cenumns. cpp). L'oggetto Namespace è un oggetto contenitore che può essere enumerato per trovare tutti gli oggetti nodo radice per questo spazio dei nomi.
6.  Class factory e codice di creazione per un oggetto generico Active Directory e class factory, codice di creazione ed enumerazione per un oggetto contenitore di annunci generici (Cgenobj. cpp, Cenumobj. cpp, Common. cpp, Core. cpp). Questo codice viene eseguito quando viene creato un oggetto Active Directory.
7.  Filtrare ed enumerare le varianti (Cenumvar. cpp, Object. cpp). Quando una raccolta di elementi VARIANT di un singolo tipo viene gestita all'interno di ADSI, viene utilizzato questo codice.
8.  Globals (Globals. cpp). Qui sono definite le parole chiave dello spazio dei nomi, le strutture di mapping della sintassi dai formati di dati nativi al tipo VARIANT di automazione degli annunci.
9.  Marshalling/unmarshalling dei dati (Pack. cpp, Property. cpp, Smpoper. cpp). La conversione da formati di dati nativi al set supportato di tipi VARIANT di automazione si verifica quando le proprietà di un oggetto vengono caricate nella cache delle proprietà. È necessario eseguire un'altra gestione speciale dei dati quando le strutture con puntatori vengono copiate, eliminate o spostate in memoria.
10. Cache delle proprietà (cProps. cpp). La memorizzazione nella cache delle proprietà è una funzionalità dell'ambiente ADSI. I metodi [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo), [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)e [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) agiscono sulla cache delle proprietà.
11. Gestione della memoria (Memory. cpp). L'utilizzo di un set di funzioni di memoria per allocare e liberare memoria consente al componente provider di esempio di tenere traccia dell'utilizzo della memoria e di arrestare le perdite di memoria.
12. Oggetti e gestione dello schema (Cschobj. cpp, Cprpobj. cpp, Cclsobj. cpp, Cenumsch. cpp). Sono incluse le routine per creare, gestire ed enumerare gli oggetti dello schema. Sono inclusi oggetti della classe di schema, oggetti proprietà e oggetti sintassi, oltre a poter enumerare l'oggetto contenitore della classe dello schema.
13. Chiamate specifiche del sistema operativo (RegDSAPI. cpp). Sono incluse tutte le chiamate che fanno riferimento al sistema operativo nativo. Tra le altre funzioni, includono funzioni che aprono, chiudono, leggono e modificano gli oggetti, nonché quelli che accedono ai dati dello schema e della proprietà. Il componente provider di esempio è stato usato per simulare una gerarchia di directory tramite il registro di sistema. Solo i nomi di funzione devono essere molto interessanti per un writer del provider.
14. Implementazione di [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr. cpp). Questo codice accede ai dati della libreria dei tipi per consentire che i metodi di interfaccia vengano richiamati in modo compatibile con l'automazione.

 

 