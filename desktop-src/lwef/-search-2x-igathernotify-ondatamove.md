---
title: Metodo IGatherNotify OnDataMove (deprecato)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify OnDataMove (deprecato)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Metodo OnDataMove (deprecato) funzionalità dell'ambiente Windows legacy
- Metodo OnDataMove (deprecato) funzionalità dell'ambiente Windows legacy, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, metodo OnDataMove (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353006"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Metodo IGatherNotify:: OnDataMove (deprecato)

\[**OnDataMove** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.

Questo metodo notifica all'indicizzatore i dati spostati. Quando Invia la notifica all'indicizzatore, include l'indirizzo precedente, il nuovo indirizzo e l'indirizzo logico.

## <a name="syntax"></a>Sintassi


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*eChangeAdviseSemantics* \[ in\]
</dt> <dd>

Tipo: **Long**

Parametro enumerato che descrive il tipo di spostamento che si è verificato.

</dd> <dt>

*bstrOldAddress* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo precedente dell'elemento spostato. Per i file normali,*eChangeAdviseSematics* è **null**. Per una cartella o una directory, impostare *eChangeAdviseSematics* su \_ gthr \_ directory semantica CA \_ .

</dd> <dt>

*bstrNewAddress* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Nuovo indirizzo dell'elemento spostato.

</dd> <dt>

*bstrLogicalAddress* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo logico dell'elemento spostato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

 

 
