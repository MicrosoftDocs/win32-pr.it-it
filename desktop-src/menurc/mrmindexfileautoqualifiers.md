---
title: Funzione MrmIndexFileAutoQualifiers (MrmResourceIndexer. h)
description: Indicizza un file di risorse appartenente a un'app UWP. Deduce un elenco di qualificatori di risorse dal parametro FilePath. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menu della funzione MrmIndexFileAutoQualifiers e altre risorse
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
ms.openlocfilehash: 65254a8715073060e9b4fc1578b68d54ae987958
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119098"
---
# <a name="mrmindexfileautoqualifiers-function"></a>MrmIndexFileAutoQualifiers (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Indicizza un file di risorse appartenente a un'app UWP. Deduce un elenco di qualificatori di risorse dal parametro *filePath* . Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ in\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse che indicizza il file di risorse.

</dd> <dt>

*filePath* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso relativo di un file contenente una risorsa che si desidera indicizzare. Questo percorso è relativo alla radice del progetto dell'app UWP per cui si generano file PRI. La radice del progetto corrisponde al valore di *projectRoot* passato a [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Il segmento di nome file di *filePath* viene usato come nome della risorsa; i qualificatori di risorse e vengono derivati dal percorso. Se ad esempio si passa L "images \\ de-de \\ scale-100 \\background.png" a *filePath* , l'indicizzatore di risorse aggiunge una risorsa denominata "background.png" con i qualificatori di risorse "Language-de-de" e "scale-100".

L "files" verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.

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

 

