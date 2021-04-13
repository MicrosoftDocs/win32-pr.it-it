---
title: Uso delle interfacce IADs
description: ADSI, ogni elemento di un servizio directory è rappresentato da un oggetto ADSI, ovvero un oggetto Component Object Model (COM) che supporta l'interfaccia standard di IUnknown COM, nonché le interfacce IDispatch e IADs.
ms.assetid: bdbf2012-6863-4611-8173-6a3cd9c4960f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, utilizzo
- ADSI ADSI, utilizzo di, utilizzo delle interfacce IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878afa9350a45f18238bebb69df1a96eba52715e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399729"
---
# <a name="using-the-iads-interfaces"></a>Uso delle interfacce IADs

ADSI, ogni elemento di un servizio directory è rappresentato da un oggetto ADSI, ovvero un oggetto Component Object Model (COM) che supporta l'interfaccia standard di [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) com, nonché le interfacce [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . **IADs** fornisce le funzioni di manutenzione di base per gli oggetti ADSI.

Ogni oggetto ADSI deve supportare questa interfaccia, che serve per:

-   Specificare l'identificazione dell'oggetto in base al nome, alla classe o ADsPath.
-   Identificare il contenitore di oggetti che gestisce la creazione e l'eliminazione di oggetti.
-   Ottenere la definizione dello schema dell'oggetto.
-   Caricare gli attributi dell'oggetto nella cache delle proprietà ed eseguire il commit delle modifiche nell'archivio directory permanente.
-   Accedere e modificare i valori degli attributi dell'oggetto nella cache delle proprietà.

L'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) è progettata per garantire che gli oggetti ADSI forniscano agli amministratori di rete e ai provider di servizi di directory una rappresentazione efficiente e coerente dei vari servizi directory sottostanti.

![oggetto ADSI che supporta l'interfaccia IADs](images/ds2iads.png)

La figura precedente mostra un oggetto ADSI generico che supporta le interfacce di base [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Un oggetto ADSI, ad esempio, gestisce i dati dall'archivio dati del servizio directory sottostante tramite le interfacce supportate. Questi dati sono noti come proprietà dell'oggetto e le routine che ottengono e impostano queste proprietà sono note come metodi di proprietà. Le proprietà di sola lettura hanno un metodo di proprietà che ottiene il valore della proprietà. Le proprietà di lettura/scrittura hanno due metodi; Metodo che imposta il valore e uno che ottiene il valore. Le proprietà vengono implementate in ogni oggetto ADSI utilizzando una [cache delle proprietà](the-adsi-attribute-cache.md). [**IADs:: Get \_ ADsPath**](iads-property-methods.md) e **IADs::p UT \_ ADsPath** sono esempi di metodi di proprietà. I metodi di proprietà non sono evidenti per Visual Basic e altri client di automazione che consentono riferimenti diretti alla proprietà. Ad esempio, Visual Basic fa riferimento a **IADs:: ADsPath** direttamente usando la sintassi **Object. ADsPath** . Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

Inoltre, un oggetto ADSI interagisce con altri oggetti ADSI e direttamente in uno spazio dei nomi tramite metodi. I metodi vengono eseguiti immediatamente. Esempi di metodi includono [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) e [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).

Tutte le proprietà, i metodi di proprietà e i metodi sono accessibili tramite interfacce COM standard.

Un oggetto ADSI viene identificato in modo univoco dal relativo ADsPath. Ad esempio, un ADsPath per lo spazio dei nomi LDAP è "LDAP://MyServer/DC=Fabrikam,DC=COM". Per ulteriori informazioni su ADsPaths, vedere [binding ADSI](binding-to-an-adsi-object.md). Per i programmatori che conoscono i moniker COM, questo è concettualmente simile al nome visualizzato del moniker COM.

Qualsiasi oggetto ADSI che contiene altri oggetti ADSI, denominato oggetto contenitore ADSI, supporta anche l'interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , che fornisce metodi e proprietà che gestiscono la creazione, l'eliminazione e l'enumerazione di oggetti ADSI contenuti nell'oggetto. Nella figura seguente viene illustrato un oggetto contenitore ADSI.

![oggetto contenitore ADSI](images/dsiadsc.png)

La maggior parte degli oggetti ADSI è contenuta in altri oggetti. L'unico oggetto ADSI senza contenitore padre è l'oggetto **spazi dei nomi** ADSI di primo livello ("ads:").

Il metodo [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) su un oggetto contenitore archivia in modo permanente le proprietà memorizzate nella cache dell'oggetto contenitore ADSI nell'archivio, oltre agli oggetti creati con il metodo [**IADsContainer:: create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) . [**IADsContainer::D Elimina**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) non influisce sulla cache delle proprietà, ma elimina l'elemento directory dello spazio dei nomi sottostante rappresentato da questo oggetto.

 

 