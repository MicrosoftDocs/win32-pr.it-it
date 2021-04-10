---
title: Metodo Initialize INapSoHProcessor (NapProtocol. h)
description: Inizializza il pacchetto del protocollo e il sistema di elaborazione del rapporto di integrità. Questo metodo deve essere chiamato una sola volta.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapSoHProcessor
- Interfaccia NAP di INapSoHProcessor, metodo Initialize
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964220"
---
# <a name="inapsohprocessorinitialize-method"></a>Metodo INapSoHProcessor:: Initialize

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSoHProcessor:: Initialize** Inizializza il pacchetto del protocollo e il sistema di elaborazione del rapporto di integrità. Questo metodo deve essere chiamato una sola volta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

rapporto di *integrità* \[ in\]
</dt> <dd>

Puntatore al pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) da elaborare.

</dd> <dt>

*richiesta* \[ in\]
</dt> <dd>

**Bool** che è **true** se il pacchetto è un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se è un **SoHResponse**.

</dd> <dt>

*ID* in \[ uscita\]
</dt> <dd>

Un [SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'SHA o del servizio di convalida dell'integrità di sistema che ha creato il pacchetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione riuscita.<br/>                                    |
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

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





