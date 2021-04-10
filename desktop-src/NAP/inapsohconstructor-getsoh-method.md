---
title: Metodo INapSoHConstructor GetSoH (NapProtocol. h)
description: Recupera il pacchetto SoHRequest o SoHResponse costruito.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- NAP metodo GetSoH
- Metodo GetSoH NAP, interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP, metodo GetSoH
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
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119643"
---
# <a name="inapsohconstructorgetsoh-method"></a>Metodo INapSoHConstructor:: GetSoH

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSoHConstructor:: GetSoH** Recupera il pacchetto SoHRequest o SoHResponse costruito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

rapporto di *integrità* \[ out\]
</dt> <dd>

Puntatore a un puntatore al pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) o **SoHResponse** costruito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                   |
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

[**INapSoHConstructor**](inapsohconstructor.md)
</dt> </dl>

 

 





