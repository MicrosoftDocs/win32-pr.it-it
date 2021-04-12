---
title: Funzione MrmCreateResourceIndexer (MrmResourceIndexer. h)
description: Consente di creare un indicizzatore di risorse, usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menu della funzione MrmCreateResourceIndexer e altre risorse
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400856"
---
# <a name="mrmcreateresourceindexer-function"></a>MrmCreateResourceIndexer (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Consente di creare un indicizzatore di risorse, usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*packageFamilyName* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

Nome della famiglia di pacchetti dell'app UWP per cui verranno generati i file PRI. Questo valore verrà usato come nome della mappa delle risorse quando in seguito si genera un file PRI da questo indicizzatore di risorse.

</dd> <dt>

*projectRoot* \[ in\]
</dt> <dd>

Tipo: **PCWSTR**

La radice del progetto dell'app UWP per cui verranno generati i file PRI. In altre parole, il percorso dei file di risorse dell'app. Questa impostazione viene specificata in modo che sia possibile specificare i percorsi relativi a tale radice nelle chiamate API successive allo stesso indicizzatore di risorse.

</dd> <dt>

*platformVersion* \[ in\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versione della piattaforma di destinazione per l'indicizzatore di risorse.

</dd> <dt>

*defaultQualifiers* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco di qualificatori di risorse predefiniti. Ad esempio, L "lingua-en-US \_ scale-100 \_ contrasto-standard"

</dd> <dt>

*indicizzatore* \[ in uscita\]
</dt> <dd>

Tipo: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

Puntatore a un handle dell'indicizzatore di risorse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

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

 

