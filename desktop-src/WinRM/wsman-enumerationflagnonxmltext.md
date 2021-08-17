---
title: Metodo WSMan.EnumerationFlagNonXmlText (WSManDisp.h)
description: Restituisce il valore della costante di enumerazione WSManFlagNonXmlText da usare nel parametro flags del metodo Session.Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Metodo EnumerationFlagNonXmlText Windows gestione remota
- Metodo EnumerationFlagNonXmlText Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo EnumerationFlagNonXmlText
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6606a20d0ab7f59b7521367243ccdc97fd90209f1791d8f1ded3e48c70e3f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742290"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a>Metodo WSMan.EnumerationFlagNonXmlText

**WSMan.EnumerationFlagNonXmlText** restituisce il valore della costante di enumerazione **WSManFlagNonXmlText** da usare nel parametro *flags* del [**metodo Session.Enumerate.**](session-enumerate.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione.](session-constants.md)

**WSManFlagNonXmlText** è una costante **\_ \_ nell'enumerazione WSManEnumFlags.** Per altre informazioni, vedere [**Costanti di enumerazione.**](enumeration-constants.md)

## <a name="syntax"></a>Sintassi


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Cambio\]
</dt> <dd>

Valore della costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

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

[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





