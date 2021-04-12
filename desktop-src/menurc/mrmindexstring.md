---
title: Funzione MrmIndexString (MrmResourceIndexer. h)
description: Indicizza una singola risorsa di stringa che appartiene a un'app UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menu della funzione MrmIndexString e altre risorse
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
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119095"
---
# <a name="mrmindexstring-function"></a>MrmIndexString (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Indicizza una singola risorsa di stringa che appartiene a un'app UWP. Accetta un elenco esplicito (ma facoltativo) di qualificatori di risorse. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*indicizzatore* \[ in\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse che indicizza le risorse di stringa.

</dd> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

URI della risorsa da assegnare alla risorsa. Il percorso verrà usato come nome del sottoalbero della mappa delle risorse per questa risorsa quando in seguito si genera un file PRI da questo indicizzatore di risorse.

</dd> <dt>

*resourceString* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

Valore della risorsa di stringa.

</dd> <dt>

*qualificatori* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco facoltativo di qualificatori di risorse, ad esempio L "lingua-en-US \_ scale-100 \_ contrasto-standard". Una stringa vuota o **nullptr** indica una risorsa neutra. I qualificatori di risorse *non* vengono dedotti da *resourceUri*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Se si desidera specificare i qualificatori delle risorse, passarli nel parametro *Qualifiers* . I qualificatori di risorse *non* vengono dedotti da *resourceUri*.

Il segmento di nome file di *resourceUri* viene usato come nome della risorsa.

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

 

