---
title: Funzione MrmCreateResourceIndexerFromPreviousSchemaData (MrmResourceIndexer. h)
description: Crea un indicizzatore di risorse da dati dello schema in memoria creati con una chiamata precedente a MrmDumpPriFileInMemory o MrmDumpPriDataInMemory.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Menu della funzione MrmCreateResourceIndexerFromPreviousSchemaData e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477153"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a>MrmCreateResourceIndexerFromPreviousSchemaData (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea un indicizzatore di risorse da dati dello schema in memoria creati con una chiamata precedente a [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md). Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*projectRoot* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

La radice del progetto dell'app UWP per cui verranno generati i file PRI. In altre parole, il percorso dei file di risorse dell'app. Questa impostazione viene specificata in modo che sia possibile specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.

</dd> <dt>

*platformVersion* \[ in\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versione della piattaforma di destinazione per l'indicizzatore di risorse.

</dd> <dt>

*defaultQualifiers* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco di qualificatori di risorse predefiniti. Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"

</dd> <dt>

*schemaXmlData* \[ in\]
</dt> <dd>

Tipo: **byte \** _

Puntatore ai dati dello schema creati da una precedente chiamata a [_ *MrmDumpPriFileInMemory* *](mrmdumpprifileinmemory.md) o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md). Non liberare *schemaXmlData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.

</dd> <dt>

*schemaXmlSize* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Dimensione dei dati a cui punta *schemaXmlData*.

</dd> <dt>

*indicizzatore* \[ in uscita\]
</dt> <dd>

Tipo: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

Puntatore a un handle dell'indicizzatore di risorse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Non liberare *schemaXmlData* fino al termine dell'uso dell'indicizzatore di risorse creato da questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1803 \[\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[API per l'indicizzazione delle risorse del pacchetto e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

