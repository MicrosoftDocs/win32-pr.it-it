---
title: Interfacce IAD e IDirectoryObject
description: I client ADSI gestiscono e modificano gli oggetti del servizio directory usando una delle due interfacce COM IAD o IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI ,about
- IDirectoryObject ADSI , informazioni
- Interfacce ADSI ADSI ,using,IADs e IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dccfa643c0076224abece6f449f20caf5a4de5d378c03d37cf0e2248ed5a50b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838381"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>Interfacce IAD e IDirectoryObject

I client ADSI gestiscono e modificano gli oggetti del servizio directory usando una delle due interfacce COM: [**IAD**](/windows/desktop/api/Iads/nn-iads-iads) o [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). **IAD** è [**un'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) destinata all'uso da parte di client ad associazione tardiva, ad esempio quelli scritti in Microsoft Visual Basic, Java e diversi linguaggi di scripting. **IDirectoryObject è** un'interfaccia vtable che fornisce l'accesso diretto agli oggetti da parte di client ad associazione anticipata, ad esempio quelli scritti in C e C++.

Ogni oggetto ADSI deve implementare sia [**IAD**](/windows/desktop/api/Iads/nn-iads-iads) che [**IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) I client ADSI scritti in linguaggi come C o C++, in grado di accedere direttamente alle tabelle vtable, possono usare entrambe le interfacce, ma non entrambe nella stessa applicazione. I client ADSI scritti in Visual Basic o Java sono limitati all'uso **di IAD.**

[**L'interfaccia IADs**](/windows/desktop/api/Iads/nn-iads-iads) consente ai client ad associazione tardiva di sfruttare le funzionalità intrinseche di gestione del modello a oggetti ADSI. Tra queste funzionalità è disponibile la cache delle proprietà, che consente ai client di leggere e scrivere proprietà senza andare in rete per ogni chiamata. Inoltre, le applicazioni client ottengono l'uso di potenti librerie di controlli ActiveX interfaccia utente e di uno stile di programmazione più semplice. In cambio, i client ad associazione tardiva devono usare il tipo di dati **VARIANT,** che preclude l'uso dei tipi di dati nativi più complessi forniti da ADSI.

[**L'interfaccia IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) consente ai client ad associazione anticipata di sfruttare appieno i tipi di dati nativi del servizio directory, a s costo di rinunciare a un leggero vantaggio in termini di prestazioni dall'uso della cache delle proprietà. In cambio, **l'interfaccia IDirectoryObject** fornisce l'accesso diretto in transito alle proprietà dell'oggetto tramite una singola richiesta, anziché tramite singole **chiamate get** e **put.**

 

 