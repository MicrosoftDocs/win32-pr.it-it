---
title: Funzione MrmCreateConfigInMemory (MrmResourceIndexer.h)
description: Crea nuove informazioni di configurazione PRI inizializzate (come dati in memoria, non come file) definendo le impostazioni predefinite del qualificatore specificate.
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
ms.openlocfilehash: b30b4a64313952d48662a82e2f62cdef25106136e7757220668fc094c9258d4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011791"
---
# <a name="mrmcreateconfiginmemory-function"></a>Funzione MrmCreateConfigInMemory

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Crea nuove informazioni di configurazione PRI inizializzate (come dati in memoria, non come file) definendo le impostazioni predefinite del qualificatore specificate. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*. Chiamare [**MrmFreeMemory con**](mrmfreememory.md) lo stesso puntatore per liberare la memoria. Per altre informazioni e procedure dettagliate basate su scenario su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti e sistemi [di compilazione personalizzati.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

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

*platformVersion* \[ Pollici\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versione della piattaforma (*targetOsVersion*) da usare per le informazioni di configurazione generate.

</dd> <dt>

*defaultQualifiers* \[ in, facoltativo\]
</dt> <dd>

Tipo: **PCWSTR**

Elenco di qualificatori di risorse predefiniti. Ad esempio, L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*outputXmlData* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* BYTE**

Indirizzo di un puntatore a BYTE. La funzione alloca memoria e restituisce un puntatore a tale memoria in *outputXmlData*. Chiamare [**MrmFreeMemory con**](mrmfreememory.md) il puntatore a BYTE per liberare tale memoria.

</dd> <dt>

*outputXmlSize* \[ Cambio\]
</dt> <dd>

Tipo: **ULONG \***

Indirizzo di un ULONG. In *outputXmlSize* la funzione restituisce le dimensioni della memoria allocata a cui punta *outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Usare le macro SUCCEEDED() o FAILED() (definite in winerror.h) per determinare l'esito positivo o negativo.

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

 

