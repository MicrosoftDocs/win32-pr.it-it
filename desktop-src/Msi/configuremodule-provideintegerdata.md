---
description: Il metodo ProvideIntegerData dell'oggetto ConfigureModule viene chiamato da Mergemod.dll per recuperare dati Integer dallo strumento client.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Metodo ConfigureModule. ProvideIntegerData (Mergemod. h)
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332621"
---
# <a name="configuremoduleprovideintegerdata-method"></a>ConfigureModule. ProvideIntegerData, metodo

Il metodo **ProvideIntegerData** dell' [**oggetto ConfigureModule**](configuremodule-object.md) viene chiamato da Mergemod.dll per recuperare dati Integer dallo strumento client.

Mergemod.dll fornisce il *nome* dalla voce corrispondente nella [tabella ModuleConfiguration](moduleconfiguration-table.md).

Lo strumento deve restituire S \_ OK e fornire l'intero di personalizzazione appropriato in *ConfigData*.

Se lo strumento non fornisce dati di configurazione per questo valore del *nome* , la funzione deve restituire S \_ false. In questo caso Mergemod.dll ignora il valore dell'argomento *ConfigData* e usa il valore predefinito della tabella ModuleConfiguration.

## <a name="syntax"></a>Sintassi


```JScript
ConfigureModule.ProvideIntegerData(
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

Vedere [**funzione ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




