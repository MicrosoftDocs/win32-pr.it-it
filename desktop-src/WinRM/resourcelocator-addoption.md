---
title: Metodo ResourceLocator.AddOption (WSManDisp.h)
description: Aggiunge dati aggiuntivi necessari per elaborare la richiesta. Ad esempio, alcuni provider WMI possono richiedere un oggetto IWbemContext o SWbemNamedValueSet con informazioni specifiche del provider.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Metodo AddOption Windows Gestione remota
- Metodo AddOption Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Windows gestione remota, metodo AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c03e587c4884e6d9efc3b98bdd7b41b4204a783e153d9e59a400a4e4bc02a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112966"
---
# <a name="resourcelocatoraddoption-method"></a>Metodo ResourceLocator.AddOption

Aggiunge dati aggiuntivi necessari per elaborare la richiesta. Ad esempio, alcuni provider WMI possono richiedere un [**oggetto IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) con informazioni specifiche del provider. È possibile fornire un [**oggetto ResourceLocator**](resourcelocator.md) anziché specificare un URI di risorsa nelle operazioni dell'oggetto [**Session,**](session.md) ad esempio [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OptionName* \[ Pollici\]
</dt> <dd>

Nome (chiave) dell'oggetto dati facoltativo.

</dd> <dt>

*OptionValue* \[ Pollici\]
</dt> <dd>

Valore fornito per l'oggetto dati facoltativo.

</dd> <dt>

*mustComply* \[ Pollici\]
</dt> <dd>

Flag che indica che l'opzione deve essere elaborata. Il valore predefinito **è False** (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

**IWSManResourceLocator::AddOption** è il metodo C++ corrispondente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

