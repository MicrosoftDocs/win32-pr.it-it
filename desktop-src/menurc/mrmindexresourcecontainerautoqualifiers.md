---
title: Funzione MrmIndexResourceContainerAutoQualifiers (MrmResourceIndexer. h)
description: Indicizza le risorse di stringa contenute in un file di risorse (con estensione resw/resjson) o con estensione PRIInfo o prifile, appartenenti a un'app UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menu della funzione MrmIndexResourceContainerAutoQualifiers e altre risorse
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234566d166e73f75a70b6e613d3f0dfda648ff7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302320"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a>MrmIndexResourceContainerAutoQualifiers (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Indicizza le risorse di stringa contenute in un file di risorse (con estensione resw/resjson) o con estensione PRIInfo o prifile, appartenenti a un'app UWP. Deduce un elenco di qualificatori di risorse dal parametro *containerPath* . Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ in\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse che indicizza le risorse di stringa.

</dd> <dt>

*containerPath* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso relativo di un oggetto. resw,. resjson,. PRIInfo o. prifile che contiene le risorse di stringa che si desidera indicizzare. Questo percorso è relativo alla radice del progetto dell'app UWP per cui si generano file PRI. La radice del progetto corrisponde al valore di *projectRoot* passato a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

I qualificatori di risorse vengono dedotti da *containerPath*. Ad esempio, un valore di L "en-US \\ \\ Resources. resw" aggiunge risorse di stringa con il qualificatore "Language-en-US".

Il nome del file di risorse verrà usato come nome del sottoalbero della mappa risorse per queste risorse quando in seguito si genera un file PRI da questo indicizzatore di risorse.

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

 

