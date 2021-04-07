---
title: Interfacce IADs e IDirectoryObject
description: I client ADSI gestiscono e modificano oggetti servizio directory usando una delle due interfacce COM IADs o IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, informazioni
- IDirectoryObject ADSI, informazioni
- Interfacce ADSI ADSI, using, IADs e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dfef47fe1c66e4303725deecec14fe93d1fd92
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872965"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>Interfacce IADs e IDirectoryObject

I client ADSI gestiscono e modificano oggetti servizio directory usando una delle due interfacce COM seguenti: [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). **IADs** è un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) progettata per l'uso da parte di client ad associazione tardiva, ad esempio quelli scritti in Microsoft Visual Basic, Java e vari linguaggi di scripting. **IDirectoryObject** è un'interfaccia vtable che fornisce l'accesso diretto agli oggetti da client ad associazione anticipata, ad esempio quelli scritti in C e C++.

Ogni oggetto ADSI deve implementare sia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) che [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). I client ADSI scritti in linguaggi come C o C++, che sono in grado di accedere direttamente a vtable, possono usare entrambe le interfacce, ma non entrambe nella stessa applicazione. I client ADSI scritti in Visual Basic o Java sono limitati all'uso di **IADs**.

L'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) consente ai client ad associazione tardiva di sfruttare le funzionalità di manutenzione intrinseche del modello a oggetti ADSI. Tra queste funzionalità si trova la cache delle proprietà, che consente ai client di leggere e scrivere le proprietà senza passare attraverso la rete per ogni chiamata. Inoltre, le applicazioni client ottengono l'utilizzo di potenti librerie di controlli ActiveX e di interfaccia utente e uno stile di programmazione più semplice. In restituzione, i client ad associazione tardiva devono utilizzare il tipo di dati **Variant** , che impedisce l'utilizzo dei tipi di dati nativi più ricchi forniti da ADSI.

L'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) consente ai client con associazione anticipata di sfruttare tutti i vantaggi dei tipi di dati del servizio directory nativi, a scapito di un lieve vantaggio in termini di prestazioni rispetto all'utilizzo della cache delle proprietà. In restituzione, l'interfaccia **IDirectoryObject** fornisce l'accesso diretto e in transito alle proprietà degli oggetti tramite una singola richiesta, anziché tramite singole chiamate **Get** e **put** .

 

 