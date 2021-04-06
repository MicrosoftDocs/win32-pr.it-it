---
title: Metodo INapComponentConfig3 DeleteAllConfig (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) per fornire un modo per reimpostare l'archivio di convalida integrità di sistema sullo stato originale dopo l'installazione.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- NAP metodo DeleteAllConfig
- Metodo DeleteAllConfig NAP, interfaccia INapComponentConfig3
- Interfaccia INapComponentConfig3 NAP, metodo DeleteAllConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873565"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>INapComponentConfig3::D Metodo eleteAllConfig

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **DeleteAllConfig** viene implementato da convalida integrità sistema (SHV) per fornire un modo per reimpostare l'archivio di convalida integrità di sistema sullo stato originale dopo l'installazione. È necessario eliminare tutti i dati di configurazione ad eccezione della configurazione predefinita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                           | Descrizione                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | L'operazione è riuscita.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





