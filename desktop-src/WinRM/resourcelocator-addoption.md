---
title: Metodo ResourceLocator. AddOption (WSManDisp. h)
description: Aggiunge dati aggiuntivi necessari per elaborare la richiesta. Alcuni provider WMI, ad esempio, possono richiedere un oggetto IWbemContext o SWbemNamedValueSet con informazioni specifiche del provider.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo AddOption
- Metodo AddOption Gestione remota Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, metodo AddOption
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
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048013"
---
# <a name="resourcelocatoraddoption-method"></a>ResourceLocator. AddOption, metodo

Aggiunge dati aggiuntivi necessari per elaborare la richiesta. Alcuni provider WMI, ad esempio, possono richiedere un oggetto [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) con informazioni specifiche del provider. È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

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

*OptionName* \[ in\]
</dt> <dd>

Nome (chiave) dell'oggetto dati facoltativo.

</dd> <dt>

*OptionValue* \[ in\]
</dt> <dd>

Valore fornito per l'oggetto dati facoltativo.

</dd> <dt>

*mustComply* \[ in\]
</dt> <dd>

Flag che indica che l'opzione deve essere elaborata. Il valore predefinito è **false** (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

**IWSManResourceLocator:: AddOption** è il metodo C++ corrispondente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

