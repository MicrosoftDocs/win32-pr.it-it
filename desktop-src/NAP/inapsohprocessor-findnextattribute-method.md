---
title: Metodo INapSoHProcessor FindNextAttribute (NapProtocol.h)
description: Trova la posizione (indice) dell'attributo successivo del tipo indicato da SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Metodo FindNextAttribute NAP
- Metodo FindNextAttribute NAP , interfaccia INapSoHProcessor
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
ms.openlocfilehash: 4425707487994904d1bd2a622cd1ab66f286469c93e80a8eb01e71c0319426ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939578"
---
# <a name="inapsohprocessorfindnextattribute-method"></a>Metodo INapSoHProcessor::FindNextAttribute

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSoHProcessor::FindNextAttribute** trova la posizione (indice) dell'attributo successivo del tipo indicato da *SoHAttributeType.*

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

*fromLocation* \[ Pollici\]
</dt> <dd>

Posizione iniziale (indice) nel pacchetto Statement of Health (SoH) per iniziare la ricerca degli attributi. Questo valore deve essere compreso nell'intervallo compreso tra 0 e (**numAttrib** - 1) in cui **numAttrib** viene recuperato tramite [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).

> [!Note]  
> Il pacchetto SoH usa indici di attributi basati su 0.

 

</dd> <dt>

*type* \[ Pollici\]
</dt> <dd>

Struttura [**SoHAttributeType**](sohattributetype-enum.md) che contiene il tipo di attributo da individuare.

</dd> <dt>

*attributeLocation* \[ Cambio\]
</dt> <dd>

Puntatore che contiene la posizione (indice) nel pacchetto SoH del primo attributo di tipo *SoHAttributeType* *dall'indice fromLocation*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>        | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**FILE \_ DI ERRORE NON \_ \_ TROVATO**</dt> </dl> | Attributo non trovato.<br/>                                    |



 

## <a name="remarks"></a>Commenti

Il **metodo FindNextAttribute** cerca gli attributi di tipo *SoHAttributeType* dall'indice specificato da *fromLocation* e versioni successive fino a quando non viene trovata una corrispondenza. Se non viene trovata alcuna corrispondenza, **viene restituito ERROR \_ FILE \_ NOT \_** FOUND.

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

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





