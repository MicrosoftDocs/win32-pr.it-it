---
title: Funzione MrmCreateResourceFileInMemory (MrmResourceIndexer.h)
description: Crea informazioni PRI come BLOB in memoria, non come file su disco.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menu e altre risorse della funzione MrmCreateResourceFileInMemory
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
ms.openlocfilehash: ff34ddaab25f47f537c1270ad3a70719a43e2e1efa978fbad19cbe9ae77ba937
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886751"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>Funzione MrmCreateResourceFileInMemory

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea informazioni PRI come BLOB in memoria, non come file su disco. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputPriData*. Chiamare [**MrmFreeMemory con**](mrmfreememory.md) lo stesso puntatore per liberare la memoria. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.

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

*indicizzatore* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse da cui creare le informazioni PRI.

</dd> <dt>

*packagingMode* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Specifica se le informazioni PRI devono essere autonome o essere un pacchetto di risorse. **MrmPackagingModeAutoSplit** non è supportato.

</dd> <dt>

*packagingOptions* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Specifica opzioni aggiuntive sulle informazioni PRI.

</dd> <dt>

*outputPriData* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* BYTE**

Indirizzo di un puntatore a BYTE. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputPriData*. Chiamare [**MrmFreeMemory con**](mrmfreememory.md) il puntatore a BYTE per liberare la memoria.

</dd> <dt>

*outputPriSize* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

Indirizzo di un ULONG. In *outputPriSize* la funzione restituisce le dimensioni della memoria allocata a cui punta *outputPriData.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Se si passa *outputPriData* a [**MrmCreateResourceIndexerFromPreviousPriData,**](mrmcreateresourceindexerfrompreviouspridata-.md)non liberare la memoria fino a quando non si è terminato di usare l'indicizzatore di risorse.

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

 

