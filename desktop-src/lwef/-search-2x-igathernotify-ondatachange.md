---
title: Metodo IGatherNotify OnDataChange (deprecato)
description: Questo Windows dell'interfaccia di Desktop Search è deprecato e viene sostituito dall'API ISearchPersistentItemsChangedSink di Windows Search nell'SDK Windows. | Metodo IGatherNotify OnDataChange (deprecato)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Metodo OnDataChange (deprecato) Legacy Windows Environment Features
- Metodo OnDataChange (deprecato) Legacy Windows Environment Features , interfaccia IGatherNotify
- Interfaccia IGatherNotify Legacy Windows, metodo OnDataChange (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95533a7937136a0f828a292efe7e398258e3c880974e031d9d7d2797f721f2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481595"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Metodo IGatherNotify::OnDataChange (deprecato)

\[**OnDataChange può** essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo Windows'interfaccia di Desktop Search è deprecato e viene sostituito dall'API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) di Windows Search nell'SDK Windows.

Questo metodo notifica all'indicizzatore i dati modificati. Quando invia la notifica all'indicizzatore, include il tipo di modifica, l'indirizzo fisico e l'indirizzo logico.

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

*eChangeAdvise* \[ Pollici\]
</dt> <dd>

Tipo: **long**

Valore enumerato che specifica il tipo di modifica.

</dd> <dt>

*bstrPhysicalAddress* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo fisico dell'elemento modificato.

</dd> <dt>

*bstrLogicalAddress* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Indirizzo logico dell'elemento modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

 

 
