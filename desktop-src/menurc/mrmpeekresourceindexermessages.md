---
title: Funzione MrmPeekResourceIndexerMessages (MrmResourceIndexer. h)
description: Consente di visualizzare tutti i messaggi generati da un indicizzatore di risorse. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere API PRI (Package Resource Indexing) e sistemi di compilazione personalizzati.
ms.assetid: 87D093AE-7444-4778-8B9E-1D0D972C90E1
keywords:
- Menu della funzione MrmPeekResourceIndexerMessages e altre risorse
topic_type:
- apiref
api_name:
- MrmPeekResourceIndexerMessages
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45599865633afa413594be7e82b0c7ace853434b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048426"
---
# <a name="mrmpeekresourceindexermessages-function"></a>MrmPeekResourceIndexerMessages (funzione)

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Consente di visualizzare tutti i messaggi generati da un indicizzatore di risorse. Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintassi


```C++
HRESULT HRESULT MrmPeekResourceIndexerMessages(
  _In_  MrmResourceIndexerHandle  indexer,
  _Out_ MrmResourceIndexerMessage **messages,
  _Out_ ULONG                     *numMsgs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*indicizzatore* \[ in\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle che identifica l'indicizzatore di risorse di cui si desidera visualizzare i messaggi.

</dd> <dt>

*messaggi* \[ di out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerMessage**](mrmresourceindexermessage.md)\*\***

Puntatore a un puntatore a un [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md). La funzione alloca una matrice di **MrmResourceIndexerMessage** e restituisce un puntatore a tale memoria nei *messaggi*. Non liberare il puntatore il cui indirizzo viene passato ai *messaggi*.

</dd> <dt>

*numMsgs* \[ out\]
</dt> <dd>

Tipo: **ULONG \** _

Numero di messaggi restituiti in _messages *.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

S \_ OK se la funzione ha avuto esito positivo, in caso contrario un altro valore. Utilizzare le macro SUCCEEDed () o FAILED () (definite in Winerror. h) per determinare l'esito positivo o negativo.

## <a name="remarks"></a>Commenti

L'app non è proprietaria della memoria allocata e restituita nei *messaggi*, quindi non è disponibile.

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

 

