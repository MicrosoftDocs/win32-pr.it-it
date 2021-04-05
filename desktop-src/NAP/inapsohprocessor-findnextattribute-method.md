---
title: Metodo INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Trova il percorso (indice) dell'attributo successivo del tipo indicato da SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- NAP metodo FindNextAttribute
- Metodo FindNextAttribute NAP, interfaccia INapSoHProcessor
- Interfaccia INapSoHProcessor NAP, metodo FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740223"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>Metodo INapSoHProcessor:: FindNextAttribute

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSoHProcessor:: FindNextAttribute** trova il percorso (indice) dell'attributo successivo del tipo indicato da *SoHAttributeType*.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fromLocation* \[ in\]
</dt> <dd>

Posizione iniziale (indice) nel pacchetto del rapporto di integrità (SoH) per iniziare la ricerca degli attributi. Questo valore deve essere compreso nell'intervallo da 0 a (**numAttrib** -1) in cui **numAttrib** viene recuperato utilizzando [**INapSoHProcessor:: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).

> [!Note]  
> Il pacchetto di rapporto di integrità utilizza gli indici degli attributi in base 0.

 

</dd> <dt>

*tipo* \[ di in\]
</dt> <dd>

Struttura [**SoHAttributeType**](sohattributetype-enum.md) che contiene il tipo di attributo da individuare.

</dd> <dt>

*attributeLocation* \[ out\]
</dt> <dd>

Puntatore che contiene il percorso (indice) nel pacchetto SoH del primo attributo di tipo *SoHAttributeType* dall'indice *fromLocation*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**FILE di errore \_ \_ non \_ trovato**</dt> </dl> | Attributo non trovato.<br/>                                    |



 

## <a name="remarks"></a>Commenti

Il metodo **FindNextAttribute** cerca gli attributi di tipo *SoHAttributeType* dall'indice specificato da *fromLocation* e versioni successive fino a quando non viene trovata una corrispondenza. Se non viene trovata alcuna corrispondenza, viene restituito il **file di errore \_ \_ non \_ trovato** .

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

 

 





