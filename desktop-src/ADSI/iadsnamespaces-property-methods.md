---
title: Metodi della proprietà IADsNamespaces (Iads.h)
description: I metodi delle proprietà dell'interfaccia IADsNamespaces ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà di interfaccia.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsNamespaces ADSI
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
ms.openlocfilehash: e8daeed67202add437ee06b9905cbd70a0c202863c476155216f2340be1c7b70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691429"
---
# <a name="iadsnamespaces-property-methods"></a>Metodi della proprietà IADsNamespaces

I [**metodi delle proprietà dell'interfaccia IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**DefaultContainer**
</dt> <dd> <dl>

La **proprietà DefaultContainer** identifica un oggetto contenitore di base a cui è possibile associare e usare come punto di partenza durante l'esplorazione. Questi dati vengono archiviati e recuperati dal valore del Registro di sistema seguente.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

ADSI definisce la **proprietà DefaultContainer** per fornire un modo rapido per ottenere un puntatore a un oggetto contenitore ADSI definito in precedenza.

<dt>

Tipo di accesso: Lettura/scrittura
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

I provider devono fornire questa proprietà per singolo utente. Il contenitore predefinito viene impostato immediatamente dopo la chiamata di **IADsNamespaces::p ut \_ DefaultContainer**. Non [**è necessario chiamare IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) In realtà, l'oggetto namespaces fornito dal sistema restituisce **E \_ NOTIMPL** per il metodo **IADs.SetInfo** chiamato su questo oggetto. Quando un contenitore è l'oggetto namespaces, un'operazione di enumerazione restituisce sempre un elenco di oggetti spazio dei nomi specifici del provider. Quando [**si usa IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) per ottenere un oggetto spazio dei nomi, il *parametro bstrClass* viene ignorato. Ciò è dovuto al fatto che il contenitore, cio' l'oggetto namespaces, contiene un solo tipo di oggetto, in particolare gli oggetti dello spazio dei nomi specifici del provider.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNamespaces è definito come 28B96BA0-B330-11CF-A9AD-00AA006BC149<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[Metodi delle proprietà dell'interfaccia](interface-property-methods.md)
</dt> </dl>

 

 





