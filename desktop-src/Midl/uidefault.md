---
title: uidefault (attributo)
description: L'attributo \uidefault\ indica che il membro delle informazioni sul tipo è il membro predefinito per la visualizzazione nell'interfaccia utente.
ms.assetid: e789be38-a509-437d-89c9-ebbc830e5ae2
keywords:
- Attributo uidefault MIDL
topic_type:
- apiref
api_name:
- uidefault
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891d37611eb931a8857157434419e5221e808710290f2e209f50c743bcb5b7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013479"
---
# <a name="uidefault-attribute"></a>uidefault (attributo)

**\[ L'attributo \] uidefault** indica che il membro delle informazioni sul tipo è il membro predefinito per la visualizzazione nell'interfaccia utente.

``` syntax
[method-attribute-list, uidefault]return-type method-name(method-parameter-list)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*method-attribute-list* 
</dt> <dd>

Altri attributi che si applicano al metodo.

</dd> <dt>

*return-type* 
</dt> <dd>

Tipo di dati che il metodo restituirà al termine dell'esecuzione.

</dd> <dt>

*method-name* 
</dt> <dd>

Nome del metodo.

</dd> <dt>

*elenco dei parametri dei metodi* 
</dt> <dd>

Zero o più parametri per il metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'applicazione dell'attributo **\[ uidefault \]** a un membro di un'interfaccia o a un'interfaccia dispatch indica Visual Basic, in fase di progettazione, di visualizzare automaticamente questo evento o proprietà all'utente. Ciò significa che quando l'utente fa doppio clic su un oggetto, Visual Basic passa all'evento nell'interfaccia di origine predefinita con **\[ l'attributo uidefault. \]** Quando l'utente seleziona un oggetto, Visual Basic del browser Proprietà visualizza la proprietà nell'interfaccia di origine predefinita con questo attributo. Se nessun evento o proprietà ha l'attributo **\[ uidefault, \]** Visual Basic visualizza il primo evento o proprietà elencato nell'interfaccia predefinita.

### <a name="typeflag-representation"></a>Rappresentazione del flag di tipo

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

[Esempio di file ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintassi del file ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 