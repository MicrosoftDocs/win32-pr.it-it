---
title: Metodo GetAttribute INapSoHProcessor (NapProtocol.h)
description: Recupera il tipo e il valore dell'attributo, in base alla posizione dell'attributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Metodo GetAttribute NAP
- Metodo GetAttribute NAP, interfaccia INapSoHProcessor
- Interfaccia INapSoHProcessor NAP, metodo GetAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba1b86ca1eab51fdca382a758a9a65650af2249eb0d605c24274c84d1f95669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939568"
---
# <a name="inapsohprocessorgetattribute-method"></a>Metodo INapSoHProcessor::GetAttribute

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSoHProcessor::GetAttribute** recupera il tipo e il valore dell'attributo, in base alla posizione dell'attributo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*attributeLocation* \[ Pollici\]
</dt> <dd>

Posizione (indice) dell'attributo di cui recuperare il tipo e il valore. Il valore di *attributeLocation* viene restituito da una chiamata precedente a [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).

</dd> <dt>

*type* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura SoHAttributeType**](sohattributetype-enum.md) che specifica il tipo dell'attributo nel *valore*.

</dd> <dt>

*value* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a [**una struttura SoHAttributeValue**](sohattributevalue-union.md) che contiene il valore dell'attributo definito dal *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





