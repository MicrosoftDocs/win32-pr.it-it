---
title: Funzione MrmDumpPriFileInMemory (MrmResourceIndexer. h)
description: Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come dati in memoria), in modo da renderlo più facilmente leggibile.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menu della funzione MrmDumpPriFileInMemory e altre risorse
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
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301024"
---
# <a name="mrmdumpprifileinmemory-function"></a>MrmDumpPriFileInMemory (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come dati in memoria), in modo da renderlo più facilmente leggibile. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*. Chiamare [**MrmFreeMemory**](mrmfreememory.md) con lo stesso puntatore per liberare la memoria. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*indexFileName* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso di file completo di un file PRI. Si tratta del file PRI di cui verrà eseguito il dump in XML.

</dd> <dt>

*schemaPriFile* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso file completo facoltativo di un file di schema o di un file PRI che rappresenta uno schema. vedere la sezione Osservazioni.

</dd> <dt>

*dumpType* \[ in\]
</dt> <dd>

Tipo: **[ **MrmDumpType**](mrmdumptype.md)**

Specifica il modo in cui il dump XML deve essere dettagliato o se deve essere eseguito il dump di uno schema.

</dd> <dt>

*outputXmlData* \[ out\]
</dt> <dd>

Tipo: **byte \* \***

Indirizzo di un puntatore a BYTE. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*. Chiamare [**MrmFreeMemory**](mrmfreememory.md) con il puntatore a byte per liberare la memoria.

</dd> <dt>

*outputXmlSize* \[ out\]
</dt> <dd>

Tipo: **ULONG \** _

Indirizzo di ULONG. In _outputXmlSize *, la funzione restituisce le dimensioni della memoria allocata a cui punta *outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

Un pacchetto di risorse senza schema è uno creato con l'argomento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passato a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (oppure con l'opzione *omitSchemaFromResourcePacks* nel file di configurazione pri). Per eseguire il dump di un pacchetto di risorse senza schema, passare il percorso ai dati PRI del pacchetto principale come argomento per il parametro *schemaPriFile* .

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

 

