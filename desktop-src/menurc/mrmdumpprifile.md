---
title: Funzione MrmDumpPriFile (MrmResourceIndexer. h)
description: Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come file su disco), in modo da renderlo più facilmente leggibile.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menu della funzione MrmDumpPriFile e altre risorse
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741826"
---
# <a name="mrmdumpprifile-function"></a>MrmDumpPriFile (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Consente di eseguire il dump di un file PRI (binario) al relativo equivalente XML (come file su disco), in modo da renderlo più facilmente leggibile. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
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

*outputXmlFile* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

Percorso di un file XML da creare.

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

 

