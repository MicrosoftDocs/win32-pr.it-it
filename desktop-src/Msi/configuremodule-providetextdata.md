---
description: Il metodo ProvideTextData viene chiamato da Mergemod.dll per recuperare i dati di testo dallo strumento client. Mergemod.dll fornisce il nome dalla voce corrispondente nella tabella ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Metodo ConfigureModule. ProvideTextData (Mergemod. h)
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332620"
---
# <a name="configuremoduleprovidetextdata-method"></a>ConfigureModule. ProvideTextData, metodo

Il metodo **ProvideTextData** viene chiamato da Mergemod.dll per recuperare i dati di testo dallo strumento client. Mergemod.dll fornisce il *nome* dalla voce corrispondente nella tabella ModuleConfiguration.

Lo strumento deve restituire S \_ OK e fornire il testo di personalizzazione appropriato in ConfigData. Lo strumento client è responsabile dell'allocazione dei dati, ma Mergemod.dllè responsabile del rilascio della memoria. Questo argomento deve essere un oggetto **BSTR** . **LPCWSTR** non è accettato.

Se lo strumento non fornisce dati di configurazione per questo valore del *nome* , la funzione deve restituire S \_ false. In questo caso Mergemod.dll ignora il valore dell'argomento ConfigData e usa il valore predefinito della tabella ModuleConfiguration.

Il codice restituito diverso da S \_ OK o s \_ false causerà la registrazione di un errore (se un log è aperto) e l'operazione di Unione avrà esito negativo.

Poiché questa funzione segue la convenzione **BSTR** standard, null equivale alla stringa vuota.

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

Il client può essere chiamato non più di una volta per ogni record nella [tabella ModuleConfiguration](moduleconfiguration-table.md). Si noti che Mergemod.dll non effettua mai più chiamate al client per lo stesso valore "Name". Se nessun record nella tabella ModuleSubstitution usa la proprietà, una voce nella tabella ModuleConfiguration non comporta chiamate al client.

### <a name="c"></a>C++

Vedere [**funzione ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




