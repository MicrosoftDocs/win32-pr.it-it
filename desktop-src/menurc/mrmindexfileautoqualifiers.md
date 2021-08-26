---
title: Funzione MrmIndexFileAutoQualifiers (MrmResourceIndexer.h)
description: Indicizza un file di risorse appartenente a un'app UWP. Deduce un elenco di qualificatori di risorsa dal parametro filePath. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti (PRI) e sistemi di compilazione personalizzati.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menu e altre risorse della funzione MrmIndexFileAutoQualifiers
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10dbdb564f7e2d830d1edea59be6ca6f11b72d2650a937f96b6d305b6c7f61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886731"
---
# <a name="mrmindexfileautoqualifiers-function"></a>Funzione MrmIndexFileAutoQualifiers

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Indicizza un file di risorse appartenente a un'app UWP. Deduce un elenco di qualificatori di risorsa dal *parametro filePath.* Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse che indicizza il file di risorse.

</dd> <dt>

*filePath* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso relativo di un file contenente una risorsa da indicizzare. Questo percorso è relativo alla radice del progetto dell'app UWP per cui si generano file PRI. La radice del progetto è il valore *di projectRoot* passato a [**MrmCreateResourceIndexer.**](mrmcreateresourceindexer.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Il segmento del nome file *di filePath* viene usato come nome della risorsa. e i qualificatori di risorsa derivano dal relativo percorso. Ad esempio, se si passa L"Images de-DE scale-100background.png" a filePath, l'indicizzatore di risorse aggiunge una risorsa denominata "background.png" con qualificatori di risorsa \\ \\ \\ "language-de-DE" e "scale-100". 

L"Files" verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.

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

 

