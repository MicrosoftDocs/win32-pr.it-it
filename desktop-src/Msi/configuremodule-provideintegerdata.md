---
description: Il metodo ProvideIntegerData dell'oggetto ConfigureModule viene chiamato Mergemod.dll recuperare dati integer dallo strumento client.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Metodo ConfigureModule.ProvideIntegerData (Mergemod.h)
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
ms.openlocfilehash: 96472a13902322d940dc7e756c3639f9befaf6764b3ede8521f27a885a50e8d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143690"
---
# <a name="configuremoduleprovideintegerdata-method"></a>Metodo ConfigureModule.ProvideIntegerData

Il **metodo ProvideIntegerData** dell'oggetto [**ConfigureModule**](configuremodule-object.md) viene chiamato Mergemod.dll per recuperare dati integer dallo strumento client.

Mergemod.dll il nome *della* voce corrispondente nella [tabella ModuleConfiguration](moduleconfiguration-table.md).

Lo strumento deve restituire S \_ OK e fornire l'intero di personalizzazione appropriato in *ConfigData*.

Se lo strumento non fornisce dati di configurazione per questo valore *Name,* la funzione deve restituire S \_ FALSE. In questo caso Mergemod.dll il valore dell'argomento *ConfigData* e usa il valore Predefinito della tabella ModuleConfiguration.

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

Il client può essere chiamato non più di una volta per ogni record nella [tabella ModuleConfiguration](moduleconfiguration-table.md). Si noti Mergemod.dll esegue mai più chiamate al client per lo stesso valore "Name". Se nessun record nella tabella ModuleSubstitution usa la proprietà , una voce nella tabella ModuleConfiguration non provoca chiamate al client.

### <a name="c"></a>C++

Vedere [**La funzione ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




