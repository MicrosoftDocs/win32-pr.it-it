---
title: Funzione MrmCreateResourceIndexerFromPreviousSchemaFile (MrmResourceIndexer.h)
description: Crea un indicizzatore di risorse da un file di schema creato con una chiamata precedente a MrmDumpPriFile. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti (PRI) e sistemi di compilazione personalizzati.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Menu della funzione MrmCreateResourceIndexerFromPreviousSchemaFile e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622fe76c9206b4a8223d27d810f3d02bc0dca1d08730623b595ead24eab719d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847371"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a>Funzione MrmCreateResourceIndexerFromPreviousSchemaFile

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea un indicizzatore di risorse da un file di schema creato con una precedente chiamata a [**MrmDumpPriFile.**](mrmdumpprifile.md) Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*projectRoot* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Radice del progetto dell'app UWP per cui verranno generati i file PRI. In altre parole, il percorso dei file di risorse dell'app. Specificare questo valore in modo da poter specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.

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

*schemaFile* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso completo di un file di schema creato da una precedente chiamata a [**MrmDumpPriFile.**](mrmdumpprifile.md)

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

 

