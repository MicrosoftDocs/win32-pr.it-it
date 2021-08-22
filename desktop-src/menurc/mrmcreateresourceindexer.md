---
title: Funzione MrmCreateResourceIndexer (MrmResourceIndexer.h)
description: Crea un indicizzatore di risorse, usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP. Per altre informazioni e procedure dettagliate basate su scenario su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti e sistemi di compilazione personalizzati.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menu della funzione MrmCreateResourceIndexer e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d427163862d084c4a386fdf47cbd8586cb1a3489b18fb081471fbd31c86854b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601811"
---
# <a name="mrmcreateresourceindexer-function"></a>Funzione MrmCreateResourceIndexer

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea un indicizzatore di risorse, usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP. Per altre informazioni e procedure dettagliate basate su scenario su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti e sistemi [di compilazione personalizzati.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*packageFamilyName* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Nome della famiglia di pacchetti dell'app UWP per cui verranno generati i file PRI. Questo valore verrà usato come nome della mappa delle risorse quando in seguito si genera un file PRI da questo indicizzatore di risorse.

</dd> <dt>

*projectRoot* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Radice del progetto dell'app UWP per cui verranno generati i file PRI. In altre parole, il percorso dei file di risorse dell'app. È possibile specificare questo valore in modo che sia possibile specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.

</dd> <dt>

*platformVersion* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versione della piattaforma di destinazione per l'indicizzatore di risorse.

</dd> <dt>

*defaultQualifiers* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco di qualificatori di risorse predefiniti. Ad esempio, L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*indicizzatore* \[ in, out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Puntatore a un handle dell'indicizzatore di risorse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1803 \[\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo \[ app desktop server\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

