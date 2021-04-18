---
title: Accesso e manipolazione di dati con ADSI
description: Tutti gli oggetti dispongono di proprietà.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, accesso e manipolazione di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3291db7490c79aae6363f619582ed24339fb83d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300427"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Accesso e manipolazione di dati con ADSI

Tutti gli oggetti dispongono di proprietà. Tutti gli oggetti COM ADSI (Active Directory Service Interface) dispongono di una o più interfacce con metodi che recuperano le proprietà dell'oggetto directory rappresentato dall'oggetto COM. È possibile leggere le proprietà di un oggetto in diversi modi:

-   Ottenere una proprietà specifica in base al nome: l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) ha due metodi [**IADs:: Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs:: GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) per leggere una proprietà specifica. Ogni oggetto ADSI COM dispone di un'interfaccia **IADs** .
-   Ottenere un elenco di proprietà specificato: l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) ha il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) che consente di specificare un elenco contenente i nomi delle proprietà da leggere e restituisce una matrice di strutture contenenti i valori di proprietà richiesti.
-   Enumerare tutte le proprietà dell'oggetto: l'interfaccia [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) consente di enumerare tutte le proprietà di un oggetto.
-   Ottenere proprietà speciali: le interfacce di automazione ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) hanno metodi di proprietà che consentono di ottenere proprietà speciali che non sono archiviate in un oggetto. In alternativa, è possibile che i metodi di proprietà consentano di ottenere una proprietà dell'oggetto in un formato dati diverso dal tipo di dati effettivo archiviato. Ad esempio, l'interfaccia **IADs** dispone di metodi di proprietà come [**IADs:: Get \_ Name**](iads-property-methods.md), che recupera il nome distinto relativo di un oggetto (RDN); **IADs:: Get \_ Classe**, che recupera la classe di un oggetto, e **IADs:: Get \_ Parent**, che recupera il ADsPath al padre dell'oggetto.

ADSI consente di memorizzare nella cache le proprietà in locale dopo che sono state lette dal server di directory. In questo modo è possibile scegliere di leggere le proprietà dalla cache delle proprietà locale o di recuperare le proprietà direttamente dal server di directory. ADSI dispone inoltre di metodi per aggiornare la cache, oltre a specificare se tutte le proprietà di un oggetto sono memorizzate nella cache o solo quelle specificate.

Dopo aver recuperato una proprietà, è possibile leggerne il valore. Il tipo di dati di una proprietà dipende dalla definizione della proprietà, nota anche come attributo, nello schema di Active Directory. Per ogni tipo di proprietà che può esistere in Active Directory, nello schema di Active Directory è presente un oggetto **attributeSchema** . Un oggetto **attributeSchema** definisce le caratteristiche dell'attributo. Una di queste caratteristiche è la sintassi dell'attributo, che determina il tipo di dati dei valori dell'attributo. Per ulteriori informazioni, vedere [caratteristiche degli attributi e delle](/windows/desktop/AD/characteristics-of-attributes) [sintassi per gli attributi Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

Le interfacce di automazione ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) restituiscono un valore di proprietà come [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) o un puntatore a un'interfaccia di automazione su un oggetto com che rappresenta la proprietà. Le interfacce [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) restituiscono una proprietà come puntatore a una struttura contenente un valore della proprietà tipizzata o un puntatore a una stringa di byte. Inoltre, **IDirectoryObject** e **IDirectorySearch** recuperano le proprietà direttamente dal server di directory anziché usare una cache delle proprietà locale.

In questa sezione vengono descritti gli argomenti seguenti:

-   [Interfacce IADs e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md)
-   [Accesso agli attributi con ADSI](accessing-attributes-with-adsi.md)
-   [Modifica degli attributi con ADSI](modifying-attributes-with-adsi.md)
-   [Accesso alla cache delle proprietà direttamente con le interfacce IADsProperty](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Sintassi degli attributi ADSI](adsi-attribute-syntax.md)

 

 