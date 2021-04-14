---
title: Funzione MrmCreateResourceFileInMemory (MrmResourceIndexer. h)
description: Crea informazioni PRI come BLOB in memoria, non come file su disco.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menu della funzione MrmCreateResourceFileInMemory e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478652"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>MrmCreateResourceFileInMemory (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea informazioni PRI come BLOB in memoria, non come file su disco. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputPriData*. Chiamare [**MrmFreeMemory**](mrmfreememory.md) con lo stesso puntatore per liberare la memoria. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ in\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse da cui creare le informazioni PRI.

</dd> <dt>

*packagingMode* \[ in\]
</dt> <dd>

Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Specifica se le informazioni PRI devono essere autonome o essere un pacchetto di risorse. **MrmPackagingModeAutoSplit** non è supportato.

</dd> <dt>

*packagingOptions* \[ in\]
</dt> <dd>

Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Specifica opzioni aggiuntive per le informazioni sul PRI.

</dd> <dt>

*outputPriData* \[ out\]
</dt> <dd>

Tipo: **byte \* \***

Indirizzo di un puntatore a BYTE. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputPriData*. Chiamare [**MrmFreeMemory**](mrmfreememory.md) con il puntatore a byte per liberare la memoria.

</dd> <dt>

*outputPriSize* \[ out\]
</dt> <dd>

Tipo: **ULONG \** _

Indirizzo di ULONG. In _outputPriSize *, la funzione restituisce le dimensioni della memoria allocata a cui punta *outputPriData*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Se si passa *outputPriData* a [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), non liberare la memoria fino a quando non viene terminato di usare l'indicizzatore di risorse.

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

 

