---
description: Il metodo ProvideTextData viene chiamato da Mergemod.dll per recuperare dati di testo dallo strumento client. Mergemod.dll il nome della voce corrispondente nella tabella ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Metodo ConfigureModule.ProvideTextData (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9712b7e7f619e40ba3804d7c5671c6855e7982eddd2c4c964f172845cf5de465
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143718"
---
# <a name="configuremoduleprovidetextdata-method"></a>Metodo ConfigureModule.ProvideTextData

Il **metodo ProvideTextData** viene chiamato da Mergemod.dll per recuperare dati di testo dallo strumento client. Mergemod.dll il nome *della* voce corrispondente nella tabella ModuleConfiguration.

Lo strumento deve restituire S \_ OK e fornire il testo di personalizzazione appropriato in ConfigData. Lo strumento client è responsabile dell'allocazione dei dati, Mergemod.dllè responsabile del rilascio della memoria. Questo argomento DEVE essere un **oggetto BSTR.** **LPCWSTR** NON è accettato.

Se lo strumento non fornisce dati di configurazione per questo valore *Name,* la funzione deve restituire S \_ FALSE. In questo caso Mergemod.dll il valore dell'argomento ConfigData e usa il valore Predefinito della tabella ModuleConfiguration.

Qualsiasi codice restituito diverso da S OK o S FALSE causerà la registrazione di un errore (se un log è aperto) e l'unione avrà esito \_ \_ negativo.

Poiché questa funzione segue la **convenzione BSTR** standard, Null equivale alla stringa vuota.

## <a name="syntax"></a>Sintassi


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* 
</dt> <dd>

Nome dell'elemento per il quale vengono recuperati i dati.

</dd> <dt>

*ConfigData* 
</dt> <dd>

Puntatore al testo di personalizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il client può essere chiamato non più di una volta per ogni record nella [tabella ModuleConfiguration](moduleconfiguration-table.md). Si noti Mergemod.dll esegue mai più chiamate al client per lo stesso valore "Name". Se nessun record nella tabella ModuleSubstitution usa la proprietà , una voce nella tabella ModuleConfiguration non provoca chiamate al client.

### <a name="c"></a>C++

Vedere [**La funzione ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




