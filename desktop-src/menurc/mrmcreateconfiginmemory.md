---
title: Funzione MrmCreateConfigInMemory (MrmResourceIndexer. h)
description: Crea le informazioni di configurazione PRI nuove inizializzate (come i dati in memoria, non come file) definendo le impostazioni predefinite del qualificatore specificate.
ms.assetid: D8822D6E-5F68-46A1-B99F-52575DB1D277
keywords:
- Menu della funzione MrmCreateConfigInMemory e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateConfigInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d809ac640061ecf8bd51b9e2016aefe537b1ee8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518694"
---
# <a name="mrmcreateconfiginmemory-function"></a>MrmCreateConfigInMemory (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea le informazioni di configurazione PRI nuove inizializzate (come i dati in memoria, non come file) definendo le impostazioni predefinite del qualificatore specificate. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*. Chiamare [**MrmFreeMemory**](mrmfreememory.md) con lo stesso puntatore per liberare la memoria. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateConfigInMemory(
  _In_     MrmPlatformVersion platformVersion,
  _In_opt_ PCWSTR             defaultQualifiers,
  _Out_    BYTE               **outputXmlData,
  _Out_    ULONG              *outputXmlSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*platformVersion* \[ in\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versione della piattaforma (*targetOsVersion*) da usare per le informazioni di configurazione generate.

</dd> <dt>

*defaultQualifiers* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco di qualificatori di risorse predefiniti. Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"

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

 

