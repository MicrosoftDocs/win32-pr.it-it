---
title: Metodo GetAttribute INapSoHProcessor (NapProtocol. h)
description: Recupera il tipo di attributo e il valore, in base alla posizione dell'attributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Metodo GetAttribute NAP
- Metodo GetAttribute NAP, interfaccia INapSoHProcessor
- Interfaccia NAP di INapSoHProcessor, metodo GetAttribute
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
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301066"
---
# <a name="inapsohprocessorgetattribute-method"></a>Metodo INapSoHProcessor:: GetAttribute

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSoHProcessor:: GetAttribute** Recupera il tipo e il valore dell'attributo, data la posizione dell'attributo.

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

*attributeLocation* \[ in\]
</dt> <dd>

Posizione (indice) dell'attributo di cui devono essere recuperati il tipo e il valore. Il valore di *attributeLocation* viene restituito da una chiamata precedente a [**INapSoHProcessor:: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).

</dd> <dt>

*tipo* \[ di out\]
</dt> <dd>

Puntatore a una struttura [**SoHAttributeType**](sohattributetype-enum.md) che specifica il tipo di attributo in *value*.

</dd> <dt>

*valore* \[ di out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**SoHAttributeValue**](sohattributevalue-union.md) che contiene il valore dell'attributo in base a quanto definito dal *tipo*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





