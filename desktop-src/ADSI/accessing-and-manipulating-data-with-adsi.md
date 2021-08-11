---
title: Accesso e manipolazione dei dati con ADSI
description: Tutti gli oggetti hanno proprietà.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, accesso e modifica dei dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ed09c1717f4f9a9c1c75372e7efdc23d2cce1adb39242197346061ae4df00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181631"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Accesso e manipolazione dei dati con ADSI

Tutti gli oggetti hanno proprietà. Tutti gli oggetti COM ADSI (Active Directory Service Interface) dispongono di una o più interfacce con metodi che recuperano le proprietà dell'oggetto directory rappresentato dall'oggetto COM. Esistono diversi modi per leggere le proprietà da un oggetto:

-   Ottenere una proprietà specifica in base al nome: l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) ha due metodi [**IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) per leggere una proprietà specifica. Ogni oggetto COM ADSI ha **un'interfaccia IADs.**
-   Ottenere un elenco specificato di proprietà: l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ha il metodo [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) che consente di specificare un elenco contenente i nomi delle proprietà da leggere e restituisce una matrice di strutture contenenti i valori di proprietà richiesti.
-   Enumerare tutte le proprietà nell'oggetto: [**l'interfaccia IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) consente di enumerare tutte le proprietà in un oggetto.
-   Ottenere proprietà speciali: le interfacce di automazione [**(IAD)**](/windows/desktop/api/Iads/nn-iads-iads)hanno metodi di proprietà che consentono di ottenere proprietà speciali non \* archiviate in un oggetto. Oppure i metodi delle proprietà possono consentire di ottenere una proprietà dell'oggetto in un formato di dati diverso dal tipo di dati effettivo archiviato. Ad esempio, **l'interfaccia IADs** include metodi di proprietà come [**IADs::get \_ Name,**](iads-property-methods.md)che recupera il nome distinto relativo (RDN) di un oggetto. **IADs::get \_ Classe**, che recupera la classe di un oggetto e **IADs::get \_ Parent,** che recupera ADsPath nell'elemento padre dell'oggetto.

ADSI consente di memorizzare nella cache le proprietà in locale dopo che sono state lette dal server di directory. In questo modo è possibile scegliere di leggere le proprietà dalla cache delle proprietà locale o di recuperare le proprietà direttamente dal server di directory. ADSI include anche metodi per aggiornare la cache, nonché per specificare se tutte le proprietà di un oggetto vengono memorizzate nella cache o solo quelle specificate.

Dopo aver recuperato una proprietà, leggerne il valore. Il tipo di dati di una proprietà dipende dalla definizione della proprietà (nota anche come attributo) nello schema di Active Directory. Per ogni tipo di proprietà che può esistere in Active Directory, è presente un **oggetto attributeSchema** nello schema di Active Directory. Un **oggetto attributeSchema** definisce le caratteristiche dell'attributo. Una di queste caratteristiche è la sintassi dell'attributo, che determina il tipo di dati dei valori dell'attributo. Per altre informazioni, vedere [Caratteristiche degli attributi e](/windows/desktop/AD/characteristics-of-attributes) [sintassi per gli attributi di Active Directory.](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)

Le interfacce di automazione [**(IAD)**](/windows/desktop/api/Iads/nn-iads-iads)restituiscono un valore della proprietà come VARIANT o un puntatore a un'interfaccia di automazione in un oggetto \* COM che rappresenta la proprietà. [](/windows/win32/api/oaidl/ns-oaidl-variant) Le [**interfacce IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) restituiscono una proprietà come puntatore a una struttura contenente un valore di proprietà tipita o un puntatore a una stringa di byte. Inoltre, **IDirectoryObject** e **IDirectorySearch** recuperano le proprietà direttamente dal server di directory invece di usare una cache delle proprietà locale.

In questa sezione vengono descritti gli argomenti seguenti:

-   [Interfacce IAD e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md)
-   [Accesso agli attributi con ADSI](accessing-attributes-with-adsi.md)
-   [Modifica degli attributi con ADSI](modifying-attributes-with-adsi.md)
-   [Accesso diretto alla cache delle proprietà con le interfacce IADsProperty](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Sintassi degli attributi ADSI](adsi-attribute-syntax.md)

 

 