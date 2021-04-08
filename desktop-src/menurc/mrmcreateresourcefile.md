---
title: Funzione MrmCreateResourceFile (MrmResourceIndexer. h)
description: Crea un file PRI (denominato \ 0034; resources. pri \ 0034;) o file su disco nella cartella specificata. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menu della funzione MrmCreateResourceFile e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80294e5829dbf90c8aa3b0f6485c2da4185add1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743063"
---
# <a name="mrmcreateresourcefile-function"></a>MrmCreateResourceFile (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea un file PRI (denominato "resources. pri") o file su disco nella cartella specificata. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ in\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse da cui creare il file PRI.

</dd> <dt>

*packagingMode* \[ in\]
</dt> <dd>

Tipo: **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Specifica se il file PRI deve essere autonomo, suddividerlo automaticamente in base al qualificatore di risorse oppure essere un pacchetto di risorse.

</dd> <dt>

*packagingOptions* \[ in\]
</dt> <dd>

Tipo: **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Specifica opzioni aggiuntive per il file PRI.

</dd> <dt>

*outputDirectory* 
</dt> <dd>

Tipo: **PCWSTR**

Percorso di una cartella in cui salvare il file PRI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

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

 

