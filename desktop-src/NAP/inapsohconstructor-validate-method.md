---
title: Metodo Validate INapSoHConstructor (NapProtocol. h)
description: Verifica la validità del pacchetto SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Convalida NAP metodo
- Metodo Validate NAP, interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP, metodo Validate
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742607"
---
# <a name="inapsohconstructorvalidate-method"></a>Metodo INapSoHConstructor:: Validate

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSoHConstructor:: Validate** controlla la validità del pacchetto SOH.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

rapporto di *integrità* \[ in\]
</dt> <dd>

Puntatore al pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) costruito.

</dd> <dt>

*richiesta* \[ in\]
</dt> <dd>

**Bool** che è **true** se il pacchetto è un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se è un **SoHResponse**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Il pacchetto del rapporto di integrità è valido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**NAP \_ E \_ pacchetto non valido \_**</dt> </dl> | Il pacchetto del rapporto di integrità non è valido.<br/>                              |



 

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

 

 





