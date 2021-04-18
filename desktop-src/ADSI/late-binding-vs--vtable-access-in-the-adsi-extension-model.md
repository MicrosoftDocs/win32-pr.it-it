---
title: Associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI
description: Una doppia interfaccia consente l'accesso diretto a vtable a tutte le relative funzioni, mentre un'interfaccia di dispatch non lo supporta.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI ADSI
- estensioni ADSI, associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI
- ADSI ADSI, esempio di codice Visual Basic, uso di IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300451"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Associazione tardiva rispetto all'accesso vtable nel modello di estensione ADSI

Una doppia interfaccia consente l'accesso diretto a vtable a tutte le relative funzioni, mentre un'interfaccia di dispatch non lo supporta. Un client C/C++ può eseguire una query per un puntatore a interfaccia duale e usare l'accesso diretto a vtable per richiamare le relative funzioni. Questo consente un accesso più rapido rispetto alla chiamata della funzione tramite le funzioni [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) . Ciò è particolarmente vero nel modello di estensione, perché tutte le interfacce duali in un oggetto di estensione devono delegare le funzioni **GetIDsOfNames** e **Invoke** prima di tutto a Aggregator (ADSI). L'aggregatore deve quindi eseguire ulteriori passaggi interni per identificare l'oggetto di estensione, eventualmente incluso l'aggregatore stesso, fornisce il supporto per la funzione chiamata e reindirizza la chiamata all'oggetto appropriato.

Visual Basic richiama inoltre una funzione a doppia interfaccia utilizzando l'accesso diretto a un oggetto vtable, se dispone di un puntatore all'interfaccia e l'accesso ai dati del tipo dalla libreria dei tipi. I client ADSI scritti in Visual Basic possono specificare un puntatore a un'interfaccia duale, ad esempio [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), in modo esplicito e quindi abilitare l'accesso vtable alle funzioni nell'interfaccia.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Poiché un'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) non supporta l'accesso vtable, questo esempio non è applicabile. Ovvero, una funzione Dispatch viene sempre richiamata tramite le funzioni [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .

Anche le versioni correnti di VBScript e JScript non supportano l'accesso vtable. Pertanto, un'interfaccia duale in un ambiente VBScript o JScript viene eseguita come un'interfaccia dispatch.

 

 