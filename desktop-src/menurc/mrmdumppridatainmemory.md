---
title: Funzione MrmDumpPriDataInMemory (MrmResourceIndexer.h)
description: Esegue il dump delle informazioni PRI (come BLOB in memoria, creato da una precedente chiamata a MrmCreateResourceFileInMemory) nell'equivalente XML (come dati in memoria), per renderle più leggibili.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menu e altre risorse della funzione MrmDumpPriDataInMemory
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbeec26f0741ebb77b742ff647e91cb5fd18afe633a1519228b887b4b438bb72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601781"
---
# <a name="mrmdumppridatainmemory-function"></a>Funzione MrmDumpPriDataInMemory

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Esegue il dump delle informazioni PRI (come BLOB in memoria, creato da una precedente chiamata a [**MrmCreateResourceFileInMemory)**](mrmcreateresourcefileinmemory.md)nell'equivalente XML (come dati in memoria), per renderle più leggibili. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData.* Chiamare [**MrmFreeMemory con**](mrmfreememory.md) lo stesso puntatore per liberare la memoria. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*inputPriData* \[ Pollici\]
</dt> <dd>

Tipo: **\* BYTE**

Puntatore ai dati PRI creati da una chiamata precedente a [**MrmCreateResourceFileInMemory.**](mrmcreateresourcefileinmemory.md)

</dd> <dt>

*inputPriSize* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Dimensioni dei dati a cui punta *inputPriData.*

</dd> <dt>

*schemaPriData* \[ in, facoltativo\]
</dt> <dd>

Tipo: **\* BYTE**

Puntatore facoltativo alle informazioni PRI (come BLOB in memoria) che rappresenta i dati dello schema creati da una precedente chiamata a [**MrmCreateResourceFileInMemory.**](mrmcreateresourcefileinmemory.md) Non liberare *schemaPriData* fino a quando non si è terminato di usare l'indicizzatore di risorse. Vedere anche La sezione Osservazioni.

</dd> <dt>

*schemaPriSize* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Dimensioni dei dati a cui punta *schemaPriData.*

</dd> <dt>

*dumpType* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmDumpType**](mrmdumptype.md)**

Specifica il livello di dettaglio del dump XML o se è necessario eseguire il dump di uno schema.

</dd> <dt>

*outputXmlData* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* BYTE**

Indirizzo di un puntatore a BYTE. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData.* Chiamare [**MrmFreeMemory con**](mrmfreememory.md) il puntatore a BYTE per liberare la memoria.

</dd> <dt>

*outputXmlSize* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

Indirizzo di un ULONG. In *outputXmlSize* la funzione restituisce le dimensioni della memoria allocata a cui punta *outputXmlData.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Un pacchetto di risorse senza schema è quello creato con l'argomento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passato a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con l'opzione *omitSchemaFromResourcePacks* nel file di configurazione PRI). Per eseguire il dump di un pacchetto di risorse senza schema, passare il percorso ai dati PRI del pacchetto principale come argomento per il *parametro schemaPriData.*

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

 

