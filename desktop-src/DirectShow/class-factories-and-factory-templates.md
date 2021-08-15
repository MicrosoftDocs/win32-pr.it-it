---
description: Questo argomento descrive come implementare una DLL per un filtro DirectShow, usando le classi DirectShow base.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Class Factory e modelli factory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9329a0b8cfd22a316add88664604df190ae96c765359c723aa2302c5b1fa1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402216"
---
# <a name="class-factories-and-factory-templates"></a>Class Factory e modelli factory

Questo argomento descrive come implementare una DLL per un filtro DirectShow, usando le classi [DirectShow base](directshow-base-classes.md).

Prima che un client crei un'istanza di un oggetto COM, crea un'istanza del class factory dell'oggetto, usando una chiamata alla [**funzione CoGetClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) Il client chiama quindi il class factory **metodo IClassFactory::CreateInstance della** classe. È l'class factory che crea effettivamente il componente e restituisce un puntatore all'interfaccia richiesta. La [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) combina questi passaggi all'interno della chiamata di funzione.

Nella figura seguente viene illustrata la sequenza di chiamate al metodo .

![chiamate al metodo per creare un class factory](images/classfactory.png)

[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) chiama la [**funzione DllGetClassObject,**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) definita nella DLL. Questa funzione crea il class factory e restituisce un puntatore a un'interfaccia nel class factory. DirectShow **dllGetClassObject,** ma la funzione si basa sul codice in modo specifico. Per comprendere il funzionamento, è necessario comprendere come DirectShow class factory.

Un class factory è un oggetto COM dedicato alla creazione di un altro oggetto COM. Ogni class factory ha un tipo di oggetto creato. In DirectShow, ogni class factory è un'istanza della stessa classe C++, **CClassFactory**. Le class factory sono specializzate tramite un'altra classe, [**CFactoryTemplate**](cfactorytemplate.md), denominata anche *modello factory*. Ogni class factory contiene un puntatore a un modello di factory. Il modello factory contiene informazioni su un componente specifico, ad esempio l'identificatore di classe (CLSID) del componente e un puntatore a una funzione che crea il componente.

La DLL dichiara una matrice globale di modelli factory, uno per ogni componente nella DLL. Quando [**DllGetClassObject crea**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) un nuovo class factory, cerca nella matrice un modello con un CLSID corrispondente. Supponendo che ne trovi uno, crea un class factory che contiene un puntatore al modello corrispondente. Quando il client chiama **IClassFactory::CreateInstance,** il class factory chiama la funzione di creazione di istanze definita nel modello.

Nella figura seguente viene illustrata la sequenza di chiamate al metodo .

![class factory modelli in una DLL](images/classfactory2.png)

Il vantaggio di questa architettura è che è possibile definire solo alcuni elementi specifici del componente, ad esempio la funzione di creazione di istanze, senza implementare l'intero class factory.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una DLL DirectShow filtro](how-to-create-a-dll.md)
</dt> </dl>

 

 
