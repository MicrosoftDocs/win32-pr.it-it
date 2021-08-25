---
title: Funzione MrmCreateResourceIndexerFromPreviousPriData (MrmResourceIndexer.h)
description: Crea un indicizzatore di risorse dai dati PRI creati da una chiamata precedente a MrmCreateResourceFileInMemory. Per altre informazioni e procedure dettagliate basate su scenario su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti e sistemi di compilazione personalizzati.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Menu della funzione MrmCreateResourceIndexerFromPreviousPriData e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d178532a77e01bc724276b40881685e0ec44d5364617fd856ffc55acfd99cf98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952354"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a>Funzione MrmCreateResourceIndexerFromPreviousPriData

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea un indicizzatore di risorse dai dati PRI creati da una chiamata precedente a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md). Per altre informazioni e procedure dettagliate basate su scenario su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti e sistemi [di compilazione personalizzati.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

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

*priData* \[ Pollici\]
</dt> <dd>

Tipo: **\* BYTE**

Puntatore ai dati PRI creati da una chiamata precedente a [**MrmCreateResourceFileInMemory.**](mrmcreateresourcefileinmemory.md) Non liberare *priData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.

</dd> <dt>

*priSize* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Dimensioni dei dati a cui punta *priData.*

</dd> <dt>

*indicizzatore* \[ in, out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Puntatore a un handle dell'indicizzatore di risorse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Non liberare *priData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.

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

 

