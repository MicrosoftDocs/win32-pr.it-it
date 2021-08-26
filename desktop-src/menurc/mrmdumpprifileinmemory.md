---
title: Funzione MrmDumpPriFileInMemory (MrmResourceIndexer.h)
description: Esegue il dump di un file PRI (binario) nell'equivalente XML (come dati in memoria), per renderlo più leggibile.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menu e altre risorse della funzione MrmDumpPriFileInMemory
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c591f95b772d71fd0ce614598bbf793d84dff70a0c29664da460c8be33569d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092151"
---
# <a name="mrmdumpprifileinmemory-function"></a>Funzione MrmDumpPriFileInMemory

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Esegue il dump di un file PRI (binario) nell'equivalente XML (come dati in memoria), per renderlo più leggibile. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData.* Chiamare [**MrmFreeMemory con**](mrmfreememory.md) lo stesso puntatore per liberare la memoria. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indexFileName* \[ Pollici\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso completo di un file PRI. Si tratta del file PRI che verrà scaricato in XML.

</dd> <dt>

*schemaPriFile* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso completo facoltativo di un file di schema (o di un file PRI che rappresenta uno schema; vedere la sezione Osservazioni).

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

Un pacchetto di risorse senza schema è quello creato con l'argomento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passato a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con l'opzione *omitSchemaFromResourcePacks* nel file di configurazione PRI). Per eseguire il dump di un pacchetto di risorse senza schema, passare il percorso ai dati PRI del pacchetto principale come argomento per il *parametro schemaPriFile.*

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

 

