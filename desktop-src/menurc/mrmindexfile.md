---
title: Funzione MrmIndexFile (MrmResourceIndexer.h)
description: Indicizza un file di risorse appartenente a un'app UWP. Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorsa. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti (PRI) e sistemi di compilazione personalizzati.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menu e altre risorse della funzione MrmIndexFile
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004e8d81f3af7d0aa7844ed5661f71713db3f7fc49616fba0d56bed833a87f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733681"
---
# <a name="mrmindexfile-function"></a>Funzione MrmIndexFile

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Indicizza un file di risorse appartenente a un'app UWP. Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorsa. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse che indicizza il file di risorse.

</dd> <dt>

*resourceUri* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

URI della risorsa da assegnare alla risorsa. Il percorso verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.

</dd> <dt>

*filePath* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso relativo di un file contenente una risorsa da indicizzare. Questo percorso è relativo alla radice del progetto dell'app UWP per cui si generano file PRI. La radice del progetto è il valore *di projectRoot* passato a [**MrmCreateResourceIndexer.**](mrmcreateresourceindexer.md)

</dd> <dt>

*qualificatori* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco facoltativo di qualificatori di risorsa, ad esempio L"language-en-US \_ scale-100 \_ contrast-standard". Una stringa vuota o **nullptr** indica una risorsa neutra. I qualificatori di risorsa *non vengono* dedotte da *resourceUri* né da *containerPath.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Se si vogliono specificare qualificatori di risorsa, passarli nel *parametro qualifiers.* I qualificatori di *risorsa non* vengono dedotte da *resourceUri* né da *filePath.*

Il segmento del nome file *di resourceUri* (non *filePath*) viene usato come nome della risorsa.

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

 

