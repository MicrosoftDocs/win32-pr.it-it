---
title: Metodo INapSoHConstructor AppendAttribute (NapProtocol. h)
description: Aggiunge un TLV alla fine del buffer del rapporto di integrità.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- NAP Metodo AppendAttribute
- Metodo AppendAttribute NAP, interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP, Metodo AppendAttribute
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
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517709"
---
# <a name="inapsohconstructorappendattribute-method"></a>Metodo INapSoHConstructor:: AppendAttribute

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSoHConstructor:: AppendAttribute** aggiunge un TLV alla fine del buffer del rapporto di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tipo* \[ di in\]
</dt> <dd>

Enumerazione [**SoHAttributeType**](sohattributetype-enum.md) che indica il tipo di attributo del nuovo TLV.

</dd> <dt>

*valore* \[ di in\]
</dt> <dd>

Puntatore a una struttura [**SoHAttributeValue**](sohattributevalue-union.md) contenente il valore per il nuovo TLV.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Non è necessario aggiungere [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV con questa funzione. Viene aggiunto come primo TLV da [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md) ai pacchetti SOH appena costruiti.

Quando si aggiunge un attributo che verrà utilizzato dal sistema NAP, non deve essere crittografato o modificato in alcun modo. Se il HealthEntity richiede il controllo di crittografia/integrità (MACs) delle informazioni private, deve essere incluso solo nell'attributo [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .

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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





