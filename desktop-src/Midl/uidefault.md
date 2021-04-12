---
title: uidefault (attributo)
description: L'attributo \ uidefault \ indica che il membro delle informazioni sul tipo è il membro predefinito per la visualizzazione nell'interfaccia utente.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- attributo MIDL di uidefault
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcef39f36abad7c7cb5562b2d892761bd1bb7b5b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398879"
---
# <a name="uidefault-attribute"></a>uidefault (attributo)

L'attributo **\[ uidefault \]** indica che il membro Information del tipo è il membro predefinito per la visualizzazione nell'interfaccia utente.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*Method-Attribute-List* 
</dt> <dd>

Altri attributi che si applicano al metodo.

</dd> <dt>

*tipo restituito* 
</dt> <dd>

Tipo di dati che il metodo restituirà al termine dell'esecuzione.

</dd> <dt>

*Nome metodo* 
</dt> <dd>

Nome del metodo.

</dd> <dt>

*elenco di parametri di metodo* 
</dt> <dd>

Zero o più parametri per il metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'applicazione dell'attributo **\[ uidefault \]** a un membro di un'interfaccia o di un'interfaccia dispatch indica Visual Basic, in fase di progettazione, di visualizzare automaticamente questo evento o proprietà all'utente. Ciò significa che quando l'utente fa doppio clic su un oggetto, Visual Basic passa all'evento nell'interfaccia di origine predefinita con l'attributo **\[ uidefault \]** . Quando l'utente seleziona un oggetto, il Visualizzatore proprietà di Visual Basic Visualizza la proprietà nell'interfaccia di origine predefinita con questo attributo. Se nessun evento o proprietà ha l'attributo **\[ uidefault \]** , Visual Basic Visualizza il primo evento o proprietà elencato nell'interfaccia predefinita.

### <a name="typeflag-representation"></a>Rappresentazione TYPEFLAG

Presenza di FUNCFLAG \_ FUIDEFAULT o VARFLAG \_ FUIDEFAULT

## <a name="examples"></a>Esempi

``` syntax
[
    dual,
    uuid(12345678-1234-1234-1234-123456789ABC),
    restricted
]
interface IForm: IDispatch
{
    [propget]HRESULT Backcolor([out, retval] long *Value);
    [propput]HRESULT Backcolor([in] long Value);
    [propget, uidefault]HRESULT Name([out, retval] BSTR *Value);
    [propput, uidefault]HRESULT Name([in] BSTR Value);
}
[
    odl,
    dual,
    uuid(87654321-1234-1234-1234-123456789ABC),
    restricted
] 
interface IFormEvents: IDispatch
{
    [uidefault]HRESULT Click();
    HRESULT Resize();
}

[
    uuid(12345678-1234-1234-1234-987654321ABC)
]
coclass Form
{
    [default] interface IForm;
    [default, source] interface IFormEvents;
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[Esempio di file di FAD](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file di FAD](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 