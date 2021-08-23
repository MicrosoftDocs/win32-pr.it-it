---
title: Metodo AppendAttribute INapSoHConstructor (NapProtocol.h)
description: Aggiunge un TLV alla fine del buffer SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Metodo AppendAttribute NAP
- Metodo AppendAttribute NAP , interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP , metodo AppendAttribute
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7d7ca4636d0eaeea35054dc5330b17f1360dffec5231922ad0acc357231c3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939588"
---
# <a name="inapsohconstructorappendattribute-method"></a>Metodo INapSoHConstructor::AppendAttribute

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSoHConstructor::AppendAttribute** aggiunge un TLV alla fine del buffer SoH.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* \[ Pollici\]
</dt> <dd>

Enumerazione [**SoHAttributeType**](sohattributetype-enum.md) che indica il tipo di attributo della nuova TLV.

</dd> <dt>

*value* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura SoHAttributeValue**](sohattributevalue-union.md) che contiene il valore per la nuova TLV.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Il [**TLV sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) non deve essere aggiunto usando questa funzione. Viene aggiunto come primo TLV da [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) ai pacchetti SOH appena costruiti.

Quando si aggiunge un attributo che verrà utilizzato dal sistema nap, non deve essere crittografato o modificato in alcun modo. Se HealthEntity richiede la crittografia/controllo dell'integrità (MAC) delle informazioni private, deve essere incluso solo nell'attributo [**sohAttributeTypeVendorSpecific.**](sohattributetype-enum.md)

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





