---
title: Metodo WSMan.CreateResourceLocator (WSManDisp.h)
description: Crea un oggetto ResourceLocator che può essere usato invece di specificare un URI di risorsa nelle operazioni dell'oggetto Session, ad esempio Session.Get, Session.Put o Session.Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Metodo CreateResourceLocator Windows gestione remota
- Metodo CreateResourceLocator Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d78276f40ee6e2e1aff10f17bc9f41bb1d1e4aa32cde68a41842c5cee8b95bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742613"
---
# <a name="wsmancreateresourcelocator-method"></a>Metodo WSMan.CreateResourceLocator

Crea un [**oggetto ResourceLocator**](resourcelocator.md) che può essere usato invece di specificare un URI di risorsa [**nelle**](session.md) operazioni dell'oggetto Session, ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

## <a name="syntax"></a>Sintassi


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*uri* \[ in, facoltativo\]
</dt> <dd>

URI della risorsa. Per altre informazioni sulle stringhe URI, vedere [URI delle risorse.](resource-uris.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**ResourceLocator**](resourcelocator.md) che può quindi essere usato per eseguire operazioni WinRM locali o remote.

## <a name="remarks"></a>Commenti

Se la **proprietà FragmentDialect** non è specificata nell'oggetto [**ResourceLocator,**](resourcelocator.md) il valore predefinito è la specifica XPath 1.0. Per altre informazioni, vedere [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente crea un oggetto [**ResourceLocator**](resourcelocator.md) e ottiene il valore della proprietà **Description** della scheda di rete dall'istanza di [**\_ Win32 NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con indice "1".


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

