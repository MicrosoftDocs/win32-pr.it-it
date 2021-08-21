---
title: Metodo GetSoH INapSoHConstructor (NapProtocol.h)
description: Recupera il pacchetto SoHRequest o SoHResponse costruito.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- Metodo GetSoH NAP
- Metodo GetSoH NAP, interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP , metodo GetSoH
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d411d57ae77a1e5bf8c04ca0d9d980a9c33e9fcf15eb05f157ddeda98711c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133824"
---
# <a name="inapsohconstructorgetsoh-method"></a>Metodo INapSoHConstructor::GetSoH

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSoHConstructor::GetSoH** recupera il pacchetto SoHRequest o SoHResponse costruito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*soh* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore al pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) o **SoHResponse** costruito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>NapProtocol.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapProtocol.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





