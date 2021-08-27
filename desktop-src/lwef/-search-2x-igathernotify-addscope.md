---
title: Metodo IGatherNotify AddScope (deprecato)
description: Questo Windows'interfaccia di Desktop Search è deprecato e viene sostituito dall'API ISearchPersistentItemsChangedSink di Windows Search in Windows SDK. | Metodo IGatherNotify AddScope (deprecato)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Metodo AddScope (deprecato) Legacy Windows Environment Features
- Metodo AddScope (deprecato) Legacy Windows Environment Features , interfaccia IGatherNotify
- Interfaccia IGatherNotify Legacy Windows, metodo AddScope (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a49c0cf652b0cfde59167fa98498a978d3c2c41d3a886ee092b8f4a28d35f61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755592"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Metodo IGatherNotify::AddScope (deprecato)

\[**AddScope** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]

Questo Windows'interfaccia di Desktop Search è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) in Windows SDK.

Aggiunge la pagina iniziale o l'URL che si sta monitorando. Viene avviata una ricerca per indicizzazione incrementale quando ci si connette e quindi si presuppone che tutte le altre modifiche all'URL siano tramite notifica.

## <a name="syntax"></a>Sintassi


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrScope* \[ Pollici\]
</dt> <dd>

Tipo: **BSTR**

Stringa che specifica la pagina iniziale o l'URL che si sta monitorando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiamata a questo metodo avvia una ricerca per indicizzazione incrementale quando si è connessi all'archivio. Successivamente, si presuppone che tutte le modifiche dell'URL siano notificate dopo l'aggiornamento iniziale.

 

 
