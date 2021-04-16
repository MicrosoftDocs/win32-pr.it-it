---
description: Questo argomento descrive come implementare una DLL per un filtro DirectShow usando le classi base di DirectShow.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Class factory e modelli di Factory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02699a8ff0740ddcf1d86b8514fd45dac9e32ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563766"
---
# <a name="class-factories-and-factory-templates"></a>Class factory e modelli di Factory

Questo argomento descrive come implementare una DLL per un filtro DirectShow usando le [classi base di DirectShow](directshow-base-classes.md).

Prima che un client crei un'istanza di un oggetto COM, crea un'istanza del class factory dell'oggetto, usando una chiamata alla funzione [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) . Il client chiama quindi il metodo **IClassFactory:: CreateInstance** del class factory. Si tratta del class factory che crea effettivamente il componente e restituisce un puntatore all'interfaccia richiesta. La funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) combina questi passaggi, all'interno della chiamata di funzione.

Nella figura seguente viene illustrata la sequenza di chiamate al metodo.

![chiamate al metodo per creare un class factory](images/classfactory.png)

[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) chiama la funzione [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , definita nella dll. Questa funzione crea il class factory e restituisce un puntatore a un'interfaccia nel class factory. DirectShow implementa **DllGetClassObject** per l'utente, ma la funzione si basa sul codice in un modo specifico. Per comprendere il funzionamento, è necessario comprendere il modo in cui DirectShow implementa le class factory.

Un class factory è un oggetto COM dedicato alla creazione di un altro oggetto COM. Ogni class factory dispone di un tipo di oggetto creato. In DirectShow ogni class factory è un'istanza della stessa classe C++, **CClassFactory**. Le class factory sono specializzate per mezzo di un'altra classe, [**CFactoryTemplate**](cfactorytemplate.md), detto anche *modello Factory*. Ogni class factory include un puntatore a un modello Factory. Il modello Factory contiene informazioni su un componente specifico, ad esempio l'identificatore di classe (CLSID) del componente, e un puntatore a una funzione che crea il componente.

La DLL dichiara una matrice globale di modelli Factory, uno per ogni componente della DLL. Quando [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuovo class factory, Cerca nella matrice un modello con un CLSID corrispondente. Presumendo che ne trovi uno, viene creato un class factory che include un puntatore al modello corrispondente. Quando il client chiama **IClassFactory:: CreateInstance**, il class factory chiama la funzione di creazione di istanze definita nel modello.

Nella figura seguente viene illustrata la sequenza di chiamate al metodo.

![modelli di class factory in una dll](images/classfactory2.png)

Il vantaggio di questa architettura è che è possibile definire solo alcuni aspetti specifici del componente, ad esempio la funzione di creazione di istanze, senza implementare l'intera class factory.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare una DLL di filtro DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
