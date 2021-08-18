---
title: Funzione MrmIndexString (MrmResourceIndexer.h)
description: Indicizza una singola risorsa stringa appartenente a un'app UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menu e altre risorse della funzione MrmIndexString
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99da5b63c08d0068553ca9240798eabe360671fa94139b31841831dd68df3958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687253"
---
# <a name="mrmindexstring-function"></a>Funzione MrmIndexString

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Indicizza una singola risorsa stringa appartenente a un'app UWP. Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorse. Per altre informazioni e procedure dettagliate basate su scenario su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti e sistemi [di compilazione personalizzati.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse che indicizza le risorse stringa.

</dd> <dt>

*resourceUri* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

URI della risorsa da assegnare alla risorsa. Il percorso verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.

</dd> <dt>

*resourceString* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Valore della risorsa stringa.

</dd> <dt>

*qualificatori* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco facoltativo di qualificatori di risorse, ad esempio L"language-en-US \_ scale-100 \_ contrast-standard". Una stringa vuota o **nullptr** indica una risorsa neutra. I qualificatori di *risorsa non* vengono dedotte da *resourceUri*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Se si vogliono specificare qualificatori di risorsa, passarli nel *parametro qualifiers.* I qualificatori di *risorsa non* vengono dedotte da *resourceUri*.

Il segmento di nome file *di resourceUri* viene usato come nome della risorsa.

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

 

