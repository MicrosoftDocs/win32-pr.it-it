---
title: Metodo INapComponentConfig3 DeleteAllConfig (NapCommon.h)
description: Viene implementato dai validator dell'integrità del sistema (SHV) per fornire un modo per ripristinare lo stato originale dell'archivio SHV dopo l'installazione.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Metodo DeleteAllConfig NAP
- Metodo DeleteAllConfig NAP , interfaccia INapComponentConfig3
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
ms.openlocfilehash: 05b2a81a33dfb659c3398c8c853132244d088b7fa65bd4bb0317869e13b85abf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621740"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a>Metodo INapComponentConfig3::D eleteAllConfig

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo DeleteAllConfig** viene implementato dai validator dell'integrità del sistema (SHV) per consentire di ripristinare lo stato originale dell'archivio SHV dopo l'installazione. Tutti i dati di configurazione, ad eccezione della configurazione predefinita, devono essere eliminati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                           | Descrizione                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | L'operazione è riuscita.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





