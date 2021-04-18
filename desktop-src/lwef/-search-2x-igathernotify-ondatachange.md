---
title: Metodo IGatherNotify OnDataChange (deprecato)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify OnDataChange (deprecato)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Metodo OnDataChange (deprecato) funzionalità dell'ambiente Windows legacy
- Metodo OnDataChange (deprecato) funzionalità dell'ambiente Windows legacy, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, Metodo OnDataChange (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321611"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Metodo IGatherNotify:: OnDataChange (deprecato)

\[**OnDataChange** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.

Questo metodo notifica all'indicizzatore i dati che sono stati modificati. Quando Invia la notifica all'indicizzatore, include il tipo di modifica, l'indirizzo fisico e l'indirizzo logico.

## <a name="syntax"></a>Sintassi


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*eChangeAdvise* \[ in\]
</dt> <dd>

Tipo: **Long**

Valore enumerato che specifica il tipo di modifica.

</dd> <dt>

*bstrPhysicalAddress* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo fisico dell'elemento modificato.

</dd> <dt>

*bstrLogicalAddress* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo logico dell'elemento modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

 

 
