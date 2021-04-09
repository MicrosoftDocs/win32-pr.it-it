---
title: Metodo WSMan. CreateResourceLocator (WSManDisp. h)
description: Crea un oggetto ResourceLocator che può essere usato invece di specificare un URI di risorsa nelle operazioni dell'oggetto sessione, ad esempio Session. Get, Session. put o Session. enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo CreateResourceLocator
- Metodo CreateResourceLocator Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo CreateResourceLocator
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
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964133"
---
# <a name="wsmancreateresourcelocator-method"></a>WSMan. CreateResourceLocator, metodo

Crea un oggetto [**resourceLocator**](resourcelocator.md) che può essere usato invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*URI* \[ di in, facoltativo\]
</dt> <dd>

URI di risorsa per la risorsa. Per altre informazioni sulle stringhe URI, vedere [URI di risorsa](resource-uris.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**resourceLocator**](resourcelocator.md) che può quindi essere utilizzato per eseguire operazioni WinRM locali o remote.

## <a name="remarks"></a>Commenti

Se la proprietà **FragmentDialect** non è specificata nell'oggetto [**resourceLocator**](resourcelocator.md) , il valore predefinito è la specifica XPath 1,0. Per altre informazioni, vedere [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene creato un oggetto [**resourceLocator**](resourcelocator.md) e viene ottenuto il valore della proprietà **Description** della scheda di rete dall'istanza di [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con indice "1".


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

