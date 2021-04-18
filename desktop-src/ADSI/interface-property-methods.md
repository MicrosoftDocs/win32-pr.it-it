---
title: Metodi di proprietà dell'interfaccia
description: Molte interfacce ADSI sono progettate per supportare l'automazione e pertanto sono interfacce duali che supportano l'accesso client tramite le interfacce IUnknown e IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà dell'interfaccia
- ADSI ADSI, Reference, method Property Explained
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300452"
---
# <a name="interface-property-methods"></a>Metodi di proprietà dell'interfaccia

Molte interfacce ADSI sono progettate per supportare l'automazione e pertanto sono interfacce duali che supportano l'accesso client tramite le interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . I client non di automazione, ad esempio quelli scritti in C/C++, risolvono direttamente la chiamata al metodo, usando il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e chiamano direttamente il metodo. I client di automazione, noti anche come client associati al nome, ad esempio quelli scritti in Visual Basic o Visual Basic Scripting Edition (VBScript), devono risolvere indirettamente la chiamata al metodo usando il metodo [**Dispatch**](/previous-versions/windows/desktop/automat/dispinterface) .

Un'interfaccia ADSI che supporta l'automazione definisce i metodi di proprietà per il recupero e la modifica delle proprietà di un oggetto che implementa l'interfaccia. I metodi di proprietà hanno nomi con **Get** \_ e **put** \_ anteposti ai nomi di proprietà appropriati, ad esempio **get \_ User** e **put \_ Name**.

Ogni **metodo \_ Get** accetta un solo parametro come output. Questo parametro è un indirizzo allocato dal metodo di una variabile del tipo di dati della proprietà. Alla restituzione, questa variabile presuppone il valore corrente della proprietà richiesta. Il chiamante deve rilasciare la memoria allocata della variabile quando la proprietà non è più necessaria.

Ogni **metodo \_ put** accetta un solo parametro come input per il tipo di dati della proprietà corrispondente. Il parametro include un nuovo valore della proprietà.

Nell'esempio di codice seguente viene illustrata la chiamata dei metodi di proprietà che seguono la routine consueta per chiamare la funzione membro di un oggetto.


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



Nell'esempio di codice seguente viene illustrata la chiamata dei metodi di proprietà nei client di automazione, che possono essere leggermente diversi. Ad esempio, Visual Basic usa la notazione del punto.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



Tutti i parametri e i tipi restituiti devono essere di quelli definiti dal tipo di dati VARIANT. Tutti i metodi su un'interfaccia doppia restituiscono un valore HRESULT per indicare l'esito positivo o negativo.

Per ulteriori informazioni su come ottenere e impostare le proprietà sugli oggetti ADSI, vedere la pagina relativa alla [cache delle proprietà](property-cache-interfaces.md).

 

 