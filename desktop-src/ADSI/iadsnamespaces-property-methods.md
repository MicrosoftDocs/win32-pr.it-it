---
title: Metodi di proprietà IADsNamespaces (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsNamespaces ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsNamespaces ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742695"
---
# <a name="iadsnamespaces-property-methods"></a>Metodi di proprietà IADsNamespaces

I metodi di proprietà dell'interfaccia [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

La proprietà **DefaultContainer** identifica un oggetto contenitore di base a cui è possibile associare e utilizzare come punto di partenza per l'esplorazione. Questi dati vengono archiviati e recuperati dal seguente valore del registro di sistema.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI definisce la proprietà **DefaultContainer** per fornire un metodo rapido per ottenere un puntatore a un oggetto contenitore ADSI definito in precedenza.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

I provider devono fornire questa proprietà per ogni singolo utente. Il contenitore predefinito viene impostato immediatamente dopo la chiamata di **IADsNamespaces::p UT \_ DefaultContainer**. La chiamata a [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) non è obbligatoria. Infatti, l'oggetto Namespaces fornito dal sistema restituisce **E \_ NOTIMPL** per il metodo **IADs. seinfo** chiamato su questo oggetto. Quando un contenitore è l'oggetto Namespaces, un'operazione di enumerazione restituisce sempre un elenco di oggetti spazio dei nomi specifici del provider. Quando si usa [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) per ottenere un oggetto spazio dei nomi, il parametro *bstrClass* viene ignorato. Questo è dovuto al fatto che il contenitore, ovvero l'oggetto Namespaces, contiene un solo tipo di oggetto, ovvero oggetti spazio dei nomi specifici del provider.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNamespaces è definito come 28B96BA0-B330-11CF-A9AD-00AA006BC149<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Metodi di proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





