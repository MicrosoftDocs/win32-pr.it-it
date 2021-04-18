---
title: Funzione MrmCreateResourceIndexerFromPreviousPriFile (MrmResourceIndexer. h)
description: Crea un indicizzatore di risorse da un file PRI creato con una chiamata precedente a MrmCreateResourceFile. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Menu della funzione MrmCreateResourceIndexerFromPreviousPriFile e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301716"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a>MrmCreateResourceIndexerFromPreviousPriFile (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea un indicizzatore di risorse da un file PRI creato con una chiamata precedente a [**MrmCreateResourceFile**](mrmcreateresourcefile.md). Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
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

*priFile* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso di file completo di un file PRI.

</dd> <dt>

*indicizzatore* \[ in uscita\]
</dt> <dd>

Tipo: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

Puntatore a un handle dell'indicizzatore di risorse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

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

 

