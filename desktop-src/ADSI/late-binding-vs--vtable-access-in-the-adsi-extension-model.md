---
title: Associazione tardiva e accesso Vtable nel modello di estensione ADSI
description: Una doppia interfaccia consente l'accesso vtable diretto a tutte le funzioni, mentre un'interfaccia dispatch non lo fa.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- Associazione tardiva e accesso vtable nel modello di estensione ADSI ADSI
- estensioni ADSI, associazione tardiva e accesso vtable nel modello di estensione ADSI
- ADSI ADSI , codice di esempio Visual Basic , con IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eacc2008d3da33cd8d1897eeff2c30301849f9ec306656fc494072c33608c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023359"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Associazione tardiva e accesso Vtable nel modello di estensione ADSI

Una doppia interfaccia consente l'accesso vtable diretto a tutte le funzioni, mentre un'interfaccia dispatch non lo fa. Un client C/C++ può eseguire una query per un puntatore a interfaccia doppia e usare l'accesso vtable diretto per richiamare le relative funzioni. In questo modo l'accesso è più rapido rispetto alla chiamata della funzione tramite le funzioni [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) Questo vale soprattutto nel modello di estensione, perché tutte le interfacce duali in un oggetto di estensione devono delegare prima le funzioni **GetIDsOfNames** e **Invoke** all'aggregatore (ADSI). L'aggregatore deve quindi eseguire passaggi interni aggiuntivi per identificare quale oggetto di estensione, eventualmente includendo l'aggregatore stesso, fornisce il supporto per la funzione chiamata e reindirizza la chiamata all'oggetto appropriato.

Visual Basic richiama anche una funzione a doppia interfaccia usando l'accesso diretto a una tabella vtable, se ha un puntatore all'interfaccia e l'accesso ai dati di tipo dalla libreria dei tipi. I client ADSI scritti in Visual Basic possono specificare un puntatore a un'interfaccia duale, ad esempio [**IAD**](/windows/desktop/api/Iads/nn-iads-iads), in modo esplicito e quindi abilitare l'accesso vtable alle funzioni nell'interfaccia.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Poiché [**un'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) non supporta l'accesso vtable, questo esempio non è applicabile. In altre informazioni, una funzione dispatch viene sempre richiamata solo tramite le funzioni [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)

Le versioni correnti di VBScript e JScript non supportano l'accesso vtable. Pertanto, un'interfaccia duale in un ambiente VBScript o JScript funziona come un'interfaccia dispatch.

 

 