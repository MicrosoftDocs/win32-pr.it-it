---
title: Metodo IGatherNotify OnDataMove (deprecato)
description: Questo Windows'interfaccia di Desktop Search è deprecato e viene sostituito dall'API ISearchPersistentItemsChangedSink di Windows Search nell'SDK Windows. | Metodo IGatherNotify OnDataMove (deprecato)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Metodo OnDataMove (deprecato) Funzionalità dell'Windows legacy
- Metodo OnDataMove (deprecato) Legacy Windows Environment Features , interfaccia IGatherNotify
- Metodo OnDataMove (deprecato) dell'Windows IGatherNotify legacy Windows Environment Features
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3d4f7d91bc9e9741f227812997a820ab4180ccf438d52ae8cfea93f67dc0bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665871"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Metodo IGatherNotify::OnDataMove (deprecato)

\[**OnDataMove** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo Windows'interfaccia di Desktop Search è deprecato e viene sostituito dall'API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) di Windows Search nell'SDK Windows.

Questo metodo notifica all'indicizzatore i dati spostati. Quando invia la notifica all'indicizzatore, include l'indirizzo precedente, il nuovo indirizzo e l'indirizzo logico.

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

*eChangeAdviseSemantics* \[ Pollici\]
</dt> <dd>

Tipo: **long**

Parametro enumerato che descrive il tipo di spostamento che si è verificato.

</dd> <dt>

*bstrOldAddress* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo precedente dell'elemento spostato. Per i file normali,*eChangeAdviseSematics* è **NULL.** Per una cartella o una directory, impostare *eChangeAdviseSematics* su GTHR \_ CA \_ SEMANTICS \_ DIRECTORY.

</dd> <dt>

*bstrNewAddress* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Nuovo indirizzo dell'elemento spostato.

</dd> <dt>

*bstrLogicalAddress* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo logico dell'elemento spostato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

 

 
